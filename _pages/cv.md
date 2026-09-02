---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Software engineer working on backend and geospatial data platforms, with a background in
large-scale data infrastructure.

[Download résumé (PDF)]({{ base_path }}/files/Huiyu_Liu_resume_Geospatial.pdf) ·
[GitHub](https://github.com/liuxhy) ·
[LinkedIn](https://www.linkedin.com/in/xinhuiyu-huiyu-liu) ·
[Google Scholar](https://scholar.google.com/citations?user=0fies7oAAAAJ&hl=en)

Experience
======

**Software Engineer**, Dyneti Technologies — San Mateo, CA · Jun 2026 – Jul 2026

* Designed, developed, tested, and deployed an end-to-end asynchronous processing workflow across a Java/Kotlin Android SDK, Node.js backend, and AWS RDS, cutting user-facing latency by over 75% by decoupling server-side ML inference from the synchronous request path
* Built a server-to-server decision API allowing partner backends to retrieve results precomputed at request time, eliminating a redundant second call and query-time inference delay
* Defined the async lifecycle across mobile and backend: API contracts, RDS-backed schemas, inference state transitions, and pending-result handling, while preserving backward compatibility for live partner integrations
* Owned releases end to end via GitHub Actions CI/CD, pairing automated unit/integration tests with multi-device instrumented tests covering async workflows, failure handling, and edge cases

**Software Engineer Intern**, IBSS Corp — Remote, US · Sep 2025 – May 2026

* Built TerraPrecise, a Python/FastAPI data platform ingesting forecast, station, and terrain datasets, storing gridded outputs in S3, and serving location-specific weather risk products to React/Leaflet clients and automated alerting workflows
* Implemented the data layer around access patterns: PostgreSQL/PostGIS for subscriber, location, and forecast metadata; TimescaleDB for location-level forecast and observation time series; and S3 for large gridded outputs
* Designed a cloud-native geospatial serving architecture using eoAPI, STAC, COG, and TiTiler, making gridded weather datasets discoverable, queryable, and servable as scalable map layers through standardized APIs
* Designed and deployed a Dockerized microservice architecture on AWS isolating GPU-based downscaling model inference from lightweight API and alerting services through shared data contracts, with Lambda supporting event-driven ingestion
* Built reproducible processing and validation workflows integrating HRRR forecasts, station observations, terrain, and high-resolution model outputs, with automated quality evaluation against independent ground observations
* Shipped an internal Vertex AI chatbot streamlining HR support workflows, automating its knowledge-base updates with scheduled Cloud Run jobs syncing documents from Google Drive to Cloud Storage

**Software Engineer Intern**, TGS — Houston, TX · May 2024 – Aug 2024

* Built parallel Python data pipelines (Xarray/Dask) on GCP processing 20 TB of numerical weather predictions and offshore lidar observations for a wind resource assessment platform
* Developed data-quality and ML-based bias-correction workflows combining model forecasts with observational data, improving wind-speed RMSE by 15% and producing calibrated datasets for downstream analytics
* Cut data processing time 70% by redesigning Zarr and Parquet storage layouts and chunking strategies, letting analytics jobs handle larger datasets within fixed memory limits

**PhD Researcher (funded by NASA)**, University of Virginia — Charlottesville, VA · Aug 2019 – May 2025

* Wrote reusable parallel Python pipelines (Xarray/Dask) for ingestion, quality control, and feature extraction across 100+ TB of satellite, reanalysis, and model-derived geospatial data in Unix/Linux environments
* Built a lightweight HTML/JS/Leaflet interface to visualize spatiotemporal analysis results from NetCDF datasets, enabling interactive exploration across time and location

Projects
======

See [Projects]({{ base_path }}/projects/) for detail.

* **Synchronized Distributed File System** — gRPC-based DFS in C++ with whole-file caching, CRC32 diffing, timestamp-based conflict resolution, server-side writer locks, and mutex-guarded concurrent client sessions
* **Multi-Agent Travel Planner** — eight Google ADK agents composed into a sequential pipeline with a bounded critic-refiner loop that validates and repairs itineraries before export
* **Expenses Tracker** — full-stack MERN application with JWT auth, deployed to AWS EC2

Skills
======

* **Geospatial & Data:** STAC, COG, TiTiler, eoAPI, PostgreSQL/PostGIS, TimescaleDB, Xarray, Dask, Zarr, Parquet, NetCDF
* **Languages:** Python, C++, Java, Kotlin, JavaScript/TypeScript, SQL
* **Backend & Web/Mobile:** FastAPI, Node.js, Express, React, Leaflet, Android SDK, REST APIs
* **Distributed & Systems:** gRPC, Protobuf, concurrency (pthreads, mutexes), Docker, Unix/Linux
* **Cloud & Tooling:** AWS (S3, Lambda, RDS, EC2, CloudWatch), GCP (Vertex AI, Cloud Run, GCS), GitHub Actions CI/CD, Git, Claude Code
* **Machine Learning:** PyTorch, TensorFlow, scikit-learn, production ML inference

Education
======

* **M.S. in Computer Science**, Georgia Institute of Technology — expected Dec 2026
  * Coursework: Graduate Algorithms (Data Structures & Algorithms), Operating Systems, Software Development Process, Machine Learning, Data & Visual Analytics
* **Ph.D. in Environmental Sciences**, University of Virginia — 2025
* **B.S. in Atmospheric Sciences**, Lanzhou University — 2019

Publications
======

Three first-author papers on atmospheric dynamics and climate model evaluation in
*Geophysical Research Letters* and *JGR: Atmospheres*. Full list, research summaries,
teaching, and conference presentations are in the
[academic archive]({{ base_path }}/academic/).
