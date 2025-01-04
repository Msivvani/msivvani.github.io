---
layout: page
title: SuperPoint Features in Visual-Inertial SLAM
description: Integrating SuperPoint features into the VINS framework for robust and repeatable keypoint detection.
img: assets/img/g401.png
importance: 3
category: Graduate
related_publications: false
---

### Project Description
This project focused on enhancing Simultaneous Localization and Mapping (SLAM) performance by integrating SuperPoint features into the VINS framework. The goal was to improve the robustness and repeatability of feature detection, particularly in challenging visual environments. By replacing the baseline VINS feature detector with SuperPoint, the system achieved superior localization accuracy and reliability.

---

### Key Contributions
1. **Integration of SuperPoint:**
   - SuperPoint, a deep learning-based keypoint detector and descriptor, was integrated into the VINS pipeline to replace the classical feature detector.
   - Improved robustness in detecting keypoints under challenging conditions such as low light, repetitive patterns, and motion blur.

2. **Keypoint Detection and Matching:**
   - SuperPoint provided higher repeatability and robustness in keypoint matching across frames.
   - Enhanced feature matching accuracy, leading to improved pose estimation and reduced drift.

3. **Seamless Integration:**
   - Modified the VINS framework to support real-time operation with SuperPoint, ensuring compatibility with existing system modules.

---

### Visualization
#### Comparison of Feature Detectors
Below is a comparison of keypoints detected on the same scene using the baseline VINS feature detector (a) and SuperPoint (b). SuperPoint extracts more robust and repeatable keypoints, especially in challenging regions.

<div class="row">
  <div class="col-sm-6 text-center">
    {% include figure.liquid path="assets/img/prep1.jpg" title="Baseline VINS Feature Detector" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-6 text-center">
    {% include figure.liquid path="assets/img/prep2.jpg" title="SuperPoint Feature Detector" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

#### SuperPoint Integrated with VINS
The image below illustrates the working of the SLAM system with SuperPoint integrated into the VINS framework.

<div class="text-center">
    {% include figure.liquid path="assets/img/r1.png" title="SLAM with SuperPoint Integrated into VINS" class="img-fluid rounded z-depth-1" %}
</div>

---

### System Implementation
1. **SuperPoint Integration:**
   - Integrated SuperPoint into the VINS pipeline, replacing the classical feature detector and descriptor.
   - Optimized the system for real-time operation without compromising computational efficiency.

2. **Feature Matching and Pose Estimation:**
   - Used SuperPoint’s keypoints and descriptors for accurate matching across frames.
   - Improved pose estimation by leveraging high-quality feature matches, reducing drift in long trajectories.

3. **Testing and Validation:**
   - Validated the system in various challenging environments, demonstrating improved robustness and reliability in feature detection and SLAM performance.

---

### Summary
By integrating SuperPoint into the VINS framework, this project successfully enhanced SLAM performance, especially in visually challenging scenarios. The integration demonstrated the potential of deep learning-based feature detectors to significantly improve traditional SLAM systems.

