# Richard Kim

**Python developer working across data pipelines, data analysis, and AI evaluation.**

I build data pipelines, analyze messy real-world data, and review code: my own, other people's, and code written by models. Over the past year I have worked in AI training, evaluating code patches and agent behaviour against written rubrics. Before that, I spent six years building analysis pipelines in genomics research labs.

I am open to AI evaluation, data, and software roles, as well as contract work.

---

### 🧪 What I do

**AI evaluation and code review.** I annotate code patches from large public repositories (NumPy, React, Numba) against their issue descriptions. I also judge virtual-agent interactions against performance rubrics. In my own projects, I score LLM output against labelled datasets instead of checking demo outputs by eye.

**Data analysis and visualization.** I take raw, inconsistent data through inspection, normalization, and QA to results someone can act on, and I document what the data cannot support. I work in Python (pandas/GeoPandas, Jupyter), R (ComplexHeatmap, phyloseq), and SQL.

**Data pipelines.** I built unattended ingestion from 38 public sources into one PostgreSQL/PostGIS schema, with incremental sync and data-quality checks. I also wrote reproducible Nextflow workflows for research data.

---

### 🏗️ Selected work

**[travel-itinerary-validation-api](https://github.com/rkkims/travel-itinerary-validation-api)**: a correction layer for AI-generated output
> FastAPI service that catches and repairs LLM-generated itineraries that read fluently but are impossible: closed venues, infeasible travel times, overlaps, duplicates. The validator is scored against a labelled dataset, and fuzz and latency checks are included.
>
> `Python` `FastAPI` `pytest` `LLM evaluation`

**[municipal-streetlight-network](https://github.com/rkkims/municipal-streetlight-network)**: reproducible data analysis
> Public infrastructure data from two municipalities goes through acquisition, inspection, normalization driven by YAML mappings, QA, network tracing, and map exhibits. It includes an honest record of the data's limitations.
>
> `Python` `GeoPandas` `NetworkX` `Jupyter`

**[canpermits-platform](https://github.com/rkkims/canpermits-platform)**: multi-source ingestion platform
> Ingests 38 sources into one PostgreSQL schema, unattended daily. Features incremental sync with change detection, spatial resolution, and PII gating. This repository is a curated extract of a production system that was retired in August 2026.
>
> `Python` `PostgreSQL` `PostGIS` `FastAPI` `Docker` `GCP`

**[VirPipe](https://github.com/rkkims/VirPipe)**: published research pipeline
> A configurable pipeline for virus detection in sequencing data. First-author paper in *Bioinformatics* (2023).
>
> `Python` `Nextflow`

---

### 🧰 Stack

**Languages** Python · SQL · JavaScript/TypeScript · R · Bash  
**Data** pandas · GeoPandas · Jupyter · PostgreSQL/PostGIS · SQLite  
**Formats** JSON · YAML · XML · HTML · Markdown · GeoJSON  
**Engineering** FastAPI · pytest · Docker · GitHub Actions · Linux · Nextflow  
**AI tooling** LLM APIs · code agents (Claude Code) · rubric-based evaluation

---

### 🔬 Earlier work: research data pipelines

I worked six years in genomics research labs, building Nextflow and Python pipelines for assembly, classification, and consensus generation. See [VSAT](https://github.com/rkkims/VSAT), [BunyaFinder](https://github.com/rkkims/BunyaFinder), [Snakehead](https://github.com/rkkims/Snakehead), [metagenome_heatmap](https://github.com/rkkims/metagenome_heatmap), and [KU-ONT-SEOV-consensus](https://github.com/rkkims/KU-ONT-SEOV-consensus).

---

### 📫 Reach me

[Email](mailto:richard.k.kim.work@gmail.com) · open to AI evaluation, data, and software work
