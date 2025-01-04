---
layout: page
title: AI-Enhanced Robotic Manipulation Using RL
description: Leveraging DDPG, HER, and PER for efficient robotic pick-and-place tasks.
img: assets/img/P2_1.jpg
importance: 3
category: Undergraduate
related_publications: false
---

### Introduction
The project aimed to develop and deploy reinforcement learning (RL) algorithms for robotic pick-and-place operations in industrial environments. The focus was on enabling a six-degree-of-freedom robotic arm to learn and adapt to unstructured environments through combinations of Deep Deterministic Policy Gradient (DDPG), Hindsight Experience Replay (HER), and Prioritized Experience Replay (PER).

### Approach
The task was simulated in the MuJoCo environment, where combinations of RL algorithms were tested for efficiency. The experiments evaluated:
1. **DDPG with HER and PER:** Integrated prioritized sampling with hindsight experience replay to enhance learning efficiency.
2. **Batch Size and Nodes:** Investigated the effect of varying batch sizes and neural network configurations on convergence rates and performance.

The deployment involved:
- Training the robotic arm for 4000 episodes with a batch size of 128.
- Evaluating the trained model's ability to achieve precise pick-and-place operations.

### Results
#### Quantitative Metrics:
- The combination of **DDPG+HER+PER** resulted in the most stable learning, but required slightly longer training times due to sampling weight computation.
- Using **DDPG+HER** alone achieved faster convergence but struggled with edge cases.
- Larger batch sizes (256) outperformed smaller ones (128) in terms of convergence speed and stability.

### Performance Metrics
#### Observations:
- **DDPG+HER+PER** demonstrated the best success rate of **91.2%** after 2500 epochs.
- Training with larger batch sizes reduced convergence time by **~30%** compared to smaller batches.
- The robotic arm learned smooth and efficient pick-and-place trajectories, outperforming simpler RL methods.

The table below summarizes the results of different reinforcement learning algorithm combinations:

| **Algorithm Combination** | **Convergence Time (epochs)** | **Final Success Rate (%)** |
|----------------------------|-------------------------------|-----------------------------|
| DDPG                      | 2000                          | 74.3                        |
| DDPG+HER                  | 1800                          | 85.6                        |
| DDPG+HER+PER              | 2500                          | 91.2                        |

---

### Visual Demonstration
#### Images: MuJoCo Simulation Environment
<div class="text-center">
    {% include figure.liquid path="assets/img/P2_1.jpg" title="Simulated MuJoCo Environment for Training" class="img-fluid rounded z-depth-1" %}
</div>
<div class="text-center">
    {% include figure.liquid path="assets/img/P2_2.jpg" title="Optimal Pick-and-Place Trajectory Learned by the Robotic Arm" class="img-fluid rounded z-depth-1" %}
</div>

### Link to Publication
[[Click here](https://www.sciencedirect.com/science/article/abs/pii/S0360835224002274)]



