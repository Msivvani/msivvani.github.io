---
layout: page
title: BEV-Perception for Precise Autonomous Parking
description: Developing a teleoperation system with Bird’s-Eye View visualization for precise vehicle navigation and parking.
img: assets/img/g10.jpg
importance: 1
category: Graduate
related_publications: false
---

### Problem Statement
The PERCIV project addresses a critical inefficiency in car manufacturing plants: the manual transportation of vehicles from production lines to storage facilities. Current methods rely heavily on human drivers, resulting in significant labor costs, time inefficiencies, and safety concerns. PERCIV seeks to replace this approach with a teleoperation system that leverages external perception to enable precise vehicle navigation and parking, reducing operational bottlenecks.

### System Implementation
#### Bird’s-Eye View (BEV) Generation
- **Experimentation with Inverse Perspective Mapping (IPM):** 
  - Evaluated IPM for generating BEV from individual camera images.
  - Determined that a homography-based planar transformation on a stitched image provided higher fidelity for visualization.
- **Final BEV Implementation:**
  - Stitched multiple camera feeds using a graph-based neural network optimized for feature-sparse environments.
  - Transformed stitched images into BEV using homography for an intuitive top-down view.

#### Object Detection and Localization
- Integrated a custom YOLO model to detect and localize the target vehicle in the BEV.
- Fused camera data with odometry using an Extended Kalman Filter (EKF) for enhanced localization accuracy.
- Achieved a mean average precision (mAP) of **97.5%** for vehicle localization against ground truth measured using ArUco markers.

#### UI/UX Design
- Designed a user interface using Streamlit and ReactJS for seamless teleoperation and waypoint-based control.
- Key features:
  - Real-time BEV visualization with trajectory overlays.
  - Speedometer, gear status, and safety alerts.
  - Support for multi-car control and intuitive navigation.

#### Image and Video Demonstrations
##### Image 1: Stitched BEV of the Scene
<div class="text-center">
    {% include figure.liquid path="assets/img/g11.png" title="Stitched BEV of the Scene" class="img-fluid rounded z-depth-1" %}
</div>

##### Image 2: Final BEV Visualization
<div class="text-center">
    {% include figure.liquid path="assets/img/g12.png" title="Final BEV Visualization with Overlays" class="img-fluid rounded z-depth-1" %}
</div>

##### Image 3: UI/UX Interface
<div class="text-center">
    {% include figure.liquid path="assets/img/g13.png" title="UI/UX Interface with Real-Time Updates" class="img-fluid rounded z-depth-1" %}
</div>

##### Video: PERCIV in Action
<div class="text-center">
    <video controls class="img-fluid rounded z-depth-1" preload="metadata" width="600" height="400">
        <source src="/assets/video/perciv_demo.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
    <div class="caption mt-2">
        Demonstration of PERCIV Teleoperation System.
    </div>
</div>

### Results
- **Performance Metrics:**
  - Update frequency: **10 Hz**, ensuring real-time visualization and control.
  - Successful parking detection: **80%**, adhering to specified tolerance limits.
  - Vehicle speed: **10 cm/s**, allowing smooth navigation.
- **Final Performance:**
  - Demonstrated teleoperation and waypoint-based autonomous control with high reliability.
  - Successfully showcased precise vehicle parking and obstacle avoidance during the Final Validation Demonstration (FVD).
