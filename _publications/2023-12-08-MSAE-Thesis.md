---
title: "A Rigid Body Framework For Modeling and Simulation of Formation of Autonomous Agents"
collection: publications
category: manuscripts
permalink: /publication/2023-MSAE-Thesis
excerpt: 'This thesis develops a Virtual Rigid Body (VRB) framework that models a formation of autonomous agents as nodes of a rigid body, enabling collision-free formation establishment, maintenance, reconfiguration, and station-keeping through constraint forces and 6-DOF dynamics. The framework integrates rigorous mathematical modeling, control law design (including LQR), and extensive simulations to demonstrate scalable and robust formation control for multi-agent systems'
date: 2023-12-08
venue: 'The University of Texas at Arlington - Mechanical and Aerospace Engineering'
paperurl:
citation: 'Sato, Suguru, "A RIGID BODY FRAMEWORK FOR MODELING AND SIMULATION OF FORMATION OF AUTONOMOUS AGENTS" (2023). <i>Mechanical and Aerospace Engineering Theses. </i> 1020.
https://mavmatrix.uta.edu/mechaerospace_theses/1020'
---

## Link to the Paper
- [Publisher version (UTA)](https://mavmatrix.uta.edu/mechaerospace_theses/1020/)

## Abstract
Formation motion, wherein multiple agents operate within close proximity while maintaining precise relative positions and coordinated movements has a significant impact in the realm of Uncrewed Aerial Systems (UAS). Formation establishment, and station-keeping have been critical research areas as several missions can be conceived, and accomplished by groups of “simple” autonomous agents. Advances in this research have led to multiple advantages in areas such as reconnaissance, aerospace exploration, map building, search and rescue, etc. particularly, if the formation motion is inspired by nature and natural phenomena such as flock of birds, school of fish, hydrodynamics (smooth streamlines), magnetic fields, and electrical charges. In such formulations, the formation motion is often captured by a few rules, which are collision avoidance, velocity matching, and flock centering. Besides the examples seen in nature, our research is motivated by the characteristics of a rigid body. By considering the autonomous agents as fixed nodes on a rigid body, the trajectory of each agent on the rigid body is automatically determined based on the behavior and motion of the rigid body itself. Therefore, there is no need to design their trajectories individually. Moreover, since distances between agents are held constant, collision free trajectories are automatically determined. We call this a Virtual Rigid Body (VRB) formation as there is no physical rigid connection between agents, and the virtual rigidity between agents is accomplished via constraint forces. The main contributions of this research are thorough mathematical modeling, control law development, and simulation of this VRB framework for formation motion. The thesis synthesizes the 6-DOF equations of motion associated with the framework for an arbitrary number of autonomous agents. Reference motion is prescribed for the aggregated rigid body – velocity of the center of mass and the angular velocity. Using these and the rigid body structure specification, local trajectories are calculated to perform the formation establishment. The thesis also develops local control laws for each agent using linear quadratic control methods, designed to ensure formation establishment, and station-keeping. Extensive simulations within an artificial environment are performed to illustrate the effectiveness of the modeling framework. Several candidate situations are considered such as – formation establishment, reconfiguration, re-orientation, and station-keeping.

## Contribution
This thesis introduces a unified Virtual Rigid Body (VRB) modeling framework that rigorously represents multi-agent formations using rigid-body dynamics and constraint forces, enabling consistent treatment of translation, rotation, and internal formation constraints in 3D space. It derives the associated equations of motion and control laws (including LQR-based regulation) to achieve collision-free formation acquisition, maintenance, reconfiguration, and station keeping, and validates the approach through comprehensive simulations demonstrating scalability, robustness, and applicability to coordinated autonomous systems.

## Supplemental Material
