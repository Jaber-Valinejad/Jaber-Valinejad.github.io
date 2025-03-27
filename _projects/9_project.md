---
layout: page
title: Target Deconvolution 
description: Generative AI-enhanced biomedical discovery using LLM fine-tuning, and phenotypic screening.
img: assets/img/z9.jpg
importance: 4
category: [ Generative AI, Natural Language Processing, Healthcare]
---

<!-- ### **Case Study: Target Identification and Drug Discovery for Rare Diseases** -->

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/z9.png" title="Target Identification and Drug Discovery for Rare Diseases" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
    Target Identification and Drug Discovery for Rare Diseases.
</div>

---

# 1. Introduction

Rare diseases face unique challenges in drug discovery due to limited datasets and insufficient therapeutic research. This project presents an end-to-end AI-driven drug discovery pipeline, combining generative models, high-throughput compound screening, and target deconvolution for diseases such as DYT1 dystonia. It further leverages cloud computing (AWS EC2 and S3) for scalable training and storage of large biomedical models and data.

# 2. Key Questions Addressed

- How can LLMs be fine-tuned for rare disease biomedical reasoning?
- How can AWS infrastructure support scalable model training and deployment?
- What techniques best link phenotypic screening hits to molecular targets?
- How can literature and structured data be combined to validate rare disease associations?

# 3. The Problem

Drug discovery for rare diseases is hindered by:

- Sparse annotations and high-dimensional biological space.
- Computational cost of large-scale phenotypic screening analysis.
- Low interpretability of chemical similarity scores.
- Lack of cloud-native infrastructure in many bioinformatics workflows.

# 4. The Importance

This project brings together LLM fine-tuning, semantic biomedical reasoning, and cloud computing to create a scalable system that:

- Extracts gene-phenotype-disease associations using a fine-tuned LLM.
- Scales compute resources via AWS EC2, enabling high-throughput model training and inference.
- Stores and retrieves large biological datasets using S3 buckets, supporting reproducibility and collaboration.
- Supports hypothesis generation through semantically grounded biological insights.

# 5. The Solution

## 5.1 Cloud Infrastructure (AWS)

- **Amazon EC2**: Utilized GPU-backed EC2 instances to fine-tune TinyLlama-1.1B using SFT + LoRA. EC2 provided scalable, on-demand compute for model training, inference, and evaluation.
- **Amazon S3**: Managed large datasets (PubChem, CTD, gene annotations, fine-tuning CSVs) in S3 buckets, allowing efficient storage and access from both notebooks and EC2.
- **Data Pipeline**: Synced model checkpoints and experiment logs (e.g., via WandB) to S3 for versioning and downstream analysis.

## 5.2 Fine-Tuned LLM for Rare Disease Reasoning

- **Model**: TinyLlama-1.1B, trained on 66,000+ biomedical triples.
- **Techniques**: Supervised Fine-Tuning (SFT) + LoRA (r=64, alpha=16, dropout=0.1)
- **Evaluation**: Benchmarked with lighteval on biomedical MMLU tasks (Anatomy, Biology, Medicine).

**Prompt Example**:
```text
<s>[INST] Which phenotypes and genes are associated with cystic fibrosis? [/INST]
```

## 6. Target Deconvolution and Association Validation

Combining semantic search, chemical similarity, and pathway analysis, this pipeline includes:

- **SwissTargetPrediction/SuperPRED** gene predictions  
- **CTD/ChEMBL**-based similar compound mining  
- **Pathway enrichment** via **ShinyGO**  
- **CID-to-CTD mapping** using **PubChem APIs**  
- **Literature mining** with **Neo4j/RDAS**

## 7. Results and Outcomes

- **LLM Accuracy**: Fine-tuned model achieved **0.73+ mean token accuracy** on biomedical prompts.  
- **Predicted Targets**: Genes like **ACHE**, **SLC2A1**, **CDC25C**, **LYN** enriched across tools and datasets.  
- **Cloud Efficiency**: Training that would typically take days was reduced using **EC2 autoscaling** with on-demand GPU instances.  
- **Storage Optimization**: Datasets and intermediate results were version-controlled and archived using **S3 buckets**.

## 8. Skills and Tools Used

### 🧠 Generative AI & NLP

- HuggingFace Transformers, PEFT (LoRA), TRL (SFTTrainer)  
- Instruction tuning, ChatML format, semantic prompting  
- Evaluation: LightEval, WandB, MMLU subsets

### ☁️ Cloud Computing

- AWS EC2: GPU-based training of LLMs  
- AWS S3: Dataset and checkpoint management  
- Serverless logging and remote monitoring via WandB + S3

### 🔬 Bioinformatics & Data Science

- SwissTargetPrediction, SuperPRED, CTD, OMIM, HPO  
- Neo4j, RDAS, Pandas, PubChem APIs  
- ShinyGO, enrichment metrics (FDR, Fold Enrichment)

## 9. Future Directions

- Deploy the LLM as an API-backed microservice using **AWS Lambda + EC2**  
- Expand multi-modal training (e.g., EHR + genomic embeddings)  
- Add few-shot prompt tuning and instruction chaining for compound generation tasks  
- Enable batch inference pipelines for large compound libraries via **EC2 autoscaling**
