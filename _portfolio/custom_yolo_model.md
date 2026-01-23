---
title: "Custom YOLOv8 Model Training and Deployment"
excerpt: "Complete step-by-step description of custom YOLOv8 model training and deployment. <br/><img src='/images/val_batch0_pred.jpg'>"
collection: portfolio
permalink: /portfolio/custom_yolo_model/
date: 2025-07-25
---

## Summary
This project provides a complete, beginner-friendly pipeline for training, validating, and deploying a custom YOLOv8 object detection model using the Ultralytics framework in Python. Starting from raw image collection, the repository walks through dataset preparation, annotation, model fine-tuning, and evaluation, with a focus on practical usability and reproducibility. While demonstrated on a single-class object (e.g., a rover), the workflow is fully extensible to multi-class detection tasks and real-world robotics and perception applications. The similar process can be applied for the new versions of YOLO.

<br/><img src='/images/val_batch0_pred.jpg'>

## What I build / contributed
I designed and implemented the **entire end-to-end training and deployment workflow**, including:
- Developing a **structured, step-by-step training pipeline** for fine-tuning the YOLOv8 nano model (`yolov8n.pt`) on custom datasets.
- Creating **data collection and preprocessing utilities**, including scripts for video-based data acquisition and automated dataset splitting.
- Establishing **a clear dataset organization standard** (YOLO-format images, labels, and YAML configuration).
- Providing **reproducible installation and environment setup instructions** for Ubuntu-based systems.
- Implementing **training, testing, and inference scripts** for images, prerecorded videos, and live camera streams.
- Documenting **common failure modes and debugging strategies** (e.g., missing labels, incorrect paths, annotation issues).
- Reporting and interpreting **quantitative detection metrics** (mAP, precision, recall, inference speed).

## Methods
The repository follows a supervised deep learning–based object detection pipeline using transfer learning:
- **Model architecture**: YOLOv8 nano (lightweight, real-time capable).
- **Training strategy**: Fine-tuning from pretrained weights to accelerate convergence and reduce data requirements.
- **Data preparation**:
  - Image extraction from video streams.
  - Manual bounding-box annotation using LabelImg in YOLO format.
  - Dataset split into training, validation, and test subsets.
- **Training configuration**:
  - Adjustable hyperparameters (epochs, batch size, image resolution, device).
  - CPU- and GPU-compatible execution.
- **Evaluation**:
  - Mean Average Precision (mAP@50).
  - Precision–recall curves and confusion matrices.
  - Inference speed benchmarking on CPU/GPU.
All steps are modular, allowing the pipeline to be adapted for different datasets, object classes, or deployment targets.

## Results
- Achieved **high detection accuracy** on a custom single-class dataset (~500 images), with:
  - **mAP@50 $$ \approx 0.99 $$**
  - **Precision $$ \approx 1.0 $$**
  - **Recall $$ \approx 0.95 $$**
- Demonstrated **real-time inference capability**:
  - $$ \tilde $$ 20–70 FPS on CPU (hardware dependent)
  - Higher performance on GPU-enabled systems
- Successfully validated the trained model on:
  - Static images
  - Prerecorded videos
  - Live camera streams
- Produced a **reproducible, extensible reference implementation** suitable for robotics perception, autonomous systems, and research prototyping.

## Links
