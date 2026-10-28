---
layout: page
title: PiSense
description: Real-time, device-free occupancy detection using WiFi Channel State Information on a Raspberry Pi
img: assets/img/research/pisense-methodology.png
importance: 2
category: research
related_publications: true
---

**Supervisors:** [Dr. Muhammad Salman](https://salmanpolito.github.io/) and [Dr. Sagheer Khan](https://pure.kfupm.edu.sa/en/persons/sagheer-khan/)

**Undergraduate research project, National University of Sciences and Technology (NUST), Islamabad, 2024–2025**

## Background and Goals

Knowing whether a room is occupied is useful for smart buildings, energy saving, elderly care and safety. Today this is usually done with cameras, which raise privacy concerns and need a clear line of sight, or with wearables and motion sensors, which people must carry, charge or install.

WiFi offers another option. When a person stands, moves or breathes in a room, they change how WiFi signals travel between a router and a receiver. These changes appear in the **Channel State Information (CSI)**, a fine-grained description of the WiFi signal across many subcarriers. Because WiFi routers are already everywhere, CSI makes it possible to sense people **without cameras, wearables or new infrastructure**.

The goal of this project was to build a low-cost system that detects room occupancy in real time from the CSI of ordinary WiFi traffic, running entirely on a Raspberry Pi.

**Two central research questions:**

(i) Can CSI captured passively by a low-cost Raspberry Pi reliably tell an occupied room from an empty one?

(ii) Can the high-dimensional CSI be reduced to compact features that work well in rooms of different sizes and with different levels of activity?

## Methodology

- **Data collection:** A Raspberry Pi 4 Model B (Broadcom BCM43455c0 chipset) with Nexmon-patched firmware passively sniffs packets from a WiFi router on the 2.4 GHz band (20 MHz channel) and extracts CSI amplitude and phase across 64 subcarriers. Data was recorded in three rooms of different sizes, covering an empty room, one person (static and moving) and several people. The data is published as a [public dataset]({{ '/projects/2_csi_dataset/' | relative_url }}).
- **Preprocessing:** Null and DC subcarriers are removed, and the signal is denoised with the Discrete Wavelet Transform (DWT).
- **Feature extraction:** Two approaches were explored. In the supervised approach, the CSI matrices in each time window are reduced to their **normalized maximum eigenvalue**. In the semi-supervised approach, an **autoencoder** learns features automatically.
- **Classification:** Machine learning and deep learning models are trained to classify each time window as _Occupied_ or _Not Occupied_, and the system raises real-time alerts.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/research/pisense-methodology.png" title="PiSense methodology" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The PiSense pipeline: CSI capture on a Raspberry Pi, preprocessing, supervised and semi-supervised feature extraction, and ML/DL classification with real-time alerts.
</div>

## Key findings

- **WiFi alone is enough to sense occupancy.** CSI captured by an inexpensive Raspberry Pi reliably separates occupied rooms from empty ones, with no cameras or wearables.
- **One number per window captures the signal.** The normalized maximum eigenvalue stays stable when the room is empty and drops sharply when someone moves. This turns large CSI matrices into a compact, robust occupancy feature.
- **It runs in real time on low-cost hardware.** The whole pipeline, from capture to classification, runs on a Raspberry Pi, making it practical for smart buildings and homes.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/research/pisense-dimensionality-reduction.png" title="Dimensionality reduction" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Dimensionality reduction: CSI matrices are reduced to normalized maximum eigenvalues, which drop sharply when a person moves in the room.
</div>

This work was published in _Computing_ (Springer, 2026). The full paper is available [here](https://link.springer.com/article/10.1007/s00607-026-01751-9), and the code is on [GitHub](https://github.com/qzaman243/WIFI-enabled-Occupancy-Detection-System).
