---
layout: page
title: Digital Twins in Healthcare 4.0
description: A review of the technologies, applications and open challenges of healthcare digital twins (submitted)
img: assets/img/research/digital-twins-healthcare.png
importance: 1
category: research
---

A **digital twin** is a living virtual copy of a real patient, organ, physiological process or hospital. It is kept in sync with its physical counterpart through a continuous, two-way flow of data, so it can show the current state, predict what happens next, and let clinicians test an intervention virtually before applying it to the patient.

In this review, with Muhammad Ahmad and [Dr. Sagheer Khan](https://pure.kfupm.edu.sa/en/persons/sagheer-khan/) (SDAIA–KFUPM Joint Research Center for AI), we look at how digital twins are shaping **Healthcare 4.0**. Existing reviews tend to focus either on clinical applications or on a single technology. We instead follow the data as it moves through a twin, **from sensing to simulation**, and link each technology to how close healthcare twins are to real clinical use.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/research/digital-twins-healthcare.png" title="Digital twins in healthcare" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The physical patient and their digital twin, linked by IoMT sensing, 5G/6G connectivity, AI, edge and cloud computing, hybrid models and feedback.
</div>

## A twin is built in layers

A healthcare digital twin is not one technology but a stack of them. We organise it into six layers, and a key point of the review is that **a twin is only as good as its weakest layer**: an error in sensing, networking, computing or modelling carries through the whole system.

| Layer | What it does | Example technologies |
|---|---|---|
| **L1 · Sensing** | Collects data from the patient | IoMT devices, wearables, ECG/EEG/PPG, Wi-Fi CSI and RF sensing, medical imaging, electronic health records |
| **L2 · Connectivity** | Moves the data reliably | Wireless body area networks, 5G, 6G, integrated sensing and communication |
| **L3 · Computing** | Processes data at the right place | Edge, fog and cloud computing, TinyML, high-performance computing |
| **L4 · Integration** | Makes different data sources work together | HL7 FHIR, DICOM, big-data analytics, multimodal data fusion |
| **L5 · Intelligence & modelling** | Turns data into predictions | Physics-based, data-driven, hybrid and multiscale models, generative AI, explainable AI |
| **L6 · Interface & decision** | Puts results in clinicians' hands | Clinical decision support, extended reality (VR/AR/MR), virtual interventions |

Security, privacy (blockchain, federated learning) and regulation cut across every layer.

## Where digital twins are used today

We review **nine application areas** and place each on a maturity scale from concept to routine clinical care:

- **Diabetes and metabolism:** the most mature, with simulators already accepted by regulators and commercial precision-nutrition twins.
- **Cardiology:** in prospective clinical studies, for example virtual hearts that guide ablation and virtual drug tests.
- **Vital-sign monitoring:** contactless Wi-Fi CSI and RF sensing twins for respiration, hydration and elderly care, still at the research stage.
- **Oncology and neurology:** experimental twins for tumour growth, radiotherapy, epilepsy, multiple sclerosis and stroke.
- **Critical care and hospital operations:** sepsis twins at the verification stage, and hospital twins in pilot deployments.
- **Surgery and drug development:** XR surgical prototypes and in silico clinical trials.

No area has yet reached routine, continuously synchronised clinical care. Most patient twins reported in the literature are still preclinical.

## Open challenges

The review identifies eight challenges that keep twins in the lab:

1. Integrating data from many sources in different formats
2. Keeping the twin synchronised in real time at a reasonable computing cost
3. Verifying and validating a model that keeps changing, with quantified uncertainty
4. Translating research into clinics with real evidence of benefit
5. Privacy, security and trust
6. Bias, fairness and explainability
7. Ethics, regulation and standardisation
8. Sensing that is uncomfortable or intrusive for patients

## Future directions

We then outline nine research directions. These include:

- contactless RF sensing and integrated sensing and communication in 6G
- hybrid physics-informed and surrogate models
- foundation models and generative AI
- federated, privacy-preserving twins
- standardised validation frameworks with open benchmarks
- the edge–cloud continuum
- human-in-the-loop decision support
- prospective clinical trials
- the long-term goal of a complete human digital twin

## How this connects to my work

Contactless sensing is a recurring theme of the review. My own research on [PiSense]({{ '/projects/1_pisense/' | relative_url }}) and the [CSI dataset]({{ '/projects/2_csi_dataset/' | relative_url }}) uses Wi-Fi Channel State Information to sense people without cameras or wearables. That is exactly the kind of continuous, unobtrusive data source a healthcare digital twin needs.

**Status:** submitted for publication. The full paper and link will be added here once it is published.
