---
layout: page
title: PiSense
description: Real-time WiFi occupancy detection on a Raspberry Pi
img: assets/img/research/pisense-methodology.png
importance: 1
category: research
related_publications: true
---

PiSense detects whether a room is occupied using only the WiFi signals already in the room. No cameras or wearables are needed. A Raspberry Pi with the Nexmon toolchain passively captures Channel State Information (CSI). The data is cleaned with DC/null-subcarrier removal and wavelet (DWT) filtering, and features are then extracted in two ways: an autoencoder (semi-supervised) or maximum eigenvalues (supervised). A trained ML/DL model uses these features to decide in real time whether the room is occupied.

Published in _Computing_ (Springer, 2026). [Read the paper](https://link.springer.com/article/10.1007/s00607-026-01751-9) · [Code on GitHub](https://github.com/qzaman243/WIFI-enabled-Occupancy-Detection-System)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/research/pisense-methodology.png" title="PiSense methodology" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The PiSense pipeline: CSI capture, preprocessing, semi-supervised and supervised feature extraction, and ML/DL classification.
</div>

The supervised branch reduces the high-dimensional CSI matrices to one value per time window: the normalized maximum eigenvalue. When someone moves, this value drops sharply, which gives a compact and robust occupancy signal.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/research/pisense-dimensionality-reduction.png" title="Dimensionality reduction" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Dimensionality reduction of CSI matrices into maximum eigenvalues over time.
</div>
