---
title: "Jackknife ARAIM: Efficient GNSS Integrity Monitoring for Simultaneous Faults under Non-Gaussian Errors"
collection: publications
category: manuscripts
permalink: /publication/2026-01-15-Jackknife-ARAIM
excerpt: "Efficient GNSS Integrity Monitoring for Simultaneous Faults under Non-Gaussian Errors <br/><img src='/assets/images/Jackknife-ARAIM-cover.jpg' width = '800'>"
date: 2026-01-15
venue: 'Aerospace Systems'
paperurl: 'https://arxiv.org/abs/2507.04284'
citation: 'Yan, P., Jin, R., Zhang, J., Wang, C., & Hsu, L. T. (2026). &quot;Jackknife ARAIM: Efficient GNSS Integrity Monitoring for Simultaneous Faults under Non-Gaussian Errors&quot;. <i>Aerospace Systems</i>.'
bibtex: |
  @article{yan2026jackknife,
    author = {Yan, Penggao and Jin, Ronghe and Zhang, Junyi and Wang, Cheng-Wei and Hsu, Li-Ta},
    title = {Jackknife ARAIM: Efficient GNSS Integrity Monitoring for Simultaneous Faults under Non-Gaussian Errors},
    journal = {Aerospace Systems},
    year = {2026},
  }
---

### 1) What problem is this paper solving?
**Context**: Solution Separation (SS) ARAIM usually assumes Gaussian errors, leading to conservative protection levels in reality.  
**Core contribution**: A non-Gaussian ARAIM framework using jackknife test to handle non-Gaussian errors efficiently.  
**Achieved goal**: Theoretically equivalent to SS ARAIM but with higher efficiency and tighter bounds.

<img src='/assets/images/SISRE-GPS-Galileo.png' width = '900'>
The folded CDF of (a) GPS and (b) Galileo SISRE for individual satellites from January 1st, 2020 to December 31st, 2022. A significant non-Gaussian pattern is observed.

### 2) Why is this paper important?
**What changed**: Real-world errors are non-Gaussian; existing multi-hypothesis fixes are too slow.  
**Problem created**: We trade off either safety (Gaussian assumption) or computational feasibility (MHSS).  
**Why current solutions fail**: They cannot handle simultaneous faults under non-Gaussian noise efficiently.

<img src='/assets/images/Jackknife-ARAIM-compution.png' width = '900'>
Computation time comparison for GPS-only constellation: (a) Trajectories of GPS satellites over a 24-hour period; (b) The box
plot of computation times for jackknife and SS ARAIM methods both with non-Gaussian overbounds.

### 3) How does this paper solve it?
**Contribution 1**: Uses fast scalar jackknife tests for single faults and triple-axis combinations for multi-faults.  
**Contribution 2**: Incorporates non-Gaussian overbounding to safely model heavy tails.  
**Key result**: Reduced 99.5th percentile Vertical Protection Level (VPL) below 40m (vs 60m for Gaussian) under GPS-Galileo dual constellation while being faster.

<img src='/assets/images/Jackknife-ARAIM-VPL.png' width = '900'>
99.5 percentile of the VPL over the course of the day yielded by (a) the SS ARAIM with Gaussian overbounds; (b) the proposed jackknife ARAIM with Gaussian overbounds; and (c) the proposed jackknife ARAIM with non-Gaussian overbounds for the GPS-Galileo dual constellation.

🎯 **Takeaway**: Jackknife ARAIM offers a faster, tighter, and distribution-free path to high-integrity navigation.

{% include gittalk.html %}
