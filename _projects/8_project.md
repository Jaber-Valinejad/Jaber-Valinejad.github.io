---
layout: page
title: EMS Response
description: Data-Driven Insights into EMS Response and Outcomes using NEMSIS (2017–2021).
img: assets/img/z8.jpg
importance: 2
category: Healthcare Data Science
giscus_comments: true
---
<!-- ### **Case Study: Fatal and Non-Fatal Opioid Overdose Analysis** -->

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/z8.png" title="Fatal and Non-Fatal Opioid Overdose Analysis" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
    The comprehensive, data-driven analysis of opioid overdose incidents across the U.S. using NEMSIS data (2017–2021), uncovering disparities in EMS response times, naloxone administration, and fatality risk through advanced statistical modeling and cloud-based processing.
</div>

---
# 1. Introduction

Opioid overdose continues to be a critical public health crisis in the United States. Timely and appropriate EMS intervention—particularly naloxone administration—can be lifesaving. This project leverages the National EMS Information System (NEMSIS) dataset to analyze fatal and non-fatal opioid overdose incidents across the U.S. from 2017 to 2021. Through advanced data engineering, statistical modeling, and cloud-based processing, the study examines disparities in response time and outcomes based on drug type, geography, race, and healthcare access.

# 2. Key Questions Addressed

- How does EMS response time vary by race, region, and urbanicity?
- What factors are significantly associated with overdose fatality?
- Is naloxone administration equitable across demographics and regions?
- How do drug types and combinations influence overdose outcomes?
- What patterns emerge from urban vs. rural comparisons in overdose cases?

# 3. The Problem

**Key challenges in overdose analysis:**

- Massive and complex datasets: NEMSIS is a high-dimensional database with millions of records per year.
- Inconsistent data across states: Not all states report the same variables or maintain consistent quality.
- Missing and incomplete bystander data: A substantial portion of records lack information about CPR, AED use, or witness reports.
- Non-uniform case definitions for overdose and fatality: Requires carefully curated logic to define cases.

# 4. The Importance

By understanding EMS response patterns and overdose risk factors:

- Policymakers can target resource allocation.
- EMS agencies can evaluate operational performance.
- Researchers can explore health disparities.
- Communities can benefit from earlier interventions and better care strategies.

# 5. The Solution

A scalable, cloud-based data pipeline and analysis framework built with SQL and AWS.

## 5.1 Data Collection & Preparation

- Downloaded and preprocessed NEMSIS datasets (2017–2021) on AWS EC2.
- Combined and normalized critical variables: primary/secondary impression, symptoms, medications, and outcomes.
- Defined fatal vs. non-fatal overdose using a multi-step logic aligned with CDC guidelines.

## 5.2 Cohort Definition

Created four main cohorts based on medication timing and location:

- **Rural | Medication before EMS arrival**
- **Rural | Medication after EMS arrival**
- **Urban | Medication before EMS arrival**
- **Urban | Medication after EMS arrival**

## 5.3 Feature Engineering & Case Definitions

- Used ICD-10 codes (F11, T40) and NEMSIS variables to flag opioid-related cases.
- Stratified by race, region, hour of day, service level, and care type.
- Engineered response time from EMS dispatch to scene arrival.

## 5.4 Statistical Analysis & Modeling

- Applied logistic regression to evaluate predictors of fatality.
- Assessed multicollinearity using Variance Inflation Factor (VIF).
- Ran 44 stratified regression models to test effects of various drug types and demographics.

# 6. Results and Outcomes

- **Disparity Insights:** Native Hawaiians had the shortest response times; Whites had the longest.
- **Fatality Risk:** Higher among elderly, uninsured, and certain race-location combinations.
- **Naloxone Administration:** Less likely in rural areas; overall probability varied by race.
- **Response Time:** Urban areas had faster response, but not always better outcomes.
- **Regression Results:** Identified significant predictors of death, including service level, drug type, and region.

# 7. Conclusion

This project provides a data-driven view into EMS performance and opioid overdose outcomes in the U.S. Through rigorous preprocessing, cloud computing, and advanced analytics, it highlights disparities and system-level gaps that can inform future interventions and policy.

# 8. Skills and Tools Used

- **Cloud Computing:** AWS EC2
- **Data Management:** SQL, Pandas
- **Statistical Modeling:** Logistic Regression, VIF, Feature Selection
- **Visualization:** Matplotlib, Seaborn
- **Data Source:** National EMS Information System (NEMSIS)

# 9. Future Directions

- Add ML classifiers (Random Forest, XGBoost) to predict fatal outcomes
- Integrate social determinants of health (SDOH) and insurance types
- Build a public-facing dashboard for real-time overdose monitoring
- Explore intervention strategies using counterfactual modeling
- Collaborate with EMS agencies for field validation of model insights
