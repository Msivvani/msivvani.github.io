---
layout: page
title: Hybrid Drive Quad-Copter for Pipeline Inspection
description: A dual-mode quadcopter for pipeline inspection with integrated crack detection mechanisms.
img: assets/img/P6_1.jpg
importance: 6
category: Undergraduate
related_publications: false
---

### Introduction
This project focused on the design and development of a hybrid drive quadcopter capable of operating in both aerial and ground modes for pipeline inspection. The system was designed to navigate through inaccessible spaces and perform anomaly detection, such as cracks and rust, on industrial pipelines. 

#### Image 1: Hybrid Drive Quad-Copter
<div class="text-center">
    {% include figure.liquid path="assets/img/P6_1.jpg" title="Hybrid Drive Quad-Copter" class="img-fluid rounded z-depth-1" %}
</div>

### Crack Detection Mechanism
- The quadcopter was equipped with a camera module and integrated deep learning-based crack detection algorithms.
- Leveraged a convolutional neural network (CNN) trained on industrial datasets, including crack and rust images.
- The model utilized:
  - **Convolutional Layers:** To extract features from input images.
  - **Pooling Layers:** To reduce dimensionality and enhance feature maps.
  - **Softmax Classification:** To identify and classify cracks with high precision.

Detection outputs were processed in real-time, with results visualized at the control station.

#### GIF: Quadcopter in Action
<div class="text-center">
    {% include figure.liquid path="assets/img/P6_2.gif" title="Quad-Copter in Action" class="img-fluid rounded z-depth-1" %}
</div>

### Results
- Successfully implemented and tested the crack detection mechanism.
- Demonstrated the capability to inspect pipelines in both aerial and ground modes, reducing the need for human intervention in hazardous environments.

