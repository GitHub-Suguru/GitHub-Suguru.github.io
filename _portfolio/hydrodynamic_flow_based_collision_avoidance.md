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
I designed and implemented the full **3D hydrodynamic-based collision avoidance framework** and its integration with formation control:

- Developed a **3D doublet and ellipsoidal manifold flow model** for dynamic obstacle representation
- Derived the induced velocity field from **Laplace’s equation for incompressible, irrotational flow**
- Implemented real-time **velocity field superposition for multiple moving obstacles**
- Designed a **proportional velocity-tracking controller** to follow induced flow streamlines
- Integrated the avoidance strategy with a **Virtual Rigid Body (VRB) formation framework**
- Implemented:
  - Constraint-force formulation using Lagrange multipliers
  - Baumgarte stabilization for rigidity enforcement
  - Optimal slot allocation for formation geometry realization
- Synthesized:
  - Hydrodynamic avoidance
  - Slot control
  - Constraint forces
  - Gravity compensation
  - Quadcopter dynamics mapping (thrust & attitude commands)
- Conducted extensive simulations including:
  - Single UAV avoidance
  - Multi-UAV VRB formations
  - Moving obstacles
  - Noisy obstacle measurements processed via Kalman filtering

## Technical Highlights

### 1: Hydrodynamic Flow-Based Obstacle Modeling
- Obstacles modeled as:
  - **3D doublets**
  - **Ellipsoidal (Rankine oval–based) manifolds**
- Flow potential satisfies:
  - Laplace’s equation (harmonic function)
  - Incompressible & irrotational assumptions
- Benefits:
  - No local minima (unlike artificial potential fields)
  - No trajectory discontinuities
  - Smooth streamline-following behavior
  - Real-time computational efficiency

---

### 2: Virtual Rigid Body (VRB) Formation Framework
- Ensures formation rigidity via:
  - \( 3N - 6 \) distance constraints (3D rigidity condition)
- Constraint forces computed using:
  - Jacobian-based formulation
  - Lagrange multipliers
  - Baumgarte stabilization
- Optimal slot allocation:
  - Minimizes total agent travel distance
  - Ensures desired geometry & orientation

---

### 3: Unified Control Architecture

Total commanded control input:

\[
\mathbf{f}_{i,cmd} = \mathbf{f}_{i,h} + \mathbf{f}_{i,s} + \mathbf{f}_{i,g} + \mathbf{f}_{i,c}
\]

Where:
- \( \mathbf{f}_{i,h} \) — Hydrodynamic induced velocity tracking
- \( \mathbf{f}_{i,s} \) — Slot allocation control
- \( \mathbf{f}_{i,g} \) — Gravity compensation
- \( \mathbf{f}_{i,c} \) — Constraint force (rigidity enforcement)

This architecture enables:
- Local obstacle avoidance
- Formation preservation
- Smooth cooperative motion
- No explicit trajectory replanning

---
## Key Results

### Single UAV
- Smooth avoidance of stationary & moving obstacles
- Adjustable clearance via doublet radius \( R_d \)
- Robust performance under Gaussian measurement noise
- Minimum clearance maintained safely above buffer threshold

### Eight-UAV Delta Formation
- Formation rigidity preserved during avoidance
- Inter-agent distances asymptotically return to desired values
- Local collision avoidance inside formation inherently achieved via constraint forces
- Robust under noisy obstacle measurements

### Emergent Dynamic Obstacles
- No predictive obstacle modeling required
- Avoidance purely reactive yet physically interpretable
- Computationally lightweight compared to MPC-based approaches

---
## Why This Matters

Traditional collision avoidance methods suffer from:

- ❌ Local minima (potential fields)
- ❌ High computational cost (MPC)
- ❌ Heavy reliance on prediction accuracy
- ❌ Limited interpretability (RL-based methods)

This hydrodynamic approach provides:

- ✔ Physics-inspired behavior
- ✔ Real-time feasibility
- ✔ No trajectory replanning
- ✔ Natural streamline motion
- ✔ Formation-level coordination
- ✔ Scalability to multi-UAV swarms

This framework is particularly suited for:

- UAV swarm navigation in cluttered environments
- Defense and surveillance operations
- Urban air mobility traffic deconfliction
- Cooperative autonomous aerial robotics
- Future drone-as-first-responder (DFR) systems

---

## Media and Publications

- 🎥 Supplemental simulation videos:  
  [https://youtu.be/QcZWW4lSVJo](https://youtu.be/QcZWW4lSVJo)

- 🎥 Multi-formation simulation playlist:  
  [https://www.youtube.com/playlist?list=PLX7ZK_42SnIBaYop_a6Q5GKgtBj6kfUKp](https://www.youtube.com/playlist?list=PLX7ZK_42SnIBaYop_a6Q5GKgtBj6kfUKp)

- 📄 AIAA Conference Paper:  
  Sato & Subbarao, *Three-Dimensional Hydrodynamic Flow-Based Collision Avoidance for UAV Formations Facing Emergent Dynamic Obstacles*  
  American Institute of Aeronautics and Astronautics (AIAA)

---

## Tools and Technologies

- **Languages:** MATLAB, Python
- **Simulation:** Custom 3D dynamics simulator
- **Control:** PID outer/inner loop control
- **Estimation:** Kalman Filtering (constant velocity model)
- **Mathematics:**  
  - Laplace’s equation  
  - Potential flow theory  
  - Lagrange multipliers  
  - Baumgarte stabilization  
  - Rigid-body dynamics  
- **Formation Control:** Virtual Rigid Body (VRB)
- **Visualization:** 3D flow field & trajectory visualization

---

## Future Work

- Integration into **ROS2–Gazebo SITL**
- Hardware-in-the-loop validation
- Replacement of PID velocity tracking with **Model Predictive Control**
- Extension to:
  - Adaptive doublet strength tuning
  - Non-spherical obstacle manifolds
  - Outdoor RTK-enabled experiments
  - Multi-swarm interaction

---

