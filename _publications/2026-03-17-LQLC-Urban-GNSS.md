---
title: "Improved GNSS Positioning in Urban Environments Using a Logistic Error Model"
collection: publications
category: manuscripts
permalink: /publication/2026-03-17-LQLC-Urban-GNSS
excerpt: "Logistic pseudorange errors and the Least Quasi-Log-Cosh (LQLC) M-estimator with IRLS for urban GNSS, validated in light, medium, and deep urban Hong Kong data <br/><img src='/assets/images/LQLC-urban-GNSS-cover.png' width = '800'>"
date: 2026-03-17
venue: 'ArXiv'
paperurl: 'https://arxiv.org/abs/2603.16420'
citation: 'Li, Z., Yan, P., Song, B., & Hsu, L. T. (2026). &quot;Improved GNSS Positioning in Urban Environments Using a Logistic Error Model&quot;. <i>arXiv preprint arXiv:2603.16420</i>. '
bibtex: |
  @misc{li2026improved,
    author = {Li, Zhengdao and Yan, Penggao and Song, Baoshan and Hsu, Li-Ta},
    title = {Improved GNSS Positioning in Urban Environments Using a Logistic Error Model},
    year = {2026},
    eprint = {2603.16420},
    archivePrefix = {arXiv},
    primaryClass = {eess.SP}
  }
---

### 1) What problem is this paper solving?
**Context**: Least squares (LS) follows from a Gaussian error model, but multipath and NLOS in cities produce heavy-tailed errors that Gaussian tails underestimate.  
**Core contribution**: Model errors with a **logistic** distribution and derive the corresponding MLE—the **Least Quasi-Log-Cosh (LQLC)** estimator—solved with **iteratively reweighted least squares (IRLS)**.  
**Achieved goal**: A simple, tractable alternative to Gaussian LS that better matches urban error tails and down-weights large residuals.


### 2) Why is this paper important?
**What changed**: Urban GNSS needs estimators aligned with heavy-tailed measurement error behavior without model complexity or extra sensors.  
**Problem created**: Gaussian model remains sensitive to large residuals that occur more often than the model allows.  
**Why current solutions help but differ**: Context maps and NLOS mitigation techniques add cost; without introducing extra sensors, we propose to use a new **statistical model** with closed-form estimator and efficient solver.

### 3) How does this paper solve it?
**Contribution 1**: Analysis on real measurement error samples (light, medium, deep urban in Hong Kong) show that logistic distribution can fit better than Gaussian while staying simpler than BGMM or Student’s-t for estimator design.  
**Contribution 2**: LQLC minimizes \\(\sum_i \ln(\cosh(\bar{r}_i)+1)\\); weights \\(w(r)=\tanh(r/2)/r\\) shrink influence for large normalized residuals.  
**Contribution 3**: Real SPP tests (GPS + Beidou L1, u-blox F9P vs. SPAN-CPT truth): **3D RMSE** improves by about **11%–31%** and **3D STD** by about **27%–61%** vs. LS; runtime stays **real-time** compatible. 

<img src='/assets/images/LQLC-urban-GNSS-cover.png' width = '900'>
Positioning results of LQLC vs. LS on real urban GNSS data in Hong Kong.

🎯 **Takeaway**: Logistic error modeling yields a practical robust urban GNSS estimator with clear tuning guidance and measured gains over LS across urban severity levels.

{% include gittalk.html %}
