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

# Experience

**Software Engineer**, Dyneti Technologies — San Mateo, CA · Jun 2026 – Jul 2026

- Designed, developed, tested, and deployed an end-to-end asynchronous processing workflow across a Java/Kotlin Android SDK, Node.js backend, and AWS RDS, cutting user-facing latency by over 75% by decoupling server-side ML inference from the synchronous request path
- Built a server-to-server decision API allowing partner backends to retrieve results precomputed at request time, eliminating a redundant second call and query-time inference delay
- Defined the async lifecycle across mobile and backend: API contracts, RDS-backed schemas, inference state transitions, and pending-result handling, while preserving backward compatibility for live partner integrations
- Owned releases end to end via GitHub Actions CI/CD, pairing automated unit/integration tests with multi-device instrumented tests covering async workflows, failure handling, and edge cases; served on-call rotations, debugging production issues via CloudWatch logs and Grafana dashboards

**Software Engineer Intern**, IBSS Corp — Remote, US · Sep 2025 – May 2026

- Built AWS Glue, Spark, and Sedona pipelines to ingest, validate, transform, and spatially align four heterogeneous raster and vector datasets (forecast, observation, terrain, and land-water masks) into standardized 3 km model inputs
- Designed the data layer around access patterns: PostgreSQL/PostGIS for relational and spatial metadata, TimescaleDB for 10M+ time-series points, and AWS S3 for TB-scale gridded outputs, enabling queries with p95 latency under 200 ms
- Served downscaled forecasts through FastAPI REST APIs and interactive React/TypeScript and Leaflet maps, supporting automated frost and heat alerts with 87% accuracy
- Designed a cloud-native geospatial serving architecture using eoAPI, STAC, COG, and TiTiler, making gridded weather datasets discoverable, queryable, and servable as scalable map layers through standardized APIs
- Deployed containerized microservices on AWS, using Lambda to trigger hourly event-driven ingestion and GPU-based CorrDiff inference for 3 km to 1 km downscaling, while isolating compute-intensive workloads from latency-sensitive services
- Built reproducible processing and validation workflows integrating HRRR forecasts, station observations, terrain, and high-resolution model outputs, with automated quality evaluation against independent ground observations
- Shipped an internal Vertex AI chatbot streamlining HR support workflows, automating its knowledge-base updates with scheduled Cloud Run jobs syncing documents from Google Drive to Cloud Storage

**Data Engineer Intern**, TGS — Houston, TX · May 2024 – Aug 2024

- Built scalable geospatial ETL pipelines on GCP using Python, Xarray, and Dask to ingest, validate, and harmonize 20 TB of gridded WRF outputs and offshore lidar observations across spatial, temporal, and vertical dimensions
- Developed data-quality and ML-based bias-correction workflows combining model forecasts with observational data, improving wind-speed RMSE by 15% and producing calibrated datasets for downstream analytics
- Designed cloud-optimized storage layouts for multidimensional raster and tabular data using Zarr and Parquet, reducing processing time 70% through optimized chunking and partitioning while supporting distributed, memory-efficient analytics

**PhD Researcher (funded by NASA)**, University of Virginia — Charlottesville, VA · Aug 2019 – May 2025

- Built reusable parallel Python/Xarray/Dask pipelines to ingest, quality-control, harmonize, and extract features from 100+ TB of satellite, reanalysis, and climate-model data on multi-node Slurm HPC clusters
- Packaged the pipelines as documented, version-controlled Python modules adopted by 2 research groups for their own datasets
- Authored 3 first-author publications in leading climate journals, presented at 7+ international conferences, and received the competitive NASA FINESST Fellowship and Best Student Presentation at the American Meteorological Society Annual Meeting

# Projects

See [Projects]({{ base_path }}/projects/) for detail.

- **Synchronized Distributed File System** — gRPC-based DFS in C++ with whole-file caching, CRC32 diffing, timestamp-based conflict resolution, server-side writer locks, and mutex-guarded concurrent client sessions
- **Multi-Agent Travel Planner** — eight Google ADK agents composed into a sequential pipeline with a bounded critic-refiner loop that validates and repairs itineraries before export
- **Expenses Tracker** — full-stack MERN application with JWT auth, deployed to AWS EC2

# Skills

- **Geospatial & Data:** STAC, COG, TiTiler, eoAPI, PostgreSQL/PostGIS, TimescaleDB, Xarray, Zarr, Parquet, NetCDF, GDAL, Leaflet, QGIS
- **Languages:** Python, C++, Java, Kotlin, JavaScript/TypeScript, SQL
- **Backend & Web/Mobile:** FastAPI, Node.js, Express, React, Android SDK, REST APIs
- **Distributed & Systems:** Spark/PySpark, Sedona, Dask, gRPC, Protobuf, concurrency (pthreads, mutexes), Docker, Unix/Linux
- **Cloud & Tooling:** AWS (S3, Lambda, RDS, EC2, CloudWatch), GCP (Vertex AI, Cloud Run, GCS), GitHub Actions CI/CD, Git, Claude Code
- **Machine Learning:** PyTorch, TensorFlow, scikit-learn, production ML inference

# Education

- **M.S. in Computer Science**, Georgia Institute of Technology — expected Dec 2026
  - Coursework: Graduate Algorithms (Data Structures & Algorithms), Operating Systems, Software Development Process, Machine Learning, Data & Visual Analytics
- **Ph.D. in Environmental Sciences**, University of Virginia — 2025
- **B.S. in Atmospheric Sciences**, Lanzhou University — 2019

# Publications

Three first-author papers on atmospheric dynamics and climate model evaluation in
_Geophysical Research Letters_ and _JGR: Atmospheres_. Full list, research summaries,
teaching, and conference presentations are in the
[academic archive]({{ base_path }}/academic/).
