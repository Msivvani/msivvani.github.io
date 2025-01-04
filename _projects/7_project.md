---
layout: page
title: 3D Modeling of NITT Clock Tower with NeRF
description: Deploying NeRF for 3D modeling of the NITT clock tower from drone-captured images.
img: assets/img/P5_1.jpg
importance: 1
category: Undergraduate
related_publications: false
---

### Introduction
Neural Radiance Fields (NeRF) have revolutionized 3D modeling by enabling high-fidelity renderings of complex structures. This project focused on deploying NeRF to model the iconic NITT clock tower using images captured via a drone. The process utilized volumetric rendering techniques to synthesize accurate and visually stunning 3D models.

#### Image 1: Dataset of Drone-Captured Images
<div class="text-center">
    {% include figure.liquid path="assets/img/P5_1.jpg" title="Dataset of Drone-Captured Images of NITT Clock Tower" class="img-fluid rounded z-depth-1" %}
</div>

### Approach
1. **Dataset Collection:**
   - Captured 49 high-resolution images (4000x2250 pixels) of the NITT clock tower using a DJI Mini drone.
   - Images were inward-facing, ensuring comprehensive coverage of the structure from multiple perspectives.

2. **Neural Radiance Fields (NeRF):**
   - NeRF uses a multi-layer perceptron (MLP) architecture to map a 5D input vector $$[x, y, z, \theta, \phi]$$ to RGB color $$[r, g, b]$$ and opacity $$\alpha$$.
   - The volumetric rendering equation is given by: <br />
     $$ C(r) = \int_{t_n}^{t_f} T(t) \sigma(r(t)) c(r(t), d) , dt $$ <br />
     where: $$ T(t) = \exp\left(-\int_{t_n}^{t} \sigma(r(s)) , ds\right) $$ <br />
     Here, $$C(r)$$ represents the expected color of the camera ray that passes through the scene.

   - The network was optimized using gradient descent to minimize the difference between rendered views and the original images.

3. **3D Modeling Process:**
   - Utilized COLMAP for feature extraction, correspondence search, and incremental structure-from-motion reconstruction.
   - The reconstructed 3D point cloud from COLMAP was refined by NeRF, which added color and density information for rendering.

#### Image 2: 3D Model of NITT Clock Tower
<div class="text-center">
    {% include figure.liquid path="assets/img/P5_2.jpg" title="3D Model of NITT Clock Tower Using NeRF" class="img-fluid rounded z-depth-1" %}
</div>

### Results
- The 3D model demonstrated high fidelity, capturing intricate details of the NITT clock tower.
- Training on a NVIDIA Tesla P100 GPU with a 32GB VRAM took approximately 3.5 hours, including 25 epochs of training and 1 hour for rendering.
- The final 3D model can be explored interactively, providing insights into the structure's geometry and visual features.

