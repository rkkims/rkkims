# Richard Kim

**Data engineer specializing in geospatial and public-sector data.**

I build ingestion systems for sources that do not cooperate: government open-data
portals, GIS endpoints, and records that arrive as monthly PDF reports. The kind where
every upstream fails differently and the schema changes without telling you.

Most recently I designed and ran a platform that ingested municipal open data from
**38 Canadian cities and provincial agencies** into one PostgreSQL schema on an
unattended daily schedule. Before that, six years building genomics data pipelines in
research labs: high-volume batch processing, DAG orchestration, reproducibility as a
hard requirement. Different domain, same discipline.

Working remote and async. Open to data engineering roles and contract work.

---

### 🗺️ What I specialize in

**Geospatial data engineering.** PostGIS at production depth: 105 GIST spatial indexes,
point-in-polygon resolution across millions of records, geocoding pipelines, geometry
validation, and polygon-layer ingestion from GeoJSON and WFS sources with checksum
manifests, so a silently changed boundary file gets caught rather than quietly reshaping
the data.

**Public-sector and civic data.** 38 municipal and provincial sources across seven
provinces: Socrata, ArcGIS REST, CKAN, Opendatasoft, WFS, CSV drops, and eight
municipalities that publish only as PDF reports. Open-data licence compliance and PII
handling included, because public records and public-domain records are not the same
thing.

**Hard-target data acquisition.** Undocumented APIs, protobuf request construction,
bot-detection handling, and document extraction where no structured feed exists at all.

---

### 🏗️ Selected work

**[canpermits-platform](https://github.com/rkkims/canpermits-platform)**: municipal open-data ingestion platform
> 38 sources into a 275-table PostgreSQL schema, unattended daily. 151 pipelines over 145
> source adapters. Incremental sync with a 14-day amendment overlap, fail-open upstream
> change detection, spatial resolution against municipal boundary layers, asymmetric PII
> gating, and an entity-resolution benchmark I shipped as a **NO-GO** after measuring my
> own roadmap assumption to be 65x wrong. Curated extract of a production system,
> 4,169 commits, retired August 2026.
>
> `Python` `PostgreSQL` `PostGIS` `FastAPI` `Docker` `GCP`

**[googleflight-scraper](https://github.com/rkkims/googleflight-scraper)**: extraction from an undocumented source
> Google Flights encodes search state as base64-wrapped protobuf and returns
> positionally-indexed arrays. No schema, and both sides change without notice. Requests
> compile from `.proto` definitions rather than string-templated URLs, and parsers are
> unit-tested against captured response fixtures, so an upstream shape change fails in CI
> instead of silently in production.
>
> `JavaScript` `protobuf` `Docker` `GitHub Actions`

**[travel-itinerary-validation-api](https://github.com/rkkims/travel-itinerary-validation-api)**: validation and correction service
> FastAPI service that parses free-text itineraries, resolves stops against place APIs,
> checks them against a rule set (closed, overlapping, infeasible travel time, duplicate),
> then applies a push-forward correction cascade. Scored against a labelled dataset rather
> than eyeballed.
>
> `Python` `FastAPI` `SQLAlchemy` `pytest`

**[VirPipe](https://github.com/rkkims/VirPipe)**: composable pipeline framework
> Lets researchers compose and deploy custom detection pipelines over high-throughput
> sequencing data without rewriting orchestration each time.
>
> `Python` `Nextflow`

---

### 🧰 Stack

**Languages** Python · SQL · JavaScript/TypeScript · Bash · R
**Spatial** PostGIS · GeoJSON · WFS · ArcGIS REST · geocoding · spatial indexing
**Data** PostgreSQL · SQLAlchemy · psycopg2 · schema migrations · entity resolution
**Pipelines** incremental sync · watermarking · change detection · idempotent upserts · Nextflow
**Serving** FastAPI · REST API design · Pydantic
**Infra** Docker · GCP · GitHub Actions · Sentry · Linux
**Practice** data-quality monitoring · freshness SLOs · adjudicated benchmarks · pytest

---

### 📌 Things I care about

- **Idempotent by default.** Re-running a pipeline should be free and safe. That
  assumption is what makes overlap windows, backfills, and replays cheap.
- **Fail open on uncertainty.** Every ambiguous path in a skip decision should take the
  expensive branch. A false skip costs correctness; a false fetch costs seconds.
- **Measure before you scope.** I have killed my own feature with a 57-case adjudicated
  sample. Days of measurement beat months building on a wrong denominator.
- **Write the reason, not the value.** A tuning constant without its incident recorded
  beside it is a constant nobody can safely change later.

---

### 🔬 Earlier work: research data pipelines

Six years as a research software engineer in genomics, building and maintaining Nextflow
pipelines for genome assembly, metagenomic classification, and consensus generation from
long- and short-read sequencing data
([VSAT](https://github.com/rkkims/VSAT),
[BunyaFinder](https://github.com/rkkims/BunyaFinder),
[Snakehead](https://github.com/rkkims/Snakehead),
[KU-ONT-SEOV-consensus](https://github.com/rkkims/KU-ONT-SEOV-consensus)).

These were data engineering problems with a different noun in front of them: unreliable
instrument output, long-running batch DAGs, schema drift between tool versions, and
pipelines other people had to run without me in the room.

---

### 📫 Reach me

[Email](mailto:richard.k.kim.work@gmail.com) · open to remote and async data engineering work
