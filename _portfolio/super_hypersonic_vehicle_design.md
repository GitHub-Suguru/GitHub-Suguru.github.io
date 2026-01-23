---
title: "Benchmark Study of Charles Lindbergh's Transatlantic Flight in Supersonic and Hypersonic Speed Regimes"
excerpt: "Designs of supersonic and hypersonic tech demonstrators for transatlantic flight inspired by Charles Lindbergh's first ever transatlnantic flight. <br/><img src='/images/Mach3_vehicle.png'>"
collection: portfolio
permalink: /portfolio/supersonic_hypersonic_demonstrator/
date: 2023-06-08
---

## Summary
This project presents a conceptual benchmark study of supersonic and hypersonic airbreathing vehicles capable of completing Charles Lindbergh’s historic transatlantic flight at cruise speeds ranging from Mach 2 to Mach 7. Using a unified parametric sizing methodology based on Hypersonic Convergence, six minimum-capability demonstrator vehicles were synthesized to investigate how key aircraft design parameters scale with cruise Mach number. The study provides quantitative correlations between Mach number and vehicle size, weight, volume, and slenderness, offering physically grounded starting points for future high-speed aircraft conceptual design.

## What I build / contributed
I served as "Chief Engineer and Synthesis Lead", responsible for integrating multidisciplinary analyses into a unified conceptual design framework. My primary contributions included:
- Leading the "overall system-level synthesis" of geometry, propulsion, aerodynamics, structures, and mission performance across Mach 2–7 vehicles.
- Developing and implementing the "Hypersonic Convergence–based parametric sizing workflow", including convergence logic and solution-space generation.
- Defining "design selection criteria" and supervising the selection of representative design-point vehicles from each solution space.
- Coordinating "cross-disciplinary consistency" between weight, volume, thrust-to-weight, wing loading, and trajectory analyses.
- Performing and interpreting "Mach-scaling trend analyses" for key aircraft parameters (TOGW, planform area, wetted area, volume, OEW, and slenderness).
- Contributing to "verification activities", including SR-71 benchmark validation.
- Co-authoring the technical documentation and figures used in the final paper.

## Methods
The study employed a "parametric (preliminary) sizing process derived from Hypersonic Convergence", a multidisciplinary conceptual design methodology that simultaneously enforces weight and volume closure, a critical requirement for high-speed vehicles with large fuel fractions.

Key methodological elements included:
- Mission definition based on Lindbergh’s transatlantic flight ($$ \approx 6,000 $$ km range, single pilot, minimal payload).
- Airbreathing blended-body flying-wing configuration with hydrocarbon fuel to simplify storage and integration.
- Iterative numerical solution of coupled weight and volume budget equations, converged through planform area iteration.
- Generation of solution-space carpet plots across structural index ($$ I_{str} $$) and slenderness ($$ \tau $$)ranges for each cruise Mach number.
- Constraint enforcement using approach wing loading limits and mission-segment thrust-to-weight requirements.
- Trajectory-based fuel fraction estimation, combining empirical climb models and the Breguet range equation.
- Verification of the methodology through SR-71 Blackbird reproduction, ensuring physical credibility of the sizing process.

## Results
- Viable solution spaces were generated for six vehicles (Mach 2–7), each satisfying mission and constraint requirements.
- Vehicle size, weight, volume, and wetted area increased from Mach 2 to Mach 5, then plateaued or decreased beyond Mach 5, indicating a shift in dominant design drivers.
- The slenderness parameter ($$ \tau $$) reached a minimum near Mach 5, highlighting a geometric transition between supersonic and hypersonic regimes.
- Fuel fraction increased monotonically with Mach number, driving the growth of higher-Mach vehicles.
- Wing loading limits required increasing $$ C_{L,max} $$ assumptions at Mach 5–7 to enable feasible design point selection.
- The resulting Mach-scaling trends provide physically interpretable correlations that can be reused as starting estimates in future high-speed conceptual design studies.

## Links
