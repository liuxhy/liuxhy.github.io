---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Software engineer working on backend and distributed systems. Based in the San Jose, CA area.
[Download PDF]({{ base_path }}/files/Huiyu_Liu_Resume_SWE.pdf) ·
[GitHub](https://github.com/liuxhy) ·
[LinkedIn](https://www.linkedin.com/in/xinhuiyu-huiyu-liu)

Education
======

* **M.S. in Computer Science**, Georgia Institute of Technology — expected Dec 2026
  * Coursework: Graduate Algorithms (Data Structures & Algorithms), Operating Systems, Software Development Process, Machine Learning, Natural Language Processing
* **Ph.D. in Environmental Sciences**, University of Virginia — 2025
* **B.S. in Atmospheric Sciences**, Lanzhou University — 2019

Experience
======

**Software Engineer**, Dyneti Technologies — San Mateo, CA · Jun 2026 – Jul 2026

* Designed, developed, tested, and deployed an asynchronous fraud-detection workflow for a credit-card scanning mobile SDK, cutting scan-to-response latency by over 75% by decoupling server-side ML inference from the synchronous scan path
* Built a server-to-server Fraud Decision API allowing merchant backends to retrieve fraud results precomputed at scan time, eliminating a redundant second scan and query-time inference delay
* Defined the async lifecycle across a Java/Kotlin Android SDK and Node.js backend, covering API contracts, RDS-backed schemas, inference state transitions, and pending-result handling, while preserving backward compatibility for live partner integrations
* Owned releases end to end via GitHub Actions CI/CD, pairing automated unit/integration tests with multi-device instrumented tests covering async workflows, failure handling, and edge cases

**Software Engineer Intern**, IBSS Corp — Remote, US · Sep 2025 – May 2026

* Built TerraPrecise, a Python/FastAPI data platform ingesting forecast, station, and terrain data and serving location-specific weather risk products to React/Leaflet frontend clients and alerting workflows
* Designed the data layer around access patterns: PostgreSQL/PostGIS for subscriber and spatial metadata, TimescaleDB for forecast and observation time series, and S3 for large gridded outputs
* Deployed a Dockerized microservice architecture on AWS isolating GPU-based downscaling inference from lightweight API and alerting services, with Lambda driving event-driven ingestion
* Designed a cloud-native geospatial serving layer (eoAPI, STAC, COG, TiTiler) making gridded datasets discoverable, queryable, and servable as scalable map layers
* Shipped an internal Vertex AI chatbot streamlining HR support workflows, automating its knowledge-base updates with scheduled Cloud Run jobs that sync documents from Google Drive to Cloud Storage with safeguards against accidental deletion

**Software Engineer Intern**, TGS — Houston, TX · May 2024 – Aug 2024

* Built parallel data ingestion and transformation pipelines (Python/Xarray/Dask) on GCP processing 20 TB of simulation and offshore sensor data for a wind-energy analytics platform
* Cut data processing time 70% by redesigning Zarr and Parquet storage layouts and chunking strategies, letting analytics jobs handle larger datasets within fixed memory limits

**PhD Researcher (funded by NASA)**, University of Virginia — Charlottesville, VA · Aug 2019 – May 2025

* Wrote parallel Python pipelines (Xarray/Dask) for ingestion, quality control, and feature extraction across 100+ TB of satellite and model-derived data in Unix/Linux environments

Projects
======

See [Projects]({{ base_path }}/projects/) for detail.

* **Synchronized Distributed File System** — gRPC-based DFS in C++ with whole-file caching, CRC32 diffing, timestamp-based conflict resolution, server-side writer locks, and mutex-guarded concurrent client sessions
* **Multi-Agent Travel Planner** — eight Google ADK agents composed into a sequential pipeline with a bounded critic-refiner loop that validates and repairs itineraries before export
* **Expenses Tracker** — full-stack MERN application with JWT auth, deployed to AWS EC2

Skills
======

* **Languages:** Python, C++, Java, Kotlin, JavaScript/TypeScript, SQL
* **Distributed & Systems:** gRPC, Protobuf, concurrency (pthreads, mutexes), Dask, Docker, Unix/Linux
* **Backend & Web/Mobile:** Node.js, Express, FastAPI, React, Android SDK, REST APIs
* **Cloud & Tooling:** AWS (EC2, S3, Lambda, RDS), GCP (Vertex AI, Cloud Run, GCS), GitHub Actions CI/CD, Git, Claude Code
* **Data & ML:** PostgreSQL, PostGIS, TimescaleDB, Xarray, Parquet, Zarr, PyTorch, scikit-learn, production ML inference

---

<sub>For publications, teaching, conference presentations, and my academic CV, see the [academic archive]({{ base_path }}/academic/).</sub>
