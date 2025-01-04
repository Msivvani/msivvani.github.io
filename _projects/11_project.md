---
layout: page
title: Automated Estimation of Choroidal Thickness
description: Developing a semi-automated tool to estimate sub-foveal choroidal thickness (SFChT) for pathological myopia prognostics.
img: assets/img/P3_1.jpg
importance: 5
category: Undergraduate
related_publications: true
---

### Introduction
Pathological myopia is a progressive condition affecting millions worldwide. Sub-foveal choroidal thickness (SFChT) has emerged as a crucial biomarker for prognostics. This project aimed to develop a semi-automated tool that accurately measures SFChT using fundus images, reducing the need for manual interventions and enabling clinician-friendly diagnostics.

#### Image 1: Fundus Image of the Eye
<div class="text-center">
    {% include figure.liquid path="assets/img/P3_1.jpg" title="Fundus Image with Key Choroidal Features" class="img-fluid rounded z-depth-1" %}
</div>

#### Image 2: Annotated Fundus Image Highlighting SFChT
<div class="text-center">
    {% include figure.liquid path="assets/img/P3_2.jpg" title="Annotated Fundus Image Showing SFChT" class="img-fluid rounded z-depth-1" %}
</div>

### Approach
The estimation of SFChT required advanced image processing techniques for accurate identification of key features within the fundus images:
1. **Data Preparation:**  
   Optical biometry datasets from myopic subjects at Sankara Nethralaya, Tamilnadu, India, were preprocessed using Gaussian filters and dilation operations to enhance input quality.
   
2. **Measurement Process:**
   - Key choroidal features (anterior corneal and choroidal peaks) were manually selected using an interactive graphical interface.
   - Pixel distances between the peaks were computed and scaled using the known axial length of the eye.
   - Zhang’s calibration method ensured high accuracy in the scaling process.

### GUI for SFChT Estimation
To streamline the measurement process, a user-friendly graphical user interface (GUI) was developed. The GUI enabled clinicians to interactively mark peaks and obtain accurate measurements instantly.

#### Image 3: GUI for SFChT Estimation
<div class="text-center">
    {% include figure.liquid path="assets/img/P3_GUI.jpg" title="Semi-Automated GUI for SFChT Estimation" class="img-fluid rounded z-depth-1" %}
</div>

### Results
The semi-automated tool demonstrated high precision, producing measurements that closely matched manual estimations. The framework was successfully validated using datasets of myopic subjects, paving the way for its application in clinical settings.

### Link to Publication
[Placeholder for publication link]
