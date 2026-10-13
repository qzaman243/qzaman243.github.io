---
title: "CSI Dataset for WiFi Based Human Detection"
collection: publications
category: datasets
permalink: /publication/2025-06-11-csi-dataset-wifi-human-detection
excerpt: 'Time-series WiFi CSI (amplitude and phase, 64 subcarriers, 2.4 GHz / 20 MHz) collected with a Raspberry Pi 4 and Nexmon in three indoor rooms, labelled Occupied / Not Occupied, for real-time indoor occupancy detection.'
date: 2025-06-11
venue: 'IEEE DataPort'
paperurl: 'https://ieee-dataport.org/documents/csi-dataset-wifi-based-human-detection'
citation: 'Q. Zaman, M. Ahmad, M. Salman, and S. Khan, &quot;CSI Dataset for WiFi Based Human Detection,&quot; <i>IEEE DataPort</i>, June 11, 2025. doi: 10.21227/smn7-jb67'
---
**Authors:** Qamar Zaman, Muhammad Ahmad, Muhammad Salman, Sagheer Khan

**DOI:** [10.21227/smn7-jb67](https://doi.org/10.21227/smn7-jb67)

The dataset contains raw `.pcap` captures, pre-processed `.csv` files, Python capture scripts, Discrete Wavelet Transform denoising and Doppler-based motion features. It covers an empty room, one person (static and moving) and several people, recorded in a large lab, a small room and a medium office/classroom-sized room.

## Data collection setup

![CSI data collection: router, Raspberry Pi 4B sniffer with Nexmon firmware, packet sniffing, CSV of 64 subcarriers]({{ site.baseurl }}/images/research/dataset-csi-sniffing.png)

A Raspberry Pi 4B with Nexmon-patched firmware passively sniffs packets from a WiFi router while people are in the room. It saves CSI for 64 subcarriers as CSV.

## Activities and rooms

![Activity levels (static, mild, aggressive) and room sizes (small, medium, large)]({{ site.baseurl }}/images/research/dataset-activities-rooms.png)

Data was recorded for three activity levels (static, mild and aggressive movement) in three room sizes (small 3.5×3.5, medium 4×5, large 8×8).

This dataset was used in the paper [PiSense: A Raspberry Pi-Based Real-Time Occupancy Detection System Using CSI from Commodity WiFi]({{ site.baseurl }}/publication/2026-10-10-pisense-occupancy-detection).

[View the dataset on IEEE DataPort](https://ieee-dataport.org/documents/csi-dataset-wifi-based-human-detection)
