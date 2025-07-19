# Rider-Helmet-Detection
This project utilizes deep learning models YOLOv8 and VGG16 for real-time helmet detection in two-wheeler riders, aiming to improve traffic safety by automating law violator detection. It integrates computer vision to segment riders and classify helmet usage, achieving high accuracy in crowded environments.
# 🪖 Rider Helmet Detection using YOLOv8 + VGG16

[![Conference](https://img.shields.io/badge/Accepted%20Paper-ICCIT%202024-blue)](https://ieeexplore.ieee.org/)
[![Roboflow Dataset](https://img.shields.io/badge/Dataset-Roboflow-green)](https://universe.roboflow.com/dip-project-8u3bl/segmentation_dip)

This repository contains the full implementation of the **automated motorcycle rider and helmet detection system**, developed using **YOLOv8** for rider segmentation and **VGG16** for helmet classification.

The research was accepted and published in:

> 📄 **Enhancing Road Safety and Accountability Through Automated Rider and Helmet Detection: A Deep Learning Approach**  
> *27th International Conference on Computer and Information Technology (ICCIT 2024), IEEE*  
> [View Paper (IEEE Xplore)](https://ieeexplore.ieee.org/document/XXXXX) *(coming soon)*

---

## 📌 Project Overview

This project tackles road safety concerns by automatically detecting two-wheeler riders and verifying helmet compliance using a dual-stage deep learning pipeline:

1. **YOLOv8** – Segments riders from real-world traffic images  
2. **VGG16** – Classifies cropped segments as *with helmet* or *without helmet*

---

## 📁 Dataset Overview

- **Total Images:** 3,301 (after augmentation)
- **Classes:** `Rider With Helmet`, `Rider Without Helmet`
- **Format:** YOLOv8
- **Prepared Using:** [Roboflow](https://roboflow.com)

### 🔗 Dataset Access:
👉 [segmentation_dip - Roboflow](https://universe.roboflow.com/dip-project-8u3bl/segmentation_dip)

---

## 🧠 Model Architecture

