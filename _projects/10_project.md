---
layout: page
title: Media Resilience
description: Leveraged large-scale Twitter data, machine learning, and NLP techniques to quantify and compare social–psychological resilience across five countries.
img: assets/img/z10.png
importance: 1
category: [Natural Language Processing]
related_publications: true
---



<!-- ### **Case Study: AI-Driven Rare Disease Research Collaborative Network** -->

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/z10.png" title="AI-Driven Rare Disease Research Collaborative Network" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
    Social Media-Based Analysis of Community Resilience Using NLP and Machine Learning During COVID-19.
</div>

---

# Project Overview

This project introduces a scalable, data-driven framework for measuring **Social–Psychological Community Resilience (SPCR)** using Twitter data collected during the COVID-19 pandemic {% cite valinejad2021measuring %}. By applying advanced natural language processing (NLP) and machine learning (ML) techniques, we assessed public sentiment, misinformation impact, and resilience patterns across five countries: Australia, Singapore, South Korea, the United Kingdom, and the United States {% cite valinejad2022measuring % }.

---


## Key Contributions

- Developed an end-to-end NLP pipeline to analyze over 210,000 tweets, annotated and classified as real or fake.
- Proposed and computed a novel metric, **SPCR**, using linguistic features extracted from tweets to quantify community wellbeing and social capital.
- Applied machine learning classifiers (Passive-Aggressive, Decision Tree, AdaBoost) to detect misinformation with >99.5% accuracy.
- Demonstrated the impact of accurate vs. fake information on public sentiment and resilience.
- Generated cross-country resilience profiles and temporal trend analyses using statistical modeling {% cite guo2022effect %}.

---

## Data Science & NLP Techniques

### Data Collection & Preprocessing

- Collected 50,000 tweets per country using the Twitter API, filtered by COVID-related keywords and timeline (Mar–Nov 2020).
- Preprocessing pipeline included tokenization, stopword removal, stemming, and lemmatization using **NLTK**, **WordNetLemmatizer**, and **PorterStemmer**.

### Fake Tweet Classification

- Implemented and evaluated multiple ML classifiers using **Scikit-learn**, achieving high accuracy in detecting misinformation.
- Features included **TF-IDF** vectors and text-based sentiment cues.

### Psychological Feature Extraction

- Used **LIWC (Linguistic Inquiry and Word Count)** to derive psychological and social indicators (e.g., anxiety, social cohesion, pronoun usage).
- Quantified **Community Wellbeing (CW)** and **Community Capital (CC)** for each tweet.

### SPCR Metric & Trend Analysis

- Computed **SPCR** as a composite score of CW and CC.
- Applied polynomial regression and Gaussian fitting to model SPCR dynamics over time.
- Conducted correlation analysis (**Pearson**, **Spearman**) between misinformation prevalence and SPCR.

---

## Results & Insights

- **South Korea** demonstrated the highest SPCR, highlighting the impact of effective governance and social cohesion {%cite valinejad2023social %}.
- Real tweets contributed to significantly higher SPCR scores (up to **80% improvement** vs. fake tweets).
- Country-specific patterns revealed cultural and policy-driven differences in resilience.
- Found strong **negative correlation** between misinformation and resilience across all countries.

---

## Tools & Technologies

- **Languages**: Python  
- **NLP Libraries**: NLTK, LIWC  
- **ML Libraries**: Scikit-learn, NumPy, Pandas  
- **Analytics**: Correlation analysis, Trend modeling (polynomial/Gaussian), Normalization  
- **Visualization**: Matplotlib  
- **APIs**: Twitter API

---

## Impact & Applications

- Provided a real-time, scalable alternative to traditional survey-based resilience assessments.
- Supported evidence-based policymaking by uncovering how social media sentiment and information quality influence community resilience.
- Demonstrated practical use of NLP and ML in public health informatics and crisis response analysis.

---

## Future Work

- Enhance SPCR framework using transformer-based language models (e.g., BERT, RoBERTa) for deeper sentiment and intent analysis.
- Apply agent-based simulation and deep learning for forecasting resilience trends.
- Generalize the framework to other domains (e.g., disaster recovery, geopolitical crises).

## Related Publication

{% bibliography --query @einstein1920relativity %}
