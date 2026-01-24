---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

Education
======
* Ph.D in Aerospace Engineering, University of Texas at Arlington, 2027 (expected)
* M.Sc. in Aerospace Engineering, University of Texas at Arlington, 2023
* B.Sc. in Aerospace Engineering, University of Texas at Arlington, 2022

Research experience
======
* **Spring 2026**: Graduate Research Assistant
* **Summer 2025, Summer 2024, Summer 2023**: Research Assistant
  
Skills
======
* **Guidance, Navigation, and Control (GNC)**:
  * UAV flight dynamics and simulation
  * Classical & modern control
  * Multi-UAV systems, distributed control, formation flight
  * Physics-inspired Collision avoidance
  * Optimization and estimation
* **Robotics & Autonomous Systems**:
  * Multi-UAV systems and distributed control
  * Vision-guided tracking and landing
  * Motion capture–based state feedback (custom multi-camera systems)
  * Sensor fusion
* **Simulation & Software Frameworks**:
  * ROS2
  * PX4 Autopilot (SITL, multi-vehicle simulation)
  * Gazebo, jMAVSim
  * MATLAB/Simulink (UAV Toolbox, custom dynamics & controllers)
* **Perception & Machine Learning**:
  * Computer vision
  * Deep learning for perception (YOLO, etc.)
  * Reinforcement learning fundamentals
* **Programming & Tools**:
  * Python, PyTorch, OpenAI Gymnasium, MATLAB, C/C++
  * Git/GitHub
  * Linux (Ubuntu)
  * SolidWorks, OpenVSP (for aircraft design)
* **Experimental & Research Skills**:
  * Software-in-the-loop (SITL) testing
  * Algorithm validation through simulation and real-time experiments
  * Technical writing, peer-reviewed publications, conference presentations

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
<!--  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  -->
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Service and leadership
======
* [UTA Aerospace Systems Laboratory](https://asl.uta.edu/) lab manager
