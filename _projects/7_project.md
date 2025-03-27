---
layout: page
title: Thyroid Follow-Up Study
description: Thyroid Nodule Progression Analysis Using IBM MarketScan and Azure Databricks.
img: assets/img/z7.png
importance: 1
category: Healthcare
related_publications: true
---
<!-- ### **Case Study: AI-Driven Rare Disease Research Collaborative Network** -->

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/z7.png" title="AI-Driven Rare Disease Research Collaborative Network" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
    Scalable claims-based analysis of thyroid nodule diagnosis, treatment trends, and healthcare costs using longitudinal modeling and statistical methods.
</div>

---
# 1. Introduction

Thyroid nodules are a prevalent condition, with many cases requiring careful monitoring and potential surgical intervention. Understanding their progression and the associated treatment patterns is critical for informed clinical decisions. This project analyzes real-world data from IBM MarketScan to uncover insights into thyroid nodule management over time, including population-level trends, comorbidities, and follow-up behaviors. The study leverages distributed computing on Azure Databricks and PySpark to handle and analyze this large-scale claims data efficiently.

# 2. Key Questions Addressed

- How do benign and malignant thyroid nodules differ in progression, treatment, and cost?
- What follow-up patterns emerge over 5 and 10 years for benign cases?
- What are the most common procedures and their distribution over time?
- How does insurance type or demographic profile affect treatment decisions?
- What comorbidities commonly occur in patients with thyroid nodules?

# 3. The Problem: Limitations in Claims-Based Thyroid Research

- **Data Volume**: MarketScan data contains millions of inpatient and outpatient claims, requiring efficient distributed filtering and transformation.
- **Sparse Progression Labels**: Disease progression must be inferred from changes in diagnosis and procedure codes over time.
- **Procedure Duplication**: Temporal proximity and redundant claims needed to be resolved via customized deduplication algorithms.
- **Incomplete Coverage**: MarketScan does not include Medicare, Medicaid, or uninsured populations, necessitating adjustments using external population data.
- **Insurance Impact**: Assessing how insurance type affects care delivery remains a critical equity-focused angle.

# 4. The Importance: Enabling Data-Driven Decision-Making

- **Improved Risk Stratification**: By identifying patterns in benign-to-malignant transitions (~9.26% observed), clinicians can better manage follow-up intensity.
- **Surgical Trends**: Insights into procedure timing (e.g., lobectomy, thyroidectomy) support better planning and intervention strategies.
- **Cost Transparency**: Coinsurance, copayment, and deductible data help visualize financial burdens and payer impact.
- **Policy Implications**: Findings offer evidence for insurance-related disparities and resource allocation.

# 5. The Solution: Longitudinal Modeling with PySpark and Databricks

## 5.1 Data Preprocessing & Integration

- Filtered 394,632 patients with thyroid nodules from 100M+ records using diagnosis and procedure codes.
- Addressed data inconsistencies, null values, and redundant claims using PySpark transformations.
- Adjusted for populations not covered by MarketScan using publicly available uninsured/Medicare/Medicaid statistics.

## 5.2 Feature Engineering & EDA

- Defined diagnosis progression labels: benign, malignant, benign-to-malignant.
- Computed follow-up duration, procedure timelines, surgery intervals, and patient demographics.
- Segmentations based on age, sex, insurance plan, and region.

## 5.3 Longitudinal and Predictive Modeling

- Gantt charts and stratified survival analysis for benign cases with 5 and 10 years of follow-up.
- Time-to-surgery intervals modeled from first diagnosis.
- Custom classification of surgery type (lobectomy vs. total thyroidectomy) and cost pre- and post-surgery.

## 5.4 Comorbidity and Procedure Analysis

- Tracked coexisting conditions: diabetes, hypertension, hyperlipidemia, sleep apnea, heart disease, RA, pulmonary disorders.
- Frequency distributions and cost analysis of key procedures: ultrasound, FNA, thyroidectomy variants, calcitonin tests.

## 5.5 Visualization and Reporting

Constructed dashboards and figures summarizing:

- Procedure distributions
- Progression outcomes
- Insurance plan and demographic breakdowns
- Gantt timelines for follow-up and surgery

# 6. Results and Outcomes

| Metric                          | Value        |
|--------------------------------|--------------|
| Total Patients with Thyroid Nodules | 394,632     |
| Benign Cases (≥5 years)        | 7,320        |
| Benign Cases (≥10 years)       | 3,241        |
| Benign to Malignant Progression | ~9.26%      |
| Mean Follow-up (Benign)        | 4.87 years   |
| Top Procedures                 | Ultrasound, FNA, Thyroidectomy |
| Comorbidity Tracking           | 8+ conditions segmented by sex and age |

# 7. Conclusion

This project provides a scalable and reproducible pipeline for analyzing thyroid nodule progression using real-world claims data. Through rigorous preprocessing, longitudinal modeling, and cost analysis, it enables clinical, financial, and policy insights from large, complex datasets. The use of Azure Databricks and PySpark allows for efficient computation, making it applicable to other high-volume healthcare analytics tasks.

# 8. Skills and Tools Used

- **Distributed Processing**: Azure Databricks, PySpark  
- **Statistical Modeling**: Time-series, survival analysis  
- **Data Wrangling**: Pandas, NumPy  
- **Visualization**: Matplotlib, Plotly, Seaborn  
- **Healthcare Data**: IBM MarketScan  
- **Insurance Estimation**: National policy statistics, data fusion techniques  
- **Procedural Deduplication**: Custom temporal sequence matching algorithms  

# 9. Future Directions

- Expand to Other Diagnoses: Include autoimmune and thyroid-related metabolic disorders.
- Geographic Variation: Map treatment patterns across US regions.
- Link with External Datasets: Add EHR or cancer registry data for richer outcomes.
- Procedure Pathway Optimization: Suggest optimal follow-up pathways based on historical outcomes.
- Equity Analysis: Deeper exploration of disparities across insurance types and socioeconomic factors.
