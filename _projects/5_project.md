---
layout: page
title: Diffusion Model for Action Anticipation
description: Leveraging advanced visual learning techniques to enhance perception systems.
img: assets/img/g601.png
importance: 5
category: Graduate
related_publications: false
---

### Project Description
The Visual Learning and Recognition (VLR) project explored the integration of state-of-the-art visual learning techniques into perception systems for enhanced scene understanding and decision-making. The primary objective was to bridge the gap between classical computer vision approaches and modern deep learning-based solutions.

---

### Key Objectives
1. **Enhanced Scene Understanding**:
   - Developed a pipeline for action recognition, segmentation, and temporal analysis using Convolutional Neural Networks (CNNs).
   - Incorporated feature fusion techniques to improve temporal data understanding.

2. **Robust Learning Framework**:
   - Experimented with transfer learning to leverage pre-trained models for activity recognition tasks.
   - Fine-tuned models specifically for datasets focusing on structured activities.

3. **Efficient Model Deployment**:
   - Optimized the learning pipeline for real-time inference.
   - Explored various model compression techniques to reduce latency without compromising accuracy.

---

### Dataset: 50Salads
1. **Overview**:
   - The 50Salads dataset was used for this project. It comprises 50 video sequences of people preparing mixed salads, annotated with action labels for each frame.
   - Includes annotations for both high-level and fine-grained activities, making it ideal for evaluating action recognition and temporal segmentation tasks.

2. **Preprocessing**:
   - Videos were resized and normalized to ensure uniformity in input data.
   - Data augmentation techniques, such as cropping and rotation, were applied to increase model robustness.

---

### Methodology
1. **Data Acquisition and Pre-Processing**:
   - Processed the 50Salads dataset to extract meaningful spatiotemporal features.
   - Applied normalization and augmentation to improve generalization.

2. **Model Design**:
   - Employed a combination of CNNs and Recurrent Neural Networks (RNNs) for feature extraction and temporal modeling.
   - Used pre-trained CNN backbones for initial feature extraction and trained RNNs to capture temporal dependencies.

3. **Training and Validation**:
   - Used cross-entropy loss for action classification and temporal segmentation tasks.
   - Validated the model's performance using frame-wise accuracy and F1 scores on the test set.

4. **Deployment**:
   - Focused on efficient inference pipelines for low-latency action recognition.
   - Evaluated the deployment on simulated environments with diverse lighting and activity conditions.

---

### Applications
The VLR framework has potential applications in:
- Human activity recognition for assistive robotics.
- Video surveillance and monitoring systems.
- Enhancing human-computer interaction for smart devices.

---

### Summary
The Visual Learning and Recognition project demonstrated the feasibility of using deep learning techniques on the 50Salads dataset to achieve robust action recognition and segmentation. The modular architecture ensures scalability and adaptability for diverse applications in human activity understanding.