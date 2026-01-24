---
title: "Vision-Guided Tracking and Landing of a UAV on a Moving Target via Minimum-Jerk Trajectories"
excerpt: "Vision-based UAV tracking and autonomous landing on a moving target using minimum-jerk trajectory planning. This project is a part of University of Texas at Arlington (UTARI) Maverick Autonomous Vehicle Research Center (MAVRC) grand opening celemony demonstration project | [UTARI MAVRC Link](https://utari.uta.edu/research/maverick-autonomous-vehicle-research-center/) | [Media News](https://www.nbcdfw.com/news/local/uta-drone-testing-facility/3919383/)"
collection: portfolio
permalink: /portfolio/rover_docking/
date: 2025-09-15
---

## Summary
This project presents a **vision-guided autonomy framework for tracking and landing a quadrotor UAV on a moving ground target**, combining perception, trajectory optimization, and control within a unified ROS2-based architecture. The system leverages **minimum-jerk trajectory generation** to ensure smooth, dynamically feasible UAV motion during target tracking and descent, enabling robust interaction between aerial and ground vehicles.

The framework is developed and validated in a **high-fidelity ROS2–Gazebo simulation environment** to be demonstrated at the UTA Research Institute MAVRC grand opening ceremony.

## What I build / contributed
I designed and implemented the end-to-end perception–planning–control pipeline, including:
- Developing **vision-based moving target detection and tracking**, using both:
  - **ArUco fiducial markers** for reliable pose estimation
  - **A custom-trained YOLOv8** model for learning-based target detection
- Designing a **minimum-jerk trajectory planner** to generate smooth reference trajectories for UAV tracking and landing
- Integrating perception outputs with **real-time trajectory replanning** for moving-target interception
- Building a **ROS2–Gazebo SITL environment** for UAV–ground vehicle interaction
- Implementing state feedback and command interfaces compatible with **PX4 offboard control**

## Technical highlights
- **Vision-based perception**
  - ArUco-based pose estimation for precise relative localization
  - YOLOv8 deep-learning detection for robustness to appearance and lighting changes
- **Trajectory planning**
  - Minimum-jerk polynomial trajectories for smooth position, velocity, and acceleration profiles
  - Continuous replanning to accommodate target motion
- **Control and autonomy**
  - Hierarchical architecture separating perception, planning, and control
  - Designed for seamless integration with PX4 offboard flight modes
- **Simulation and validation**
  - ROS2–Gazebo SITL with moving ground vehicle
  - Designed to scale from simulation to motion-capture-based physical experiments

## Why this matters
- Autonomous landing on moving targets is a **critical capability for logistics, recovery, and cooperative robotics**, including applications such as:
  - UAV–UGV cooperative operations
  - Autonomous package pickup and delivery
  - Precision landing in GPS-denied environments
  - Defense and inspection missions requiring mobile recovery platforms
 
By combining **vision-driven perception** with **minimum-jerk trajectory optimization**, this work demonstrates **a smooth, reliable, and hardware-ready solution** suitable for real-world deployment.

## Media and results
- Simulation video (minimum-jerk trajectory): [https://youtu.be/gZGSd9E3WjE?si=lUK6Q3aT11XOrXCT](https://youtu.be/gZGSd9E3WjE?si=lUK6Q3aT11XOrXCT)
- Simulation video (constant descending rate): [https://youtu.be/Bvyj0yh63Vw?si=WYRdmoDmtPWL4Tw7](https://youtu.be/Bvyj0yh63Vw?si=WYRdmoDmtPWL4Tw7)
  
## Tools and technilogies
- **Languages & libraries**: Python, OpenCV, PyTorch
- **Robotics middleware**: ROS2
- **Autonomy stack**: PX4 offboard control
- **Simulation**: Gazebo
- **Perception**: ArUco, YOLOv8, Monocular camera
- **Planning**: Minimum-jerk trajectory optimization

