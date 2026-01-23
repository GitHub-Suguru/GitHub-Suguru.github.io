---
title: "Optimal Thruster Configuration for 6-DOF Control of A Small Satellite"
excerpt: "Analyses on the minimum and optimal number of thrusters that support 6-DOF control of a small satellite - Presented at ASC (Astrodynamics Specialist Conference) 2025. | [Publisher Page] | [Archive](https://doi.org/10.48550/arXiv.2601.11802)"
collection: portfolio
permalink: /portfolio/optimal_thruster/
date: 2025-08-15
---

## Summary
This paper investigates the **optimal thruster configuration problem for achieving full six-degree-of-freedom (6-DOF) control** of a small cubic satellite using only unidirectional thrusters. Starting from a symmetric 24-thruster baseline, the study develops a systematic algorithm to identify **viable and thrust-efficient thruster layouts** that enable complete translational and rotational control. The proposed framework demonstrates that while **seven thrusters are sufficient for theoretical 6-DOF controllability**, a **12-thruster configuration provides an optimal balance** between control authority, thrust efficiency, and mission performance during rendezvous and docking operations.

<p align="center">
  <img src="/images/rpo_snap1.png" width="25%"><br>
  <em>Figure 1.</em> Satellite rendezvous and proximity operation snapshot 1.
</p>

<p align="center">
  <img src="/images/rpo_snap2.png" width="25%"><br>
  <em>Figure 2.</em> Satellite rendezvous and proximity operation snapshot 2.
</p>

<p align="center">
  <img src="/images/rpo_snap3.png" width="25%"><br>
  <em>Figure 3.</em> Satellite rendezvous and proximity operation snapshot 3.
</p>

## What I build / contributed
I developed the end-to-end thruster configuration optimization and control framework, including:
- Formulating the **6-DOF force–torque allocation model** for a cubic satellite with multiple surface-mounted thrusters.
- Deriving the **control allocation matrix** that maps individual thruster forces to net forces and torques.
- Designing a **heuristic search algorithm** to:
  - Enumerate feasible thruster combinations.
  - Enforce rank-6 controllability conditions.
  - Respect unidirectional thruster constraints via nonnegative least squares.
- Defining **viable** and **optimal configuration groups** based on controllability and minimum total thrust effort.
- Identifying the **minimum thruster count (7)** and the **optimal thruster count (12)** for practical missions.
- Integrating the optimized thruster layouts into a **6-DOF rendezvous and docking control framework**.
- Implementing a **linear time-varying Model Predictive Control (MPC)** scheme for coupled translational and rotational guidance.
- Conducting comparative simulations across **7–24 thruster configurations** to evaluate performance, efficiency, and robustness.

<p align="center">
  <img src="/images/seven_config.png" width="25%"><br>
  <em>Figure 4.</em> Seven-thruster configuraiton (minimum number of thrusters)
</p>

<p align="center">
  <img src="/images/twelve_config.png" width="25%"><br>
  <em>Figure 5.</em> Twelve-thruster configuraiton (optimal number of thrusters)
</p>

## Methods
- The satellite is modeled as a rigid body operating in Low Earth Orbit, with dynamics separated into **translational motion** (modeled using the Tschauner–Hempel equations in the LVLH frame) and **relative rotational motion** (represented using quaternions and angular velocity dynamics). Individual thruster forces are mapped to net forces and torques through a geometry-dependent control **allocation matrix**.
- Thruster configuration optimization is performed offline using a **combinatorial search** over candidate thruster subsets. For each candidate configuration, the allocation matrix is reconstructed and tested for:
  - Rank-6 controllability.
  - Ability to generate all positive and negative unit forces and torques.
  - Feasibility under **nonnegative least-squares optimization**.
- Among all viable configurations, the optimal set is selected by minimizing the total thrust required to generate the full set of unit force and torque commands.
- For mission validation, the selected configurations are embedded into an **MPC-based 6-DOF rendezvous and docking controller**, which enforces thruster bounds, smooth thrust profiles, and terminal docking constraints while tracking position and attitude references.

## Results
- Confirmed that **7 unidirectional thrusters** are the minimum required for full 6-DOF controllability, consistent with theoretical results.
- Demonstrated that a **12-thruster configuration** minimizes total thrust effort while maintaining strong control authority.
- Showed that configurations with fewer than 12 thrusters exhibit:
  - Longer docking times
  - Higher total impulse
  - Increased oscillatory behavior
- Verified through rendezvous-docking simulations that:
  - The 12-thruster configuration reduces docking time by over **15%** compared to the 7-thruster case.
  - Total impulse is reduced by nearly **50%** relative to the minimum configuration.
- Observed smoother thrust distribution and lower angular velocity RMS for configurations with **12 or more thrusters**.
- Identified clear trade-offs between **hardware redundancy, fuel efficiency, and control smoothness**, supporting the 12-thruster layout as a practical design choice.

<p align="center">
  <img src="/images/eight_config.png" width="25%"><br>
  <em>Figure 6.</em> Eight-thruster configuraiton.
</p>

<p align="center">
  <img src="/images/nine_config.png" width="25%"><br>
  <em>Figure 7.</em> Nine-thruster configuraiton.
</p>

<p align="center">
  <img src="/images/ten_config.png" width="25%"><br>
  <em>Figure 8.</em> Ten-thruster configuraiton.
</p>

<p align="center">
  <img src="/images/eleven_config.png" width="25%"><br>
  <em>Figure 9.</em> Eleven-thruster configuraiton.
</p>

## Links
[Publisher Page]
[Archive](https://doi.org/10.48550/arXiv.2601.11802
