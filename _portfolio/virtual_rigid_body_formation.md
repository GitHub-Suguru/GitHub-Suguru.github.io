---
title: "Modeling and Simulation of Virtual Rigid Body Formations and their applications using Multiple Air Vehicles"
excerpt: "A physics-informed multi-UAV formation framework that enforces rigid-body behavior through stabilizing inter-agent constraints. | [Publisher Page](https://doi.org/10.2514/6.2024-2016) | [Archive](https://doi.org/10.48550/arXiv.2601.11788)"
collection: portfolio
permalink: /portfolio/vrb_formation/
date: 2024-01-04
---

## Summary
This project presents a **physics-informed Virtual Rigid Body (VRB) formation control framework** for coordinating multiple UAVs by enforcing rigid-body–like distance constraints among agents. By modeling a UAV formation as a virtual rigid structure, the framework enables coordinated translation, rotation, reconfiguration, and station keeping without explicit leader–follower hierarchies or preplanned individual trajectories. The approach is validated through extensive MATLAB/Simulink simulations across single- and multi-waypoint missions with formations ranging from three to eight UAVs.



## What I build / contributed
I designed and implemented the entire VRB formation control framework, including:
- Developing a **constraint-force–based formation formulation** inspired by rigid-body mechanics.
- Deriving **inter-agent distance constraints** and synthesizing stabilizing constraint forces using:
  - d’Alembert’s principle of virtual work
  - Lagrange multipliers
  - Baumgarte stabilization for asymptotic constraint enforcement
- Deriving full **6-DOF equations of motion** for a multi-UAV system that embed constraint forces directly into the dynamics.
- Implementing **formation-level translational and rotational dynamics**, including center-of-mass motion and angular momentum evolution.
- Designing a **body-frame attachment strategy** for arbitrary formation geometries.
- Implementing an **input decoupling algorithm** to distribute rigid-body–level force and torque commands to individual UAVs.
- Integrating **LQR-based local trajectory tracking controllers** for each agent.
- Building a **MATLAB/Simulink simulation pipeline** to validate formation establishment, reconfiguration, reorientation, and waypoint tracking.
- Performing scalability studies for formations of **2–8 UAVs** with varying geometries (scalable to more agents).

## Methods
- The framework models a UAV formation as a **Virtual Rigid Body** by enforcing a minimal set of inter-agent distance constraints (3N–6 for N agents in 3D space). Constraint forces are synthesized using **constraint Jacobians and Lagrange multipliers**, ensuring that relative distances converge asymptotically to their desired values.
- To maintain numerical stability and robustness against imperfect initial conditions, **Baumgarte stabilization** is incorporated, resulting in a PID-like constraint feedback structure. The multi-agent system’s **translational and rotational equations of motion** are derived by aggregating agent dynamics about the formation center of mass.
- Formation orientation is represented using **quaternions to avoid kinematic singularities**. Desired formation motion—specified in terms of center-of-mass position, velocity, orientation, and angular rates—is mapped to individual UAV inputs via an **input decoupling matrix**. Each agent tracks its assigned trajectory using an **LQR feedback controller**, allowing the formation to behave dynamically as a single rigid body.

## Results
- Successfully demonstrated **formation establishment and stabilization** for multiple geometries and number of agents of choice, including
  - Accurate convergence of formation center-of-mass position and velocity
  - Stable formation orientation and angular rates
  - Constraint satisfaction throughout the maneuver
- Demonstrated **multi-waypoint missions** in cluttered environments with:
  - Formation reconfiguration prior to narrow passages
  - Formation reorientation and retrieval
  - Continuous enforcement of inter-agent distance constraints
- Verified scalability with increased number of agents with stable performance despite changes in formation inertia during reconfiguration.

## Links
