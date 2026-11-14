---
layout: page
title: Multi-Object Tracking
description: Real-time tracking of people and vehicles in video with YOLOv5 and Deep SORT
img: assets/img/research/multi-object-tracking.jpg
importance: 5
category: computer vision
---

**Supervisor:** Shahid Ismail

**Computer Vision semester project, National University of Sciences and Technology (NUST), Islamabad, 2025**

## Background and Goals

Object detection finds objects in a single image. Many real-world systems also need to know **which object is which over time**: the same pedestrian walking across a street, or the same car moving through traffic. This is **object tracking**. It keeps a consistent identity for each object across video frames, and it is the basis of autonomous driving, surveillance, sports analytics and gesture-based interfaces.

The goal of this project was to build a **multiple object tracking (MOT)** system that detects people and vehicles in a busy street video, gives each one a unique ID, and keeps that ID as they move through the scene.

**Two central questions:**

(i) Can a modern object detector be combined with a tracking algorithm to follow many objects at once in a crowded scene?

(ii) Can each object keep the same identity across frames, even as people pass close to one another?

## Methodology

The system follows the **tracking-by-detection** approach: detect objects in every frame, then link those detections across frames.

- **Object detection:** YOLOv5 (PyTorch) finds objects in each frame. Detections are filtered by class (person, car, truck, bus and motorcycle) and by confidence.
- **Motion prediction:** a Kalman filter predicts where each tracked object will be in the next frame.
- **Appearance features:** Deep SORT describes how each object looks, which helps tell similar objects apart.
- **Data association:** the Hungarian algorithm matches new detections to existing tracks, so each object keeps its ID.
- **Visualisation:** each frame is drawn with bounding boxes, class labels, track IDs and a live FPS counter, and the annotated video can be saved.

The system was tested on **MOT16-03**, a crowded street scene from the MOT16 benchmark, using Python, OpenCV, YOLOv5 and the Deep SORT Realtime library.

## Key findings

- **Many objects tracked at once.** People, cars and motorcycles in a dense street scene are detected and followed together.
- **Stable identities.** Each object keeps a unique ID across frames, which is the core requirement of multiple object tracking.
- **Correct classes.** Object classes stay consistent as they are tracked.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/research/multi-object-tracking.jpg" title="Multi-object tracking output" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Tracking output on the MOT16-03 street scene: each person, car and motorcycle has a bounding box, a class label and a unique track ID.
</div>

The same approach can be applied to traffic monitoring, crowd analysis, sports analytics and surveillance.
