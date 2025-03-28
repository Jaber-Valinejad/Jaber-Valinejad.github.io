---
layout: page
title: Adverse Drug Event 
description: ETL-Driven Knowledge Graph Construction for Improving Drug Safety and Pharmacovigilance in Rare Diseases
img: assets/img/z4.png
importance: 1
category: [Extract Transform Load (ETL) , Healthcare Data Science]
related_publications: true
---

<!-- ### **Case Study: ADE4RD: Adverse Drug Events for Rare Diseases** -->

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/z4.png" title="ADE4RD: Adverse Drug Events for Rare Diseases" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
    The scalable ETL and knowledge graph framework that transforms FDA adverse event data into structured insights for improving drug safety analysis in rare diseases..
</div>

---

# 1. Introduction

Rare diseases affect fewer than 200,000 individuals in the U.S., with many conditions impacting only a few dozen patients. Despite over 1,200 FDA-approved orphan drugs, adverse drug events (ADEs) related to these treatments remain poorly understood due to underreporting, rare occurrence, and unstructured data. Traditional pharmacovigilance methods are insufficient to analyze the safety of orphan drugs at scale.

**ADE4RD** introduces an end-to-end ETL pipeline and knowledge graph framework to systematically ingest, transform, and model adverse event data for rare diseases using the FDA Adverse Event Reporting System (FAERS). The project leverages NIH STRIDES computing infrastructure and parallel processing to enable scalable analysis, with results integrated into a Neo4j graph database for querying and visualization.

---

# 2. Key Questions Addressed

- How can ETL pipelines be designed to extract, transform, and normalize large-scale ADE data for rare diseases?
- How can FAERS be integrated with GARD and FDA orphan drug approval datasets at scale?
- What methods support efficient graph modeling and querying for drug-disease-event associations?
- How can parallel processing accelerate the construction of biomedical knowledge graphs?
- How can STRIDES infrastructure support reproducible and scalable data engineering workflows?

---

# 3. The Problem

Building an ADE pipeline for rare diseases presents key challenges:

- **Data Complexity**: FAERS data is unstructured, high-volume, and spread across multiple sources with differing schemas.
- **Mapping Rare Diseases to Drugs**: Requires harmonizing orphan drug designations with disease names from GARD using string and fuzzy matching.
- **Scalability**: Millions of records from FAERS must be processed efficiently for downstream analytics.
- **Integration and Querying**: ADEs, drug properties, and clinical metadata must be represented semantically for intuitive querying and analysis.

---

# 4. The Importance

By engineering a scalable ETL framework, ADE4RD delivers:

- **Data Harmonization at Scale**: Aligns FDA orphan drug designations, GARD diseases, and ADEs in a unified graph schema.
- **Graph-Based Semantics**: Enables intuitive and relational querying using Cypher over a Neo4j knowledge graph.
- **Improved Pharmacovigilance**: Empowers analysts to identify high-risk drugs, serious ADEs, and patterns of safety concern.
- **Reusable ETL Infrastructure**: Supports extension to other biomedical datasets and use cases.
- **Cloud-Based Deployment**: Leverages NIH STRIDES infrastructure for cloud-scale ingestion, transformation, and processing.

---

# 5. The Solution

## 5.1 ETL Architecture

- **Extraction**: Utilized OpenFDA APIs and FAERS public dashboard datasets to collect data on drug events, labeling, NDC codes, and recalls.
- **Transformation**: Normalized multi-source data into structured entities (e.g., drug, patient, ADE, disease) using Pandas, regular expressions, and string mapping.
- **Parallel Processing**: Used Python multiprocessing for scalable ingestion and mapping tasks, reducing runtime across millions of records.
- **Loading**: Mapped processed data into a Neo4j graph via batch CSV imports and Py2Neo Cypher scripting.

## 5.2 Data Mapping

- **Rare Disease Linkage**: Mapped FDA orphan drug approvals to GARD rare diseases using labeled indications and designations via exact and fuzzy matching.
- **Relationship Modeling**: Defined 10 primary node classes and 9 relationship types, including `HAS_ADVERSE_EFFECT`, `TREATED_WITH`, and `RECALL_ASSOCIATION`.

## 5.3 Infrastructure

- **Cloud Deployment**: Deployed parallelized pipelines on NIH STRIDES cloud platform to process large datasets efficiently.
- **Dockerized Setup**: Built a Docker container with Neo4j and supporting tools for reproducible local development and deployment.

---

# 6. Results and Outcomes

- **Graph Stats**: 17,833 nodes and 19,617 edges across patients, drugs, ADEs, recalls, and rare diseases {% cite jab10822513 %}.
- **Case Study 1**: In 2019, 6,375 ADEs were reported across 195 rare diseases, with over 3,200 classified as serious.
- **Case Study 2**: Identified top 10 orphan drugs associated with highest ADEs (e.g., ADALIMUMAB, APREMILAST), including fatal events.
- **Graph Querying**: Used Cypher to identify event frequency, recall counts, and patient-level reactions.

---

# 7. Conclusion

ADE4RD demonstrates the power of ETL-based knowledge graph engineering for pharmacovigilance in rare diseases. By transforming FAERS data into structured relationships between drugs, ADEs, and diseases, the project provides a scalable framework for safety analysis, research, and data-driven decision making. The combination of cloud infrastructure, graph modeling, and scalable ETL pipelines makes this approach highly extensible to other biomedical applications.

---

# 8. Skills and Tools Used

### 💻 Programming & Scripting

- Python (Pandas, NumPy, Py2Neo, Regex, Multiprocessing)
- Cypher Query Language
- Shell scripting & Docker

### 📊 Data Engineering

- ETL pipeline design and orchestration
- Parallel processing for high-volume biomedical data
- Semantic data modeling
- Graph schema design

### 🧠 Graph Database

- Neo4j with Docker integration
- Knowledge graph construction and querying

### ☁️ Infrastructure

- NIH STRIDES cloud environment
- Containerized reproducible workflows

### 📚 Data Sources

- FAERS (OpenFDA APIs)
- GARD (Genetic and Rare Diseases)
- FDA Orphan Drug Designations and Approvals

---

# 9. Future Directions

- **LLM-Enhanced Validation**: Use GPT/BioMedLM to validate or enrich ADE reports with literature evidence.
- **Clinical Trial and EHR Integration**: Incorporate real-world evidence from STRIDES and PubMed.
- **Automated Matching**: Apply fuzzy string matching and BERT-based entity linking for robust mapping.
- **Global Expansion**: Extend system to include EMA and international pharmacovigilance data.
- **Interactive Dashboards**: Build user-friendly front-ends for clinicians and researchers.
