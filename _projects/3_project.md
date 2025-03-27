---
layout: page
title: Community Resilience
description: AI-driven disaster resilience modeling through NLP, social sensing, and critical infrastructure data integration.
img: assets/img/z3.png
redirect: https://unsplash.com
importance: 1
category: [Natural Language Processing, Energy Data Science]
---

<!-- ### **Case Study: AI-Driven Rare Disease Research Collaborative Network** -->

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/z3.png" title="AI-Driven Rare Disease Research Collaborative Network" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
    A cyber-physical-social system weathering disaster through interconnected data, NLP, and adaptive modeling.
</div>

---


# 1. Introduction

Disasters like hurricanes and floods increasingly disrupt modern communities across cyber, physical, and social domains. Understanding how populations behave and infrastructures perform during crises is essential for emergency response, risk mitigation, and long-term recovery. This project introduces an AI-powered, multi-agent cyber-physical-social resilience model, combining natural language processing, social media analytics, and infrastructure data to assess and predict community resilience.

Using real-world data from Hurricanes Harvey and Irma, we develop a system that models dynamic behavioral and infrastructure responses. Through NLP-based social sensing (Twitter, Google Trends), power utility data, and emergency services reports, we quantify resilience across domains.

# 2. Key Questions Addressed

- How can NLP and social sensing quantify human response and emotion during disasters?
- What role do misinformation and online media play in shaping public behavior?
- How do infrastructure interdependencies (e.g., power & emergency services) affect resilience?
- How can we model cyber-physical-social feedback loops using multi-agent simulations?
- What resilience metrics best reflect dynamic community functionality?

# 3. The Problem

Modern cities rely on tightly coupled systems—social networks, digital platforms, and physical infrastructures. During disasters, misinformation, infrastructure failure, and social panic amplify risk. Challenges include:

- **Modeling Human Behavior**: Quantifying fear, cooperation, and adaptability in real time.
- **Infrastructure Complexity**: Capturing the dependencies between power systems, emergency services, and social networks.
- **Fake News & Risk Perception**: Measuring how misinformation spreads and shapes behavior.
- **Data Fusion**: Integrating multimodal datasets (text, time-series, spatial) for resilience analysis.

# 4. The Importance

This project pioneers a holistic view of disaster resilience:

- **Behavioral Insights via NLP**: Extract mental health signals, risk perception, and collective cooperation from social media using tools like LIWC and SEANCE.
- **Misinformation Modeling**: Quantify the spread and impact of fake news using fact-checking sources like Snopes.
- **Infrastructure Simulation**: Model dynamic access to electricity and emergency services using FEMA and utility data.
- **Multi-Agent Systems**: Simulate how individual and group behaviors evolve over time based on external shocks.

# 5. The Solution

## 5.1. Data Preparation

- **Social Media Collection**: Over 490,000 tweets related to Hurricanes Harvey and Irma were collected using Twitter APIs.
- **News & Fake News**: Crawled and validated CNN articles and Snopes fact checks to assess sentiment and misinformation.
- **Infrastructure Data**: Acquired power outage and emergency response data from FEMA and utility providers.

## 5.2. NLP and Text Mining

- **Psychological Analysis with LIWC**: Measured fear, adaptability, cooperation, and risk perception from tweets.
- **Sentiment and Emotion Tracking**: Applied SEANCE, WordNet, MPQA, and NRC lexicons to classify emotional tone and cognitive load.
- **Topic Analysis**: Analyzed top n-grams in fake news vs. authentic posts.

## 5.3. Dynamic Modeling

- **Multi-Agent Simulation**: Agents simulate adaptive behavior across physical, cyber, and social layers, updating in response to disaster severity, news sentiment, and infrastructure status.
- **Behavioral Threshold Modeling**: Used logistic functions to model fear, learning, cooperation, and flexibility thresholds.
- **Cyber-Physical-Social Interdependencies**: Simulated how power outages trigger fear and how empathy between communities supports recovery.

## 5.4. Resilience Metrics

- **Social**: Fear, cooperation, adaptability, learning, risk perception.
- **Cyber**: News positivity, fake news volume.
- **Physical**: Electricity access from DERs, microgrids, and utilities; emergency services availability.

# 6. Results and Outcomes

- Tweet-based fear index matched real-world outage timelines.
- Higher cooperation correlated with faster recovery and learning.
- Communities with stronger internal ties showed higher resilience despite smaller populations.
- Fake news volumes spiked before behavior shifts (e.g., evacuations, panic).
- All resilience features—fear, health, adaptability, and electricity access—were validated using daily, hourly, and 3-hour simulations, achieving R² scores > 0.9 across most metrics.

# 7. Conclusion

This project demonstrates how natural language processing, multi-agent modeling, and critical infrastructure data can be fused to dynamically measure and simulate community resilience. By analyzing text data through a psychological lens and integrating it with real-time infrastructure metrics, we provide actionable insights into disaster behavior and system interdependencies.

# 8. Skills and Tools Used

- **NLP & Text Mining**: LIWC, SEANCE, MPQA, WordNet, NRC Lexicon
- **Programming**: Python, Pandas, Scikit-learn, TensorFlow (for text classification tasks)
- **Data Collection**: Twitter API, Google Trends, FEMA, CNN, Snopes
- **Simulation & Modeling**: Multi-agent systems, threshold models, logistic functions
- **Visualization**: Matplotlib, Seaborn
- **Statistical Validation**: R² analysis, QQ-plots, Pearson/Kendall/T-tests

# 9. Future Directions

- Generalization to Other Disasters: Wildfires, pandemics, floods.
- Multi-Modal Fusion: Combine geospatial, textual, and IoT sensor data.
- Real-Time Monitoring Dashboards: For emergency services and public health agencies.
- Personalized Risk Modeling: Predict behavior shifts at neighborhood or individual levels.
- Explainable AI: Better interpretation of NLP-derived metrics for policymakers.
