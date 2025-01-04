---
layout: page
title: "SimplySort: Autonomous Book Shelf Organiser"
description: Developing autonomous manipulation capabilities for robotic arm with perception, planning, and control integration.
img: assets/img/g30.png
importance: 4
category: Graduate
related_publications: false
---

### Project Description
This project focused on the development of autonomous manipulation capabilities for robotic arm, integrating perception, planning, and control subsystems. The objective was to enable a robotic arm to navigate complex environments while avoiding obstacles and efficiently reaching predefined goals.

### System Overview
The system architecture included:
1. **Perception Subsystem:**
   - Used a stereo camera for depth estimation and object detection.
   - Integrated real-time obstacle detection using a pre-trained YOLO model.

2. **Planning Subsystem:**
   - Implemented a local planner using the Dijkstra algorithm for optimal pathfinding.
   - Utilized a global planner for long-range navigation goals, considering dynamic and static obstacles.

3. **Control Subsystem:**
   - Designed a Proportional-Integral-Derivative (PID) controller for smooth trajectory following.
   - Incorporated velocity scaling to ensure safety in dynamic environments.

### Results
The system demonstrated reliable autonomous navigation in various test environments, showcasing the integration of perception and planning pipelines with real-time control. Key features included robust obstacle avoidance and efficient goal-reaching behaviors.

---

### Video Demonstration
Below is a video showcasing the autonomous manipulation and control capabilities of the system.

<div class="text-center">
    <video controls class="img-fluid rounded z-depth-1" preload="metadata" width="600" height="400">
        <source src="/assets/video/rauto.mp4" type="video/mp4">
        Your browser does not support the video tag.
    </video>
    <div class="caption mt-2">
        Demonstration of Autonomous Manipulation and Control.
    </div>
</div>
