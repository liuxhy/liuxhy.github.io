---
title: "Multi-Agent Travel Planner"
excerpt: "Eight Google ADK agents composed into a pipeline with a bounded critic-refiner loop that validates itineraries and repairs them before export."
collection: portfolio
---

A trip planner that turns a one-line request ("San Francisco to Lake Tahoe and Las Vegas,
Jan 10–20, $3000, driving") into a complete day-by-day itinerary with hotels, transport,
activities, and a cost breakdown.

**Architecture.** Eight agents composed into a `SequentialAgent` pipeline: route planning →
initial itinerary → refinement loop → export. The flight, hotel, and activity agents are not
peers in that pipeline — they are wrapped as `AgentTool`s and handed to a lead planner that
calls them as tools, so delegation is hierarchical rather than flat. State moves between
stages through shared session keys.

**Self-correction.** The refinement stage is a bounded `LoopAgent` containing a critic and a
refiner. The critic validates the plan against concrete rules — no 15-hour driving days, no
flights in a trip the user asked to drive, enough time to actually do the listed activities —
and returns either `APPROVED` or three specific corrections. The refiner applies them,
re-querying the flight and hotel agents as needed, and writes the revised plan back to the
same session key the critic reads from. Capped at two iterations.

**Grounding.** Flight search runs through `google_search`; weather comes from the Open-Meteo
API, with indoor alternatives suggested on days with a high rain probability. The final plan
is converted to structured JSON and exported as a day-by-day Excel file.

**Stack:** Python, Google ADK, Gemini 2.5 Flash Lite, Streamlit, Pandas, OpenPyXL

**Source:** [github.com/liuxhy/trip_planner_agent](https://github.com/liuxhy/trip_planner_agent)
