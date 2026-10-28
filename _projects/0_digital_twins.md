---
layout: page
title: Digital Twins in Healthcare 4.0
description: Review paper on digital twins for healthcare (submitted)
img: assets/img/research/digital-twins-healthcare.png
importance: 1
category: research
---

A **digital twin** is a living virtual copy of a real patient, organ or care environment. It is kept up to date with data from sensors and clinical systems, and it uses AI and simulation to help predict what will happen next. In healthcare, digital twins could help doctors monitor patients continuously, test treatments virtually before applying them, and catch problems earlier.

I am contributing to a review paper on digital twins in **Healthcare 4.0**, together with [Dr. Sagheer Khan](https://pure.kfupm.edu.sa/en/persons/sagheer-khan/) (SDAIA–KFUPM Joint Research Center for AI). The review covers the technologies that make healthcare digital twins possible, such as IoT and Internet of Medical Things (IoMT) sensing, communication networks, computing and artificial intelligence, along with their clinical applications and the challenges that remain.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/research/digital-twins-healthcare.png" title="Digital twins in healthcare" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The physical patient and their digital twin, linked by IoMT sensing, 5G/6G connectivity, AI, edge and cloud computing, hybrid models and feedback.
</div>

## From factories to hospitals

The digital twin idea started in engineering. Aerospace and manufacturing teams linked physical machines to virtual models so they could monitor them, predict failures and test changes safely. As sensors, connectivity, cloud computing and AI matured with **Industry 4.0**, the same idea moved into medicine.

Healthcare has followed a similar path:

- **Healthcare 1.0:** in-person visits and paper records
- **Healthcare 2.0:** electronic records and online portals
- **Healthcare 3.0:** telemedicine and remote monitoring
- **Healthcare 4.0:** AI, IoT, big data and cloud computing working together for connected, personalised and preventive care

Digital twins are one of the most promising technologies of this fourth stage.

## Model, shadow or twin?

Not every virtual model of a patient is a true digital twin. A common way to tell them apart is by how data flows between the real and virtual sides:

| | Data flow | Example |
|---|---|---|
| **Digital model** | None. It is built once and doesn't update automatically. | A 3D heart model made from a single scan |
| **Digital shadow** | One way, from the patient to the model | A dashboard that mirrors live readings from a wearable |
| **Digital twin** | Both ways. The model updates from the patient, and its predictions feed back into care. | A virtual patient that tracks live data and helps choose the next treatment |

## What goes into a healthcare digital twin

No single technology makes a digital twin. It takes data from wearables, medical devices and health records, networks to carry that data, computing power to process it, and AI or simulation models to turn it into useful predictions. All of this has to be secure, because health data is some of the most sensitive data there is.

## Why it matters

As the world's population ages, hospitals and care homes are under growing pressure. Healthcare needs to shift from reacting to illness towards **continuous, predictive and preventive care**. Digital twins could help by:

- monitoring patients continuously at home and in hospital
- spotting warning signs earlier
- letting doctors try treatments on a virtual patient first
- personalising care to each individual
- helping hospitals plan beds, staff and resources

## Why it's hard

Building a twin that a doctor can rely on is still difficult. Patient data comes from many systems in different formats. The human body is far more complex and changeable than a machine. And models must be accurate, explainable, secure and validated before they can guide real clinical decisions. Most healthcare digital twins today are still research prototypes.

## How this connects to my work

My research focuses on **contactless sensing**. [PiSense]({{ '/projects/1_pisense/' | relative_url }}) and the [CSI dataset]({{ '/projects/2_csi_dataset/' | relative_url }}) use ordinary Wi-Fi signals to detect people without cameras or wearables. Sensing like this can provide a steady, comfortable and privacy-friendly stream of data, which is exactly what a healthcare digital twin needs to stay up to date.

**Status:** submitted for publication. More details will be added here once the paper is published.
