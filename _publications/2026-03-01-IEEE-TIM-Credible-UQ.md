---
title: "Credible Uncertainty Quantification under Noise and System Model Mismatch"
collection: publications
category: manuscripts
permalink: /publication/2026-03-01-IEEE-TIM-Credible-UQ
excerpt: "Unified NCI, NLL, and ES framework with empirical location test (ELT) and directional probing to diagnose noise vs. system model mismatch <br/><img src='/assets/images/TIM-Credible-UQ-cover.png' alt='Cover image for the credible uncertainty quantification paper' width='800'>"
date: 2026-03-01
venue: 'IEEE Transactions on Instrumentation and Measurement'
doi: '10.1109/TIM.2026.3682809'
publisherurl: 'https://ieeexplore.ieee.org/document/11479287'
publisherlabel: 'Published Version'
paperurl: 'https://arxiv.org/abs/2509.03311'
paperlabel: 'arXiv'
citation: 'Yan, P., Zhan, X., Sun, R., & Hsu, L.-T. (2026). &quot;Credible Uncertainty Quantification under Noise and System Model Mismatch&quot;. <i>IEEE Transactions on Instrumentation and Measurement</i>, 1-1. https://doi.org/10.1109/TIM.2026.3682809'
bibtex: |
  @article{yan2026credible,
    author = {Yan, Penggao and Zhan, Xingqun and Sun, Rui and Hsu, Li-Ta},
    title = {Credible Uncertainty Quantification under Noise and System Model Mismatch},
    journal = {IEEE Transactions on Instrumentation and Measurement},
    year = {2026},
    pages = {1--1},
    doi = {10.1109/TIM.2026.3682809},
    url = {https://doi.org/10.1109/TIM.2026.3682809}
  }
---

### 1) What problem is this paper solving?
**Context**: Filters and estimators report covariances or predictive distributions, but **credibility** of that uncertainty can fail under **noise model mismatch (NMM)** (e.g., wrong covariance scaling) or **system model misspecification (SMM)** (e.g., bias).  
**Core contribution**: A **unified multi-metric framework** combining **noncredibility index (NCI)**, **negative log-likelihood (NLL)**, and **energy score (ES)**, with an **empirical location test (ELT)** to detect SMM and **directional probing** on scaled covariances to separate NMM from SMM.  
**Achieved goal**: Turn patterns in credibility indicators into **actionable diagnoses** of which modeling assumption is wrong.

### 2) Why is this paper important?
**What changed**: Single-metric checks (e.g., NEES/NCI alone) can be **misleading** under violations—different metrics react asymmetrically to optimism vs. pessimism vs. bias.  
**Problem created**: Downstream fusion, planning, and safety logic depend on **trustworthy** uncertainty; miscalibration is hard to attribute without disentangling NMM and SMM.  
**Why this framework helps**: **NLL** and **ES** exhibit **complementary asymmetries**; combining them with **ELT** and probing yields robust diagnosis vs. single-metric baselines.

### 3) How does this paper solve it?
**Contribution 1**: **ELT** (energy-distance–based) detects **SMM**; **centering** errors mitigates bias so **NMM** effects can be isolated.  
**Contribution 2**: **Directional probing** scales reported covariances and compares **NLL/ES** responses to classify optimism, pessimism, and SMM.  
**Key result**: Simulations across six credibility scenarios reach **80%–100%** diagnosis accuracy and beat single-metric methods; a **real UWB positioning** study shows identification of **coexisting pessimism and SMM** where classical NEES/NCI are insufficient; complexity and scalability (including high state dimension) are analyzed.

<img src='/assets/images/TIM-Credible-UQ-cover.png' alt='Framework figure for credible uncertainty quantification' width='900'>
The framework for diagnosing NMM and SMM in a unified multi-metric framework.

🎯 **Takeaway**: Multi-metric credibility with ELT plus directional probing is a practical validation layer when you need to know *whether* and *why* reported uncertainty is wrong.

{% include gittalk.html %}
