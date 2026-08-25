# Richard Kim

**Data engineer specializing in geospatial data and hard-to-reach sources.**

I build ingestion systems for sources that do not cooperate: GIS endpoints, undocumented APIs, and records that arrive only as PDF reports.

Most recently, I designed and ran a platform called [CanPermits](https://canpermits.com) that consolidated **38 Canadian municipal and provincial data sources** into a single PostgreSQL schema on an unattended daily schedule, with spatial resolution across millions of records. Before that, I spent six years building genomics data pipelines in research labs: high\-volume batch processing, DAG orchestration, and reproducibility as a hard requirement.

I am open to data engineering roles and contract work.

---

### 🗺️ What I specialize in

**Geospatial data engineering.** PostGIS at production depth: 105 GiST spatial indexes, point-in-polygon resolution across millions of records, geocoding pipelines, geometry validation, and polygon-layer ingestion from GeoJSON and WFS sources with checksum manifests.

**Civic and property data.** Public data from 38 municipalities across 7 provinces, sourced in various formats: ArcGIS REST, Socrata, CKAN, OpenDataSoft, WFS, CSV drops, and PDF reports. A single canonical schema was built around these sources, so downstream consumers do not need to know which source a record came from. Open-data license compliance and PII handling included.

**Hard-target data acquisition.** Undocumented APIs, protobuf request construction, bot-detection handling, TLS fingerprint impersonation, and document extraction where no structured feed exists at all.

---

### 🏗️ Selected work

**[canpermits-platform](https://github.com/rkkims/canpermits-platform)**: multi-source ingestion platform
> 38 sources into a PostgreSQL schema, running unattended daily. Incremental sync with upstream change detection, point-in-polygon spatial resolution against boundary layers, and asymmetric PII gating. The public repo above is the curated extract of a production system that was retired in August 2026.
> 
> `Python` `PostgreSQL` `PostGIS` `FastAPI` `Docker` `GCP`

**[googleflight-scraper](https://github.com/rkkims/googleflight-scraper)**:
> Google Flights’ base64-wrapped protobuf payload can be decoded into positionally indexed arrays. For round-trip flights, the outbound flight search result is reconstructed as protobuf and fed into the return-flight search.
> 
> `JavaScript` `protobuf` `Docker`

**[travel-itinerary-validation-api](https://github.com/rkkims/travel-itinerary-validation-api)**: validation and correction service
> FastAPI service that parses free-text itineraries, resolves stops against place APIs, and checks them against a rule set for closed locations, overlapping stops, infeasible travel times, and duplicates.
> 
> `Python` `FastAPI` `SQLAlchemy` `pytest`

**[JipBap](https://jipbap.com)**: Asian recipe recommendation web app based on what you have in your pantry. Features a unique Asian ingredient ontology.
>
> `TypeScript`, `HTML`


---

### 🧰 Stack

**Languages** Python · SQL · JavaScript/TypeScript · Bash · R
**Spatial** PostGIS · GeoJSON · WFS · ArcGIS REST · geocoding · spatial indexing
**Data** PostgreSQL · SQLAlchemy · psycopg2 · schema migrations · entity resolution
**Pipelines** incremental sync · watermarking · change detection · idempotent upserts · Nextflow
**Serving** FastAPI · REST API design · Pydantic
**Infra** Docker · GCP · GitHub Actions · Sentry · Linux

---

### 🔬 Earlier work: research data pipelines

Six years as a research software engineer in genomics, building and maintaining Nextflow
pipelines for genome assembly, metagenomic classification, and consensus generation from
long- and short-read sequencing data
([VSAT](https://github.com/rkkims/VSAT),
[BunyaFinder](https://github.com/rkkims/BunyaFinder),
[Snakehead](https://github.com/rkkims/Snakehead),
[KU-ONT-SEOV-consensus](https://github.com/rkkims/KU-ONT-SEOV-consensus)).

---

### 📫 Reach me

[Email](mailto:richard.k.kim.work@gmail.com) · open to data engineering work
