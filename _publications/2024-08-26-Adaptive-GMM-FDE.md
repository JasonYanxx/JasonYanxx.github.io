---
title: "Subspace-based Adaptive GMM Error Modeling for Fault-Aware Vehicular GNSS Positioning in Urban Canyons"
collection: publications
category: manuscripts
permalink: /publication/2024-08-26-Adaptive-GMM-FDE
excerpt: "Simultaneous adaptive error modeling and fault detection and exclusion <br/><img src='/assets/images/AdpGMM-cover.jpg' width = '500'>"
date: 2024-08-26
venue: 'IEEE Transactions on Intelligent Vehicles'
slidesurl: 'url'
paperurl: 'https://ieeexplore.ieee.org/abstract/document/10648803'
citation: 'Yan, P., Xia, X., Brizzi, M., Wen, W., & Hsu, L. T. (2024). &quot;Subspace-based Adaptive GMM Error Modeling for Fault-Aware Pseudorange-based Positioning in Urban Canyons&quot;. <i>IEEE Transactions on Intelligent Vehicles</i>, doi: 10.1109/TIV.2024.3450198'
---


Fault detection for localization systems with non-Gaussian measurement noises is a challenging task. This paper investigates the impacts of noise modeling on fault detection performance in the inertial measurement units (IMU) and light detection and ranging (LiDAR) integrated localization system based on the extended Kalman filter (EKF). Specifically, we model the noise distribution of LiDAR range measurements as a Gaussian mixture model (GMM) and establish a clear relationship between the measurement noise and the measurement residual in EKF through error propagation. After proving that the measurement residual is also GMM distributed, a test statistic is constructed by transforming the measurement residual to a variable that approximates a standard multivariate normal (MVN) distribution based on the law of total covariance. Then, a Chi-squared test is performed based on the constructed test statistic to detect potential faults. The performance of the proposed method is evaluated in the simulated environment regarding two types of measurement failures, including the step failure and the slope failure. Compared to the method that adopts Gaussian noise modeling, the proposed method demonstrates its superiority in detecting small faults and the improved sensitivity to slowly increasing faults.

<img src='/assets/images/AdpGMM-cover.jpg' width = '900'>