# Rider-Helmet-Detection
This project utilizes deep learning models YOLOv8 and VGG16 for real-time helmet detection in two-wheeler riders, aiming to improve traffic safety by automating law violator detection. It integrates computer vision to segment riders and classify helmet usage, achieving high accuracy in crowded environments.
# 🪖 Rider Helmet Detection using YOLOv8 + VGG16

[![Conference](https://img.shields.io/badge/Accepted%20Paper-ICCIT%202024-blue)]([https://ieeexplore.ieee.org/](https://ieeexplore.ieee.org/document/11022569))
[![Roboflow Dataset](https://img.shields.io/badge/Dataset-Roboflow-green)]([https://universe.roboflow.com/dip-project-8u3bl/segmentation_dip](https://app.roboflow.com/rider-and-helmet-instance-segmentation-and-detection))

This repository contains the full implementation of the **automated motorcycle rider and helmet detection system**, developed using **YOLOv8** for rider segmentation and **VGG16** for helmet classification.

The research was accepted and published in:

> 📄 **Enhancing Road Safety and Accountability Through Automated Rider and Helmet Detection: A Deep Learning Approach**  
> *27th International Conference on Computer and Information Technology (ICCIT 2024), IEEE*  
> [View Paper (IEEE Xplore)](10.1109/ICCIT64611.2024.11022569) 

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
<img width="644" height="821" alt="Screenshot 2025-07-19 111113" src="https://github.com/user-attachments/assets/67b78607-7f98-45af-9ca1-2b7e4aba90b1" />

## 📊 Model Evaluation
The following results are derived from the experimental evaluation conducted in the accepted ICCIT 2024 paper.

| Metric         | YOLOv8 Evaluation Result |
|----------------|---------------------------|
| mAP            | 95%                       |
| Precision      | 99%                       |
| Recall         | 96%                       |
| PR Curve AUC   | 95%                       |
| F1 Score       | 95% @ IoU 0.77            |

**Key Insights:**
- The **YOLOv8** model performs highly reliably in segmenting two-wheeler riders in traffic scenarios.
- The **F1 Score** of 0.95 (at 77% IoU threshold) indicates excellent balance between precision and recall.
- **Precision-Recall (PR) curve** suggests strong model confidence and minimal false positives.

These results demonstrate the robustness of YOLOv8 in real-world conditions for rider detection.
## 📈 Comparative Model Evaluation

| Author/Model                 | mAP  | Precision | Recall |
|-----------------------------|------|-----------|--------|
| Nandhini (SSD)              | 78.1%| –         | –      |
| Tomas (YOLOv5 + YOLOv7)     | 95%  | 95.6%     | 91%    |
| Venkateswarlu (YOLOv8)      | –    | 88.63%    | 68.3%  |
| Aboah (YOLOv8 + TTA)        | 95.3%| 91.8%     | –      |
| **Ours (YOLOv8 + VGG16)**   | **95%** | **99%** | **96%** |

