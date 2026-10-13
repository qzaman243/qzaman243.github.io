---
permalink: /
title: "Welcome to Zaman's Academic Website!"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
I am a Computer Engineering graduate with strong research interests at the intersection of Artificial Intelligence, Machine Learning, and hardware-centric intelligent systems. My academic work focuses on developing non-invasive human sensing and occupancy detection systems using Wi-Fi Channel State Information (CSI), where I integrate signal processing, machine learning, and embedded systems to solve real-world problems.

During my undergraduate research, I designed and implemented a Wi-Fi-enabled occupancy detection system using Raspberry Pi and Nexmon, involving real-time CSI extraction, noise reduction, feature engineering, and ML-based classification. This work led to the publication of a [CSI dataset on IEEE DataPort](https://ieee-dataport.org/documents/csi-dataset-wifi-based-human-detection) and a first-author journal paper, [PiSense](https://link.springer.com/article/10.1007/s00607-026-01751-9), in *Computing* (Springer, 2026).

In parallel, I have hands-on experience in machine learning, deep learning, and computer vision, including regression models, CNN-based systems, GANs (CycleGAN), and real-time inference pipelines. My hardware background includes FPGA design, embedded Linux, UART-based systems, and edge AI deployment, enabling me to bridge the gap between theory and implementation.
## My Research at a Glance

### PiSense: WiFi-based occupancy detection
*Published in Computing (Springer), 2026. [Read the paper →]({{ site.baseurl }}/publication/2026-10-10-pisense-occupancy-detection)*

PiSense detects whether a room is occupied using only the WiFi signals already in the room. No cameras or wearables are needed. A Raspberry Pi captures CSI, cleans it with DC/null-subcarrier removal and wavelet (DWT) filtering, and then extracts features in two ways: an autoencoder (semi-supervised) or maximum eigenvalues (supervised). A trained ML/DL model uses these features to decide in real time whether the room is occupied.

[![PiSense methodology: CSI capture, preprocessing, feature extraction and ML/DL classification]({{ site.baseurl }}/images/research/pisense-methodology.png)]({{ site.baseurl }}/publication/2026-10-10-pisense-occupancy-detection)

The supervised branch reduces the high-dimensional CSI matrices to one value per time window: the normalized maximum eigenvalue. When someone moves, this value drops sharply, which gives a compact and robust occupancy signal.

[![Dimensionality reduction of CSI matrices into maximum eigenvalues over time]({{ site.baseurl }}/images/research/pisense-dimensionality-reduction.png)]({{ site.baseurl }}/publication/2026-10-10-pisense-occupancy-detection)

### CSI Dataset for WiFi-based human detection
*Published on IEEE DataPort, 2025. [See the dataset →]({{ site.baseurl }}/publication/2025-06-11-csi-dataset-wifi-human-detection)*

To collect the data, a Raspberry Pi 4B with Nexmon-patched firmware passively sniffs WiFi packets from a router. It extracts CSI across 64 subcarriers and saves it as CSV.

[![CSI data collection: router, Raspberry Pi 4B sniffer with Nexmon firmware, packet sniffing, CSV of 64 subcarriers]({{ site.baseurl }}/images/research/dataset-csi-sniffing.png)]({{ site.baseurl }}/publication/2025-06-11-csi-dataset-wifi-human-detection)

The dataset covers three activity levels (static, mild and aggressive movement) in three room sizes: small (3.5×3.5), medium (4×5) and large (8×8).

[![Activity levels (static, mild, aggressive) and room sizes (small, medium, large)]({{ site.baseurl }}/images/research/dataset-activities-rooms.png)]({{ site.baseurl }}/publication/2025-06-11-csi-dataset-wifi-human-detection)

See all of my work on the [Publications page]({{ site.baseurl }}/publications/).

## Visitor Statistics
<a href="https://mapmyvisitors.com/web/1c1he"  title="Visit tracker"><img src="https://mapmyvisitors.com/map.png?d=D7lfDzzB7axCyg-zSymPkCvWXgmGaN9--XxQ_wHREXM&cl=ffffff" /></a>
