---
layout: page
title: Chassis Dimension Estimation
description: High-accuracy dimensional inspection of automotive chassis and cross members using visual feed.
img: assets/img/P1_1.jpg
importance: 4
category: Undergraduate
related_publications: false
---

### Introduction
Dimensional accuracy is critical in automotive manufacturing, particularly for chassis and cross members. To address the reliance on error-prone manual inspection, a high-accuracy automated inspection tool was developed. Using visual feeds from low-resolution CCTV cameras placed 7 meters above the ground, the system provided real-time dimensional accuracy assessments.

### Approach
The project focused on automating dimensional inspection with high precision. A dataset of 50+ industrial cross-member images was curated to evaluate and benchmark various corner detection architectures, including 10+ Siamese networks. The final system employed Zhang's calibration algorithm to compute the distortion coefficients, camera matrix, and rotational and translational matrices.

To estimate real-world dimensions:
1. The system detected corners of the chassis and cross members using advanced computer vision methods.
2. The pixel distances between detected corners were mapped to real-world values using the calculated projection matrices and SolvePnP method in MATLAB.

The results were visualized through an interactive graphical user interface that processed live visual feeds and computed dimensional metrics with exceptional accuracy.

### Results
The system demonstrated an impressive accuracy of **99.72%** in estimating dimensions and was successfully implemented in a production environment at TATA Motors, Jamshedpur. The tool not only replaced manual inspection but also ensured consistent quality checks without human intervention.

### Visual Demonstration
Below are the images showcasing the results:

#### Image 1: Chassis with F1 and F2 Marking
<div class="text-center">
    {% include figure.liquid path="assets/img/P1_1.jpg" title="Chassis with Marked Points F1, F2, F3, and F4" class="img-fluid rounded z-depth-1" %}
</div>

#### Image 2: Detection Overlay
<div class="text-center">
    {% include figure.liquid path="assets/img/P1_2.jpg" title="Corner Detection Overlay" class="img-fluid rounded z-depth-1" %}
</div>

#### Image 3: Dimensional Mapping
<div class="text-center">
    {% include figure.liquid path="assets/img/P1_3.jpg" title="Dimensional Mapping Visualization" class="img-fluid rounded z-depth-1" %}
</div>

### Challenges and Future Work

#### Challenges
- Calibrating low-resolution cameras to provide high-precision outputs.
- Managing lighting variations and noise in the live visual feed.



