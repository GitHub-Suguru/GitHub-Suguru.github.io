---
title: "Adaptive UAV Swarm Autonomy: Reinforcement Learning-Driven REconfiguration of Environment-Aware Virtual Rigid-Body Formations"
excerpt: "Multi-UAV VRB formation self-reconfiguration via environment-aware curriculum-based hierarchical reinforcement learning with temporal smoothness penalties. <br/><img src='/images/vrb_rl_snapshot.png'>"
collection: portfolio
permalink: /portfolio/vrb_rl_reconfig/
date: 2025-12-21
---

## Summary
This project investigates **adaptive autonomy for UAV swarms** by integrating **reinforcement learning (RL)** with the **Virtual Rigid Body (VRB) formation framework** to enable **environment-aware, self-reconfigurable multi-agent behavior**. The goal is to allow UAV formations to autonomously adjust their **shape, size, and orientation** in response to environmental constraints such as narrow passages, obstacles, and mission-dependent objectives, while preserving formation coherence and collision-free motion.

The framework leverages **curriculum-based hierarchical reinforcement learning** augmented with **temporal smoothness penalties**, enabling the swarm to learn structured reconfiguration strategies that are both efficient and dynamically feasible. The work targets scalable deployment in complex environments and serves as a stepping stone toward safe integration of learning-based autonomy with model-based control architectures.

## What I build / contributed
I designed and implemented the **learning-enabled VRB reconfiguration framework**, including:
- Developing a **curriculum-based hierarchical RL architecture** that decomposes long-horizon swarm navigation into sequential subtasks (path planning followed by formation reconfiguration).
- Designing **state and action representations** that encode formation geometry, scale, and orientation within the VRB framework.
- Implementing **temporal smoothness penalties** to discourage abrupt or unnecessary formation changes, promoting physically plausible and stable swarm behavior.
- Integrating **potential-based reward shaping** to improve learning convergence in large and constrained environments.
- Demonstrating **autonomous formation adaptation** in narrow, medium, and wide corridors, including both 2D and extended 3D environments with tunnels.
- Building a **simulation-ready pipeline** compatible with future integration of UAV dynamics, MPC-based safety layers, and ROS2–PX4 workflows.
- Laying the groundwork for **safe RL–MPC hybrid autonomy**, where learning enhances decision-making while model-based control enforces stability and constraint satisfaction.

## Why this matters
- **Real environments are constrained and unpredictable**, making fixed UAV formation strategies brittle and difficult to scale.
- This work enables **intelligent, environment-aware formation reconfiguration** by integrating reinforcement learning with the Virtual Rigid Body framework.
- The approach learns when and how to adapt formations, balancing **efficiency, collision avoidance, and formation stability** without hand-tuned rules.
- It advances **deployable swarm autonomy**, bridging learning-based adaptability with structured, model-compatible control architectures.

## Current status and outlook


## Links
