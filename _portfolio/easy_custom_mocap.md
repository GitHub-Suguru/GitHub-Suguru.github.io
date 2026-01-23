---
title: "Off-the-shelf Webcam-Based Easy Custom Mocap from Scratch"
excerpt: "Complete step-by-step description of off-the-shelf webcam-based custom motion capture system suitable for MAV and UGV applications."
collection: portfolio
permalink: /portfolio/easy_custom_mocap/
date: 2025-05-03
---

## Summary
This project presents an accurate, **cost-effective, and easy-to-implement indoor motion capture system** designed for uncrewed vehicle systems (UVS), with particular emphasis on micro aerial vehicles and small ground robots. The system leverages off-the-shelf hardware, multi-camera triangulation, and optimal estimation techniques to provide reliable 3D position tracking without reliance on expensive commercial motion capture infrastructure. By combining kinematics-based triangulation with weighted least squares (WLS) fusion and Kalman filtering, the framework achieves millimeter- to centimeter-level accuracy suitable for control, estimation, and autonomy research in GPS-denied environments.

## What I build / contributed
I independently designed, implemented, and experimentally validated the complete motion capture system, including:
- Architecting a four-camera indoor motion capture setup using low-cost webcams and active infrared (IR) LED markers.
- Designing optimal camera placement to minimize triangulation error based on convergence-angle analysis.
- Implementing multi-view geometry algorithms, including camera calibration, projection modeling, epipolar geometry, correspondence resolution, and triangulation.
- Developing a weighted least squares (WLS) fusion framework that dynamically weights triangulated position estimates based on reprojection and depth error characteristics.
- Designing and tuning Kalman Filter (KF) and Unscented Kalman Filter (UKF) pipelines to improve temporal consistency, noise suppression, and robustness to measurement dropout.
- Integrating MATLAB-based camera calibration with a Python-based processing backend using OpenCV.
- Conducting experimental validation using a CrazyFlie micro aerial vehicle and a custom-built rover platform.
- Analyzing estimator performance under ideal conditions and camera occlusion scenarios.

## Methods
The proposed system follows a multi-stage estimation pipeline combining geometric reconstruction and stochastic filtering:
- **Hardware setup**:
  - Four calibrated webcams with IR-pass filtering.
  - Active IR LED markers mounted in known configurations on the vehicle.
  - Off-the-shelf tripods and USB infrastructure to minimize cost and complexity.
<p align="center">
  <img src="/images/camera_open.png" width="25%"><br>
  <em>Figure 1.</em> Webcam with IR-pass filter (floppy disk film) - camera open configuration for calibration
</p>
<p align="center">
  <img src="/images/crazyFlie_iso.jpg" width="25%"><br>
  <em>Figure 2.</em> Modified CrazyFlie micro drone with active IR-marker for motion capturing  
</p>
<p align="center">
  <img src="/images/env_config.png" width="30%"><br>
  <em>Figure 3.</em> Environment configuraiton.
</p>

- **Camera modeling and geometry**:
  - Intrinsic and extrinsic calibration using MATLAB’s camera calibration toolbox.
  - Projection modeling and epipolar geometry to resolve multi-camera correspondence.

- **Triangulation and fusion**:
  - Independent triangulation from each camera pair using epipolar line.
  - Depth-dependent accuracy analysis using reprojection error models.
  - Weighted least squares fusion to optimally combine triangulated position estimates.
<p align="center">
  <img src="/images/cam_diagram.png" width="40%"><br>
  <em>Figure 4.</em> Multi-camera geometry and triangulation schematic.
</p>
    
- **State estimation**:
  - Constant velocity model to increase the generalizability of the system.
  - Kalman filtering for noise suppression and state prediction.
  - Unscented Kalman filtering to handle nonlinearities and marker occlusion.
 
- **Software stack**:
  - MATLAB for calibration and parameter extraction.
  - Python and OpenCV for real-time image processing and estimation.
<p align="center">
  <img src="/images/python_env.jpg" width="40%"><br>
  <em>Figure 5.</em> Python environment.
</p>

## Results
- Achieved millimeter- to centimeter-level position accuracy in occlusion-free indoor environments.
- Demonstrated that simple averaging across camera pairs already yields high accuracy, while WLS provides a principled confidence-weighted fusion framework.
- Showed that both KF and UKF significantly reduce measurement noise, keeping estimation errors largely within $$ 3 \sigma $$ bounds.
- In occlusion scenarios:
  - UKF outperformed standard KF, maintaining better trajectory continuity during temporary measurement loss.
- Validated the system experimentally using real flight data from a CrazyFlie micro drone, confirming suitability for real-world UVS testing (still need improvement).
- Identified clear paths for future improvement, including automated calibration, IMU fusion, and multi-object tracking.

<p align="center">
  <img src="/images/mocap_raw_data.png" width="40%"><br>
  <em>Figure 6.</em> Position estimation through Kalman Filtering.
</p>

<p align="center">
  <img src="/images/kf.png" width="40%"><br>
  <em>Figure 6.</em> Position estimation through Kalman Filtering.
</p>

<p align="center">
  <img src="/images/ukf.png" width="40%"><br>
  <em>Figure 7.</em> Position estimation through Unscented Kalman Filtering.
</p>

## Links
