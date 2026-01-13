---
layout: page
title: Unscented Kalman Filter
description:
img: assets/img/Project_Card/UKF.png
importance: 13
category: work
giscus_comments: false
featured: true 
---

This project recreated and implemented “A Quaternion-Based Unscented Kalman Filter for Orientation Tracking” by Edgar Kraft, building a fully nonlinear UKF for attitude estimation from raw IMU data. Operating directly in quaternion space, the filter propagates uncertainty through true rotational dynamics using sigma points, avoiding linearization and preserving the geometry of orientation. By fusing gyroscope and accelerometer measurements within a probabilistic framework, the system achieved stable, drift-resistant estimates that closely tracked Vicon ground truth across diverse motion datasets. Achieving this level of performance required careful, dataset-specific tuning of process and measurement noise, underscoring that while a UKF is powerful, it is not a universal, drop-in solution for all sensing regimes.

<div class="PDF">
    <iframe class="pdf" 
                    src="https://hudsonkortus.github.io/assets/pdf/p1b_group8.pdf">
    </iframe>
</div>
