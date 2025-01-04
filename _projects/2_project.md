---
layout: page
title: Geometric Context in Visual Localization
description: Enhancing camera pose estimation with geometric consistency for robust visual localization.
img: assets/img/g20.png
importance: 2
category: Graduate
related_publications: false
---

### Project Description
This project focuses on improving the accuracy of visual localization for autonomous navigation by leveraging geometric priors. The objective was to refine camera pose estimation using multi-view geometric consistency, ensuring robustness in adverse environmental conditions. Our approach built upon the Accelerated Coordinate Encoding (ACE) model, incorporating additional loss functions for enhanced performance while maintaining computational efficiency.

### Approach
#### 1. Baseline Model
- The ACE model was used as the backbone for its efficient 3D coordinate regression capabilities.
- It comprises:
  - A pre-trained convolutional neural network backbone for feature extraction.
  - A scene-specific multilayer perceptron (MLP) head to predict 3D coordinates.

#### 2. Loss Functions
To enhance the localization performance, we introduced and optimized the following loss functions:

- **Reprojection Loss:**
  The reprojection loss ensures accurate camera pose predictions by minimizing the error between the predicted and ground-truth 2D points when projected back to the image plane.
  $$\ell_r(\mathbf{x}_i, \mathbf{y}_i, \mathbf{p}_i) = 
  \begin{cases} 
  \epsilon_r(\mathbf{x}_i, \mathbf{y}_i), & \text{if valid}, \\
  \|\mathbf{y}_i - \bar{\mathbf{y}}_i\|^2, & \text{if invalid}.
  \end{cases}$$
  Here:
  - $$ \mathbf{x}_i$$ and $$\mathbf{y}_i $$ are the ground-truth and predicted 2D coordinates.
  - $$ \epsilon_r $$ is a clamped robust error function to mitigate outliers.

  The clamped error function is defined as:
  $$\epsilon_r = \min(\|\mathbf{x}_i - \mathbf{y}_i\|, \tau),$$
  where $$\tau$$ is a dynamic threshold.

- **Relative Pose Error Loss:**
  This loss enforces geometric consistency by penalizing deviations in the predicted relative camera poses.
  $$\ell_{\text{pose}} = \| \mathbf{t}_{ij}^{\text{gt}} - \mathbf{t}_{ij} \|^2 + R_{\text{err}}(\mathbf{R}_{ij}^{\text{gt}}, \mathbf{R}_{ij})^2,$$
  where:
  - $$\mathbf{t}_{ij}$$ and $$\mathbf{R}_{ij}$$ are the predicted translation and rotation.
  - $$R_{\text{err}}$$ computes the rotational error between predicted and ground-truth rotations.

---

### Visualization of Results
Below are side-by-side comparisons of the vanilla ACE model and our improved implementation for visual localization.

#### Pair 1: Scene 1
<div class="row">
  <div class="col-sm-6 text-center">
    {% include figure.liquid path="assets/img/seq1_bad.jpg" title="Vanilla ACE - Scene 1" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-6 text-center">
    {% include figure.liquid path="assets/img/seq1_good.png" title="Improved ACE - Scene 1" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

#### Pair 2: Scene 2
<div class="row">
  <div class="col-sm-6 text-center">
    {% include figure.liquid path="assets/img/seq2_bad.png" title="Vanilla ACE - Scene 1" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-6 text-center">
    {% include figure.liquid path="assets/img/seq2_good.png" title="Improved ACE - Scene 1" class="img-fluid rounded z-depth-1" %}
  </div>
</div>

#### Pair 3: Scene 3
<div class="row">
  <div class="col-sm-6 text-center">
    {% include figure.liquid path="assets/img/seq3_bad.png" title="Vanilla ACE - Scene 1" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-6 text-center">
    {% include figure.liquid path="assets/img/seq3_good.png" title="Improved ACE - Scene 1" class="img-fluid rounded z-depth-1" %}
  </div>
</div>