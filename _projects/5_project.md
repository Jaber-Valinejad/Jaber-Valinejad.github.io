---
layout: page
title: Energy market
description: Multi-Carrier Energy Market Optimization & Bayesian Uncertainty Quantification
img: assets/img/z5.png
importance: 3
category: Energy Data Science
---

<!-- ### **Case Study: Multi-Carrier Energy Market Optimization** -->

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid loading="eager" path="assets/img/z5.png" title="Multi-Carrier Energy Market Optimization" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
<div class="caption">
    Data-Driven Investment Planning and Forecasting in Renewable-Dominated Power Systems.
</div>

---

# 1. Introduction

Modern power and energy systems are undergoing rapid transformation due to the rise of renewable energy and distributed infrastructure. This project addresses two critical challenges:

- Long-term investment planning in multi-carrier energy markets (electricity, gas, thermal) under regulatory incentives and strategic competition.
- Short-term uncertainty quantification in stochastic economic dispatch (SED) with high-dimensional wind power data.

Through a fusion of multi-level optimization, Bayesian machine learning, and manifold learning techniques, this work provides an integrated, computationally efficient solution for resilient, adaptive energy system operations and planning.

# 2. Key Questions Addressed

- How can strategic GENCOs plan investments across electricity, gas, and CHP units considering market regulations and competition?
- What are the optimal incentive mechanisms (e.g., capacity payments, firm contracts) to drive efficient infrastructure development?
- How can we model and forecast the uncertainty of renewable generation for real-time market operations?
- Can Gaussian Process Emulators and manifold learning replace Monte Carlo simulations in uncertainty propagation?
- How do these tools integrate into practical grid planning, operation, and policy analysis?

# 3. Problem Scope

This project targets two distinct but connected layers of power system challenges:

## A. Strategic Investment in Multi-Energy Markets

- **Tri-Level Optimization**: Captures GENCO investment strategy, market offerings, and system-level welfare maximization.
- **Regulatory and Financial Incentives**: Models policy impacts like tax credits, firm contracts, and capacity payments.
- **Stochastic Load Modeling**: Uses Markov chains to simulate multi-stage demand uncertainty.

## B. Uncertainty Quantification in Stochastic Economic Dispatch

- **High-Dimensional Renewable Inputs**: Hourly wind farm outputs across multiple locations, modeled as spatiotemporal random fields.
- **Curse of Dimensionality**: Addressed with nonlinear dimensionality reduction (Isomap).
- **Surrogate Modeling**: GPE replaces time-intensive Monte Carlo methods, enabling efficient inference.

# 4. Why It Matters

- **For Policymakers**: Quantifies the effectiveness of financial incentives for clean energy expansion.
- **For System Operators**: Enables reliable real-time decision-making under renewable variability.
- **For Industry**: Provides an integrated framework for investment, operation, and forecasting in future grid infrastructure.
- **For Researchers**: Demonstrates how advanced ML tools can solve hard optimization and simulation problems in power systems.

# 5. Methodological Highlights

## 5.1. Multi-Level Market Optimization

- **Tri-level structure**: Investment → Offering → Social Welfare
- **Mathematical Tools**: Mixed-Integer Linear Programming (MILP), Karush–Kuhn–Tucker (KKT) conditions
- **Scenario Analysis**: Demand uncertainty simulated using branching Markov chains
- **Case Study**: Realistic energy hub with electricity, gas, and heat networks (without IEEE benchmark dependence)

## 5.2. Bayesian Uncertainty Quantification (UQ) Framework

- **Dimensionality Reduction**: Isomap captures latent structure in wind data better than traditional PCA/KLE
- **Gaussian Process Emulators (GPEs)**: Serve as nonparametric surrogate models for SED
- **Bayesian Inference**: Uses MLE and quadratic basis priors for accurate mean/variance estimation
- **Sampling**: Latin Hypercube Sampling (LHS) in latent space allows efficient scenario generation
- **KDE-Based PDF Estimation**: Models non-Gaussian latent distributions without parametric assumptions

# 6. Key Results

- 35% improvement in cost-optimized investment strategies with proper incentive modeling
- ~0.1% relative error in cost estimates using only 100 GPE training samples (vs. 8,000 MC samples)
- Computational time reduced from hours (MC) to seconds (GPE-based UQ)
- Dimensionality reduction from 72D to 9D while preserving statistical accuracy
- Cross-season validation proves robustness in both winter and summer wind scenarios

# 7. Tools and Technologies

- **Optimization**: MILP, KKT, duality, tri-level programming
- **ML & Stats**: GPE, KDE, Isomap, MLE, Bayesian inference
- **Sampling**: Latin Hypercube Sampling (LHS), scenario generation
- **Programming**: Python, NumPy, SciPy, Scikit-learn, GAMS
- **Data Science**: Surrogate modeling, statistical forecasting, probabilistic modeling

# 8. Future Work

- Scale UQ methods to national-level or real-time control applications
- Combine this framework with multi-modal data (e.g., solar, grid status, price signals)
- Investigate deep GP and neural surrogate models for more expressive representations
- Develop APIs or lightweight inference engines for integration into energy platforms
- Extend market planning framework to include demand response, storage, and microgrids

# 9. Conclusion

This unified project leverages data science, optimization, and statistics to solve two fundamental challenges in the energy domain:

- How to plan infrastructure investments strategically in complex, regulated markets, and
- How to make robust, fast operational decisions under uncertainty using statistical surrogates.

By bridging market optimization with Bayesian uncertainty modeling, it provides a blueprint for modern, intelligent energy systems capable of balancing investment, reliability, and renewables integration at scale.
