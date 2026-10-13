---
permalink: /
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
Hello! I am Qamar Zaman, a Computer Engineer. I completed my Bachelor's degree in Computer Engineering at the National University of Sciences and Technology (NUST), Pakistan.

I am currently working with [Dr. Sagheer Khan](https://pure.kfupm.edu.sa/en/persons/sagheer-khan/) (SDAIA–KFUPM Joint Research Center for Artificial Intelligence, King Fahd University of Petroleum & Minerals) on the Internet of Things (IoT), the Internet of Medical Things (IoMT) and digital twins for healthcare.

My research focuses on contactless human sensing with WiFi. During my undergraduate studies, I worked with [Dr. Muhammad Salman](https://salmanpolito.github.io/) and Dr. Sagheer Khan on occupancy detection using WiFi Channel State Information (CSI). I built a real-time sensing system on a Raspberry Pi with Nexmon. This work led to a first-author journal paper, [PiSense](https://link.springer.com/article/10.1007/s00607-026-01751-9), in *Computing* (Springer, 2026), and a public [CSI dataset on IEEE DataPort](https://ieee-dataport.org/documents/csi-dataset-wifi-based-human-detection).

I also have hands-on experience in machine learning, deep learning and NLP. My hardware background includes FPGA design, embedded Linux and edge AI deployment.

I am always happy to discuss research ideas! Please feel free to reach out to me at zqamar243463 [at] gmail [dot] com.

## Research Interests

- **Wireless and contactless sensing:** using WiFi Channel State Information (CSI) to detect human presence, activity and occupancy without cameras or wearables.
- **IoT and the Internet of Medical Things (IoMT):** connected sensing systems for smart environments and healthcare monitoring.
- **Digital twins for healthcare:** virtual models of patients and care environments that combine real-time sensor data with AI.
- **Machine learning and deep learning for signals:** signal processing, feature extraction and semi-supervised learning on time-series sensor data.
- **Edge AI and embedded systems:** running intelligent models on low-cost hardware such as the Raspberry Pi and FPGAs.

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
