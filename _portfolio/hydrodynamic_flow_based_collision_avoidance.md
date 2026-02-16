---
title: "Three-dimensional Hydrodynamic Flow-Based Collision Voidance for UAV Formations"
excerpt: "Physics-inspired 3D hydrodynamic flow-based collision avoidance framework for single and multi-UAV Virtual Rigid Body (VRB) formations operating in dynamic environments. Smooth, real-time avoidance without trajectory replanning | [AIAA SciTech Paper](https://arc.aiaa.org/doi/abs/10.2514/6.2024-2016) | [Simulation Videos](https://www.youtube.com/playlist?list=PLX7ZK_42SnIBaYop_a6Q5GKgtBj6kfUKp)"
collection: portfolio"
collection: portfolio
permalink: /portfolio/hydro_oa/
date: 2026-01-15
---

## Summary
This project presents a **three-dimensional hydrodynamic flow-based collision avoidance framework** for both single UAVs and multi-UAV formations operating in dynamic environments.

Instead of explicitly replanning trajectories or predicting long-horizon obstacle motion, **emergent obstacles are modeled as 3D doublets or ellipsoidal manifolds** that generate local velocity fields derived from Laplace’s equation. UAVs follow these induced streamlines, naturally executing **smooth, continuous, and collision-free maneuvers** without trajectory discontinuities.

To preserve coordinated motion in multi-agent systems, this flow-based avoidance strategy is integrated with a **Virtual Rigid Body (VRB) formation framework**, enabling UAV formations to maintain geometry and rigidity while maneuvering around moving obstacles.

The work demonstrates a **real-time, interpretable, and computationally lightweight alternative** to MPC- and learning-based avoidance approaches.

<p align="center">
  <img src="/images/doublet_flow.png" width="55%"><br>
  <em>Figure 1.</em> Velocity field visualization around a 3D doublet (hydrodynamic obstacle model).
</p>

<p align="center">
  <img src="/images/single_vehicle_avoidance.png" width="55%"><br>
  <em>Figure 2.</em> Single UAV avoiding stationary and moving obstacles while tracking a predefined trajectory.
</p>

<p align="center">
  <img src="/images/vrb_delta_formation.png" width="55%"><br>
  <em>Figure 3.</em> Eight-UAV Virtual Rigid Body (VRB) delta formation establishment and maintenance.
</p>

<p align="center">
  <img src="/images/vrb_hydro_combined.png" width="55%"><br>
  <em>Figure 4.</em> Eight-UAV VRB formation performing coordinated hydrodynamic-based avoidance against moving obstacles.
</p>

---

## What I build / contributed


## Methods


## Results


## Links
