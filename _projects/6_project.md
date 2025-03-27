---
layout: page
title: SmartGridGuard 
description: Real-Time Anomaly Detection and Insulation Coordination in Power Transmission Networks
img: assets/img/z6.png
importance: 4
category: Energy
---
<!-- ### **Case Study: boosting grid reliability with real-time insights.** -->

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/z6.png" title="Boosting grid reliability with real-time insights." class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
  A data-driven tool that improves power grid reliability through simulation and real-time anomaly detection under environmental stress.
</div>

---
# 1. Introduction

Power transmission networks are critical to energy delivery—but they are highly vulnerable to environmental stressors such as pollution and climate change. In regions like Mazandaran and Golestan (Northern Iran), increased pollution levels have significantly reduced insulator performance, causing outages, equipment failure, and reliability issues.

This project introduces **SmartGridGuard**, a data-driven system for analyzing, simulating, and optimizing insulation coordination under varying environmental conditions. It combines real-time anomaly detection, geospatial environmental data processing, and simulation-driven engineering analysis, delivering insights that drive smarter maintenance and operational strategies.

# 2. Key Questions Addressed

- How can real-time anomaly detection enhance reliability in high-voltage transmission systems?
- What data engineering techniques enable scalable storage and processing of power system simulations?
- How can environmental data be integrated into insulation coordination using simulation-based modeling?
- What software architecture supports both historical analysis and real-time monitoring?
- How can we ensure data quality, integrity, and operational compliance in infrastructure-scale systems?

# 3. The Problem

Traditional insulation coordination methods are outdated and reactive. In polluted and climate-sensitive areas, nearly **47% of outages** in high-voltage lines were traced to inadequate insulation, as shown in field studies from Northern Iran.

**Core technical challenges:**

- Processing large-scale environmental data (e.g., pollution, lightning risk, altitude)
- Simulating high-voltage behavior under multiple overvoltage conditions (switching, lightning, power frequency)
- Designing an automated pipeline for real-time anomaly detection
- Logging network activity and simulation output to an SQL database for traceability and reporting

# 4. Real-Time Anomaly Detection: The Story

During a 2015 winter storm, the Esfarayen-Aliabad 400kV line experienced multiple cascading outages due to salt pollution and inadequate creepage distance. Using SmartGridGuard, we simulated insulation behavior under extreme weather conditions and deployed a real-time anomaly detector that:

- Monitors high-voltage activity
- Predicts risk levels using pollution data from nearby weather stations
- Alerts operators of insulation vulnerabilities before failure occurs

# 5. The Solution

## 5.1 Data Processing and Simulation

- Integrated pollution, weather, altitude, and lightning datasets via ETL pipelines  
- Stored structured metadata and simulation output using SQL databases  
- Utilized MATLAB for simulation with a GUI-based engine for insulation coordination

## 5.2 Real-Time Anomaly Detection

- Designed a rule-based alerting system for rapid identification of dangerous conditions  
- Developed Python scripts to extract and ingest new data from regional weather stations  
- Triggered alerts based on thresholds derived from simulation-based models

## 5.3 Software Design

- Built a custom MATLAB application with GUI for engineering teams  
- Applied modular architecture to separate data processing, simulation, and anomaly detection  
- Created SQL-backed storage for model outputs, sensor logs, and outage metadata

# 6. Results and Outcomes

- **80% reduction** in outage duration  
- **200 MWh** reduction in lost energy  
- **>130 outage events prevented annually** after model deployment  
- SQL-based historical logs facilitated trend analysis and regulatory reporting

# 7. Conclusion

**SmartGridGuard** demonstrates the power of integrating simulation software, data engineering, and real-time monitoring in smart energy infrastructure. By simulating insulation behavior under harsh environmental conditions and embedding anomaly detection into operations, we’ve created a scalable solution for modern transmission networks.

# 8. Skills and Tools Used

- **Programming**: Python, MATLAB, C++  
- **Data Engineering**: SQL, ETL pipelines, structured logging  
- **Simulation & Modeling**: Insulation coordination, MATLAB GUI  
- **Anomaly Detection**: Threshold-based alerting, weather-linked diagnostics  
- **Data Sources**: Synoptic weather stations, pollution indices, lightning maps  
- **Software Architecture**: Modular design, simulation + real-time components

# 9. Future Directions

- Integrate machine learning models for predictive maintenance  
- Expand system to low- and mid-voltage networks  
- Enhance anomaly detection with multi-modal data fusion (e.g., IoT + satellite data)  
- Develop web-based dashboards for real-time visualization  
- Add automated quality checks for insulator degradation patterns
