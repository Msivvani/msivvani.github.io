---
layout: page
title: Visually Guided Motion Planning
description: Leveraging dense 3D reconstruction and 6D pose estimation for precision robotic grasping.
img: assets/img/P4_2.jpg
importance: 2
category: Undergraduate
related_publications: false
---

### Introduction
This project aimed to enhance the precision and reliability of robotic grasping tasks by integrating vision-based motion planning. By leveraging dense 3D reconstruction and real-time 6D pose estimation, the system optimized grasp point estimation and improved robotic arm performance.

#### Image 1: Dataset of Objects for Reconstruction
<div class="text-center">
    {% include figure.liquid path="assets/img/P4_1.jpg" title="Dataset of 900+ Images for 3D Reconstruction" class="img-fluid rounded z-depth-1" %}
</div>

### Approach
1. **Data Collection and Reconstruction:**  
   - Curated a dataset of 900+ images using an Intel RealSense D435 depth camera.
   - Performed dense 3D reconstruction of the scene using Structure-from-Motion (SfM) and Multi-View Stereo (MVS) techniques.
   - Created a detailed 3D model of the target scene for subsequent pose estimation.

#### Image 2: Dense 3D Reconstruction of the Scene
<div class="text-center">
    {% include figure.liquid path="assets/img/P4_2.jpg" title="Dense 3D Reconstruction of the Scene" class="img-fluid rounded z-depth-1" %}
</div>

2. **6D Pose Estimation and Motion Planning:**
   - Utilized the Deep Object Pose Estimation model to compute the real-time 6D pose of objects.
   - Integrated vision-driven motion generation to optimize grasping precision by detecting the optimal grasp points for the robotic arm.

#### Image 3: Processed 3D Mesh of the Target Object
<div class="text-center">
    {% include figure.liquid path="assets/img/P4_3.jpg" title="Processed 3D Mesh of the Target Object for 6D Pose Estimation" class="img-fluid rounded z-depth-1" %}
</div>

### Results
- Achieved precise 6D pose estimation of objects in real time.
- Enhanced grasping precision by **8%** using the Franka robotic arm, improving efficiency and accuracy in motion planning tasks.
- Validated the system’s performance across multiple real-world scenarios, showcasing its robustness and adaptability.


