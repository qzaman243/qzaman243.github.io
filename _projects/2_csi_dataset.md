---
layout: page
title: CSI Dataset
description: Public WiFi CSI dataset for human detection (IEEE DataPort)
img: assets/img/research/dataset-csi-sniffing.png
importance: 3
category: research
related_publications: true
---

To collect the data, a Raspberry Pi 4B with Nexmon-patched firmware passively sniffs WiFi packets from a router. It extracts CSI (amplitude and phase) across 64 subcarriers on the 2.4 GHz band and saves it as CSV. The dataset includes raw `.pcap` captures, pre-processed `.csv` files, Python capture scripts, DWT denoising and Doppler-based motion features.

[View the dataset on IEEE DataPort](https://ieee-dataport.org/documents/csi-dataset-wifi-based-human-detection) · DOI: [10.21227/smn7-jb67](https://doi.org/10.21227/smn7-jb67)

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/research/dataset-csi-sniffing.png" title="CSI data collection" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Data collection: router, Raspberry Pi 4B sniffer with Nexmon firmware, packet sniffing and CSV output of 64 subcarriers.
</div>

The dataset covers three activity levels (static, mild and aggressive movement) in three room sizes: small (3.5×3.5), medium (4×5) and large (8×8).

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/research/dataset-activities-rooms.png" title="Activities and rooms" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Activity levels (static, mild, aggressive) and room sizes (small, medium, large).
</div>
