---
title: "Subspace-based Adaptive GMM Error Modeling for Fault-Aware Vehicular GNSS Positioning in Urban Canyons"
collection: publications
category: manuscripts
permalink: /publication/2024-08-26-Adaptive-GMM-FDE
excerpt: "Simultaneous adaptive error modeling and fault detection and exclusion <br/><img src='/assets/images/AdpGMM-cover.jpg' width = '500'>"
date: 2024-08-26
venue: 'IEEE Transactions on Intelligent Vehicles'
doi: '10.1109/TIV.2024.3450198'
paperurl: '/files/Subspace-basedAdaptiveGMMErrorModelingforFault-AwarePseudorange-basedPositioninginUrbanCanyons.pdf'
citation: 'Yan, P., Xia, X., Brizzi, M., Wen, W., & Hsu, L. T. (2024). &quot;Subspace-based Adaptive GMM Error Modeling for Fault-Aware Pseudorange-based Positioning in Urban Canyons&quot;. <i>IEEE Transactions on Intelligent Vehicles</i>, http://dx.doi.org/10.1109/TIV.2024.3450198'
bibtex: |
  @article{yan2024adaptive,
    author = {Yan, Penggao and Xia, Xiaoxuan and Brizzi, Marco and Wen, Weisong and Hsu, Li-Ta},
    title = {Subspace-based Adaptive GMM Error Modeling for Fault-Aware Pseudorange-based Positioning in Urban Canyons},
    journal = {IEEE Transactions on Intelligent Vehicles},
    year = {2024},
    doi = {10.1109/TIV.2024.3450198}
  }
---

### 1) What problem is this paper solving?
**Context**: Fixed static error models fail in dynamic urban environments where multipath varies.  
**Core contribution**: A subspace-based adaptive Gaussian Mixture Model (GMM) that updates in real-time.  
**Achieved goal**: Improved Fault Detection and Exclusion (FDE) and positioning accuracy in urban canyons.

### 2) Why is this paper important?
**What changed**: Vehicles move through rapidly changing environments (open sky to deep urban).  
**Problem created**: Static models are either too optimistic (miss faults) or too pessimistic (false alarms).  
**Why current solutions fail**: They cannot adapt to the instantaneous severity of multipath and NLOS.

### 3) How does this paper solve it?
**Contribution 1**: Divides measurement space into sub-bins based on elevation and C/N0.  
**Contribution 2**: Dynamically updates GMM error profiles for each bin and excludes abnormal measurements over a sliding window.  
**Key result**: Reduced mean positioning error by 9-16% in real-world urban datasets.

🎯 **Takeaway**: Dynamic environments need dynamic error models; adapting GMMs in real-time solves this.

<img src='/assets/images/AdpGMM-cover.jpg' width = '900'>

{% include gittalk.html %}
