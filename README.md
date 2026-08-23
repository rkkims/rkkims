# Richard Kim

**Data engineer.** I build ingestion systems for messy, heterogeneous, real-world
sources — the kind where every upstream fails differently and the schema changes
without telling you.

Most recently I designed and ran a platform that ingested municipal open data from
**38 Canadian cities and provincial agencies** into one Postgres schema on an
unattended daily schedule. Before that, six years building genomics data pipelines in
research labs — high-volume batch processing, DAG orchestration, reproducibility as a
hard requirement. Different domain, same discipline.

Working remote and async. Open to data engineering roles.

---

### 🏗️ Selected work

**[canpermits-platform](https://github.com/rkkims/canpermits-platform)** — municipal open-data ingestion platform
> 38 sources → 275-table Postgres schema, unattended daily. 151 pipelines over 145
> source adapters (Socrata, ArcGIS, WFS, CKAN, CSV drops, and monthly PDFs parsed
> with `pdfplumber`). Incremental sync with a 14-day amendment overlap, fail-open
> upstream change detection, asymmetric PII gating, and an entity-resolution
> benchmark I shipped as a **NO-GO** after measuring my own roadmap assumption to be
> 65× wrong. Curated extract of a production system — 4,169 commits, retired Aug 2026.
>
> `Python` `PostgreSQL` `PostGIS` `FastAPI` `Docker` `cron` `GCP`

**[travel-itinerary-validation-api](https://github.com/rkkims/travel-itinerary-validation-api)** — validation & correction service
> FastAPI service that parses free-text itineraries, resolves stops against place
> APIs, checks them against a rule set (closed / overlap / infeasible travel time /
> duplicate), and applies a push-forward correction cascade. Clean service-layer
> separation with an eval harness scored against a labelled dataset.
>
> `Python` `FastAPI` `SQLAlchemy` `pytest`

**[googleflight-scraper](https://github.com/rkkims/googleflight-scraper)** — resilient extraction from an undocumented source
> Google Flights encodes search state as base64-wrapped protobuf and returns
> positionally-indexed arrays — no schema, both sides change without notice. Requests
> are compiled from `.proto` definitions rather than string-templated; parsers are
> unit-tested against **captured response fixtures**, so an upstream shape change fails
> in CI instead of silently in production. A scheduled job rolls fixture dates forward
> so the suite never expires.
>
> `JavaScript` `protobuf` `Docker` `GitHub Actions` `Apify`

**[VirPipe](https://github.com/rkkims/VirPipe)** — configurable bioinformatics pipeline framework
> Lets researchers compose and deploy custom virus-detection pipelines over
> high-throughput sequencing data without rewriting orchestration each time.
>
> `Python` `Nextflow`

---

### 🧰 Stack

**Languages** Python · SQL · JavaScript/TypeScript · Bash · R
**Data** PostgreSQL · PostGIS · SQLAlchemy · psycopg2 · pandas · SQLite
**Pipelines** Nextflow · cron orchestration · incremental sync & watermarking · CDC-style change detection · entity resolution
**Serving** FastAPI · REST API design · Pydantic
**Infra** Docker · GCP · GitHub Actions · Sentry · Linux
**Practice** schema migrations · data-quality monitoring · freshness SLOs · adjudicated benchmarks · pytest

---

### 📌 Things I care about

- **Idempotent by default.** Re-running a pipeline should be free and safe. That
  assumption is what makes overlap windows, backfills, and replays cheap.
- **Fail open on uncertainty.** Every ambiguous path in a skip/short-circuit decision
  should take the expensive branch. A false skip costs correctness; a false fetch
  costs seconds.
- **Measure before you scope.** I've killed my own feature with a 57-case adjudicated
  sample. Days of measurement beat months building on a wrong denominator.
- **Write the reason, not the value.** A tuning constant without its incident recorded
  beside it is a constant nobody can safely change later.

---

### 🔬 Earlier work — research data pipelines

Six years as a research software engineer in genomics, building and maintaining
Nextflow pipelines for genome assembly, metagenomic classification, and consensus
generation from long- and short-read sequencing data
([VSAT](https://github.com/rkkims/VSAT),
[BunyaFinder](https://github.com/rkkims/BunyaFinder),
[Snakehead](https://github.com/rkkims/Snakehead),
[KU-ONT-SEOV-consensus](https://github.com/rkkims/KU-ONT-SEOV-consensus)).
These were data engineering problems with a different noun in front of them:
unreliable instrument output, long-running batch DAGs, schema drift between tool
versions, and pipelines other people had to run without me in the room.

---

### 📫 Reach me

[Email](mailto:richard.k.kim.work@gmail.com) · open to remote / async data engineering roles
