---
layout: page
title: Projective Geometry, Rectification
description: Exploring affine rectification, metric rectification, and planar homography for vision-based tasks.
img: assets/img/g51.png
importance: 6
category: Graduate
related_publications: false
---

### Affine Rectification
Affine rectification restores the parallelism of lines that appear skewed due to perspective distortion. The homography matrix \( H \) was computed to achieve this transformation.

#### Steps:
1. **Find Points at Infinity**:
   - Parallel lines were identified, and their intersections calculated to determine points at infinity.
   - The vanishing line was computed using:
     $$ l'_{\infty} = \text{cross}(P_{\infty 1}, P_{\infty 2}) $$

2. **Affine Rectification Homography**:
   - Constructed \( H \) to restore parallelism:
     $$ H = \begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ l_1 & l_2 & l_3 \end{bmatrix} $$

#### Visualization:
<div class="text-center">
    {% include figure.liquid path="assets/img/GA1/chess1_affine_rect.png" title="Affine Rectification Output" class="img-fluid rounded z-depth-1" %}
</div>
<div class="text-center">
    {% include figure.liquid path="assets/img/GA1/facade_affine_rect.png" title="Affine Rectification Output" class="img-fluid rounded z-depth-1" %}
</div>

---

### Metric Rectification
Metric rectification further refines the affine transformation to restore both parallelism and orthogonality.

#### Key Concepts:
1. **Circular Points at Infinity**:
   - The remaining distortion after affine rectification is captured by the conic at infinity \( C_{\infty} \):
     $$ C_{\infty} = H \cdot C'_{\infty} \cdot H^T $$

2. **Perpendicular Line Constraints**:
   - Enforced using:
     $$ l'^T C'_{\infty} m' = 0 $$

3. **Homography Matrix**:
   - Computed using SVD to derive eigenvalues and eigenvectors, yielding the final transformation matrix.

#### Visualization:
<div class="text-center">
    {% include figure.liquid path="assets/img/GA1/final_metric_rect.png" title="Metric Rectification Output" class="img-fluid rounded z-depth-1" %}
</div>
<div class="text-center">
    {% include figure.liquid path="assets/img/GA1/chess1_metric_rect.png" title="Affine Rectification Output" class="img-fluid rounded z-depth-1" %}
</div>

---

### Planar Homography
Planar homography computes a \( 3 \times 3 \) matrix \( H \) to map points between two planes based on correspondences.

#### Steps:
1. **Homography Equation**:
   $$ X' = H \cdot X $$

2. **Constraints Using Point Correspondences**:
   - Derived the matrix \( A \) from correspondences:
     $$ A \cdot h = 0 $$

3. **Solve Using SVD**:
   - Resolved \( A \) to compute \( H \), transforming images accurately.

#### Visualization:
<div class="text-center">
    {% include figure.liquid path="assets/img/GA1/homography.png" title="Planar Homography Result" class="img-fluid rounded z-depth-1" %}
</div>

---

### Metric Rectification from Perpendicular Lines
To directly achieve metric rectification, perpendicular line constraints were used to populate the matrix \( A \), ensuring geometric consistency.

#### Visualization:
<div class="text-center">
    {% include figure.liquid path="assets/img/GA1/checker1_Direct_rect copy.png" title="Direct Metric Rectification Output" class="img-fluid rounded z-depth-1" %}
</div>

---

### Applications of Homography
Planar homography was extended to multiple images for applications such as perspective overlays and wall blending.

#### Visualization:
<div class="text-center">
    {% include figure.liquid path="assets/img/GA1/input_hom_multi.jpeg" title="Input Images to be warped and overlaid" class="img-fluid rounded z-depth-1" %}
</div>

<div class="text-center">
    {% include figure.liquid path="assets/img/GA1/blended_image.jpg" title="Blended Homography Output" class="img-fluid rounded z-depth-1" %}
</div>
