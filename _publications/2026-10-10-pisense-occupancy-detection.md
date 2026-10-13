---
title: "PiSense: A Raspberry Pi-Based Real-Time Occupancy Detection System Using CSI from Commodity WiFi"
collection: publications
category: manuscripts
permalink: /publication/2026-10-10-pisense-occupancy-detection
excerpt: 'A low-cost, real-time occupancy detection system that uses WiFi Channel State Information (CSI) captured on a Raspberry Pi with the Nexmon toolchain.'
date: 2026-10-10
venue: 'Computing (Springer), vol. 108, no. 11, art. 161'
paperurl: 'https://link.springer.com/article/10.1007/s00607-026-01751-9'
citation: 'Q. Zaman, M. Ahmad, S. Khan, and M. Salman, &quot;PiSense: A Raspberry Pi-based real-time occupancy detection system using CSI from commodity WiFi,&quot; <i>Computing</i>, vol. 108, no. 11, art. 161, 2026. doi: 10.1007/s00607-026-01751-9'
---
**Authors:** Qamar Zaman, Muhammad Ahmad, Sagheer Khan, Muhammad Salman

**DOI:** [10.1007/s00607-026-01751-9](https://doi.org/10.1007/s00607-026-01751-9)

## Methodology

![PiSense methodology: CSI capture, preprocessing, feature extraction and ML/DL classification]({{ site.baseurl }}/images/research/pisense-methodology.png)

CSI is captured passively from commodity WiFi. It is cleaned with DC/null-subcarrier removal and Discrete Wavelet Transform (DWT) filtering. Features are then extracted in one of two ways: automatically by an autoencoder (semi-supervised) or as maximum eigenvalues (supervised). A trained ML/DL model uses them to detect occupancy in real time.

## Dimensionality reduction

![Dimensionality reduction of CSI matrices into maximum eigenvalues over time]({{ site.baseurl }}/images/research/pisense-dimensionality-reduction.png)

The CSI matrices for each time window are reduced to a single normalized maximum eigenvalue. Plotting this value over time shows clear drops when a person moves in the room.

Related dataset: [CSI Dataset for WiFi Based Human Detection]({{ site.baseurl }}/publication/2025-06-11-csi-dataset-wifi-human-detection)

[Read the article on SpringerLink](https://link.springer.com/article/10.1007/s00607-026-01751-9)
