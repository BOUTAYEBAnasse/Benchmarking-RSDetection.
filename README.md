# 🛰 Remote Sensing Object Detection Benchmark

This repository contains the data and resources required for the comparative evaluation of the best-performing object detection models on SAR and optical remote sensing images.

<div align="center" style="border: 2px solid black; padding: 10px; background-color: #f8f8f8;">
    <img src="assets/GITHUB_COVER.PNG" alt="Description du graphique" width="650">
</div>

## 🎯️ Deformable-DETR model

**Reference article**: [“Deformable DETR: Deformable Transformers for End-to-End Object Detection”](https://arxiv.org/abs/2010.04159), Zhu et al., 2020.

**Deformable DETR** is an improved version of DETR model, designed for more efficient and accurate object detection. It introduces deformable attention to focus on relevant regions while reducing computational cost and incorporates multi-scale feature processing, making it particularly effective for detecting small objects and accelerating training convergence.

**Deformable-DETR Architecture**
<div align="center" style="border: 2px solid black; padding: 10px; background-color: #f8f8f8;">
    <img src="assets/Deformable-DETR.png" alt="Description du graphique" width="800">
</div>

## 📊 Notebooks for Benchmarking 

This repository contains benchmarking notebooks for each dataset. For both **Pleiades Aircraft Dataset** and **SSDD Dataset**, the following models are implemented:
- **Deformable DETR** (Zhu et al., 2021)
- **DETR** (Carion et al., 2020)
- **YOLO V10** (Redmon et al., 2016)
- **RetinaNet** (Lin et al., 2017)
- **Faster R-CNN** (Ren et al., 2015)
  
---
## 📁 Repository Structure

The proposed notebooks contain implementations of each model, one notebook for each model and dataset, 10 in all.
---
## 🗺️ Data to be used

This Google Drive link **[Google Drive Link](https://drive.google.com/drive/folders/1-8UDTKH-A7PerjXUXKDAXtTWKYRdj7IS?usp=sharing)** contains all the resources required to execute this project. The available resources include two datasets, Optical and SAR, using to train, validate and test the models presented.
   
---

## ▶️ Execution Instructions

To execute these notebooks, use **Google Colab** with a **GPU environment**. For optimal performance, it's recommended to use an **NVIDIA A100 GPU**.

---

## 🧪 Testing Phase 

The testing phase includes:
1. Visualizing predictions.
2. Calculating the following metrics:
   
   - **Precision**
   - **Recall**
   - **F1-Score**
   - **mAP@50**
   - **mAP@75**
   - **mAP@[0.5:0.95]**

---

## 🏆 Metric results for 12 epochs (%)

Test results show a notable performance of transformer-based models, in particular Deformable-DETR, on both datasets.

### **Pleiades Aircraft Dataset**

| Model            | Training Time (s) | Precision | Recall | F1-Score | mAP@50 | mAP@75 | mAP@[0.5:0.95] |
|-----------------|------------------|-----------|--------|----------|--------|--------|--------------|
| **Deformable DETR** | 327.34         | 97.76     | 88.59   | **92.00**     | **89.42**  | **89.42**  | **76.75**  |
| **DETR**            | 306.33         | 93.21     | 90.35   | 91.19     | 80.05  | 78.46  | 73.44  |
| **YOLO V10**        | 365.32         | 96.34     | 91.43   | 93.82     | 97.34  | 76     | 65.36  |
| **Faster R-CNN**    | 435.22         | 93.33     | 93.33   | 93.33     | 81.66  | 78.97  | 73.77  |
| **RetinaNet**       | 719.46         | 80.80     | 73.30   | 76.87     | 74.76  | 69.56  | 55.80  |


### **SSDD SAR Dataset**

| Model            | Training Time (s) | Precision | Recall | F1-Score | mAP@50 | mAP@75 | mAP@[0.5:0.95] |
|-----------------|------------------|-----------|--------|----------|--------|--------|--------------|
| **Deformable DETR** | **3370.16**         | **96.26**     | **90.88**   | **92.91**     | **92.31**  | **88.66**  | **75.14**  |
| **DETR**            | 3583.12         | 86.31     | 89.21   | 87.74     | 95.42  | 84.12  | 75.86  |
| **YOLO V10**        | 3750.52         | 94.05     | 90.31   | 92.14     | 96.49  | 81.49  | 65.18  |
| **Faster R-CNN**    | 3152.24         | 90.36     | 87.23   | 88.77     | 91.61  | 73.93  | 62.53  |
| **RetinaNet**       | 3997.13         | 83.85     | 83.13   | 82.80     | 86.75  | 78.02  | 64.54  |
