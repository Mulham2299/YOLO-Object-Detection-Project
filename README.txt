# YOLOv3 vs YOLOv8: Object Detection on Custom Vehicle Dataset 🚗📦

## 📌 Project Overview
This project compares the performance of two deep learning–based object detection models — **YOLOv3 (pre-trained)** and **YOLOv8 (custom-trained)** — using a custom vehicle dataset. Developed as part of my second-year Computer Vision module at Northumbria University, the goal was to evaluate detection accuracy, precision, and recall across both models and understand how architecture and training strategies affect real-world performance.

## 🧠 Key Objectives
- Train YOLOv8 from scratch using Ultralytics on a custom dataset (6 vehicle classes)
- Evaluate YOLOv3 using pre-trained weights on the same dataset
- Compare performance metrics: mAP@0.5, precision, recall
- Analyze architectural differences, training workflows, and ethical implications

## 📊 Results Summary

| Metric       | YOLOv3 (Pre-trained) | YOLOv8 (Custom-trained) |
|--------------|----------------------|--------------------------|
| mAP@0.5      | 0.08                 | 0.95                     |
| Precision    | 0.10                 | 0.93                     |
| Recall       | 0.12                 | 0.89                     |

YOLOv8 significantly outperformed YOLOv3 due to anchor-free architecture, advanced loss functions (CIoU, DFL, VFL), and dataset-specific training.

## 🏗️ Model Architecture Highlights
- **YOLOv3**: Darknet-53 backbone, anchor-based detection, Leaky ReLU activation
- **YOLOv8**: CSP-Darknet backbone, anchor-free detection, SiLU activation, mosaic augmentation

## 🧪 Training Details
- **YOLOv8** trained for 50 epochs on Google Colab using Ultralytics
- Dataset split: 1435 training images, 649 validation images
- Loss functions: CIoU, DFL, VFL
- Validation after each epoch to prevent overfitting

## 📁 Repository Structure