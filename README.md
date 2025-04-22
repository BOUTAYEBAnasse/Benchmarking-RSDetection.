# 🛰 Remote Sensing Object Detection Benchmark

This repository contains the data and resources needed to apply the Deformable-DETR model (Zhu et al., 2021) to optical and SAR remote sensing images.

<div align="center" style="border: 2px solid black; padding: 10px; background-color: #f8f8f8;">
    <img src="assets/GITHUB_COVER.PNG" alt="Description du graphique" width="650">
</div>

## 📊 Notebooks for Benchmarking 

This repository contains benchmarking notebooks for each dataset, in addition to the basic model. For both **Pleiades Aircraft Dataset** and **SSDD Dataset**, the following benchmarking models are implemented:

- **DEtection TRansformer (DETR)** (Carion et al., 2020)
- **YOLO V10** (Redmon et al., 2016)
- **RetinaNet** (Lin et al., 2017)
- **Faster R-CNN** (Ren et al., 2015)
  
---
## 📁 Repository Structure

The proposed notebooks contain implementations of each model, two notebooks for each model, one for the nominal process, i.e. training, validation and testing, and the other for rapid inference on a set of images for each model, 20 in all.

---
## 🗺️ Data to be used

This Google Drive link **[Google Drive Link](https://drive.google.com/drive/folders/1-8UDTKH-A7PerjXUXKDAXtTWKYRdj7IS?usp=sharing)** contains all the resources required to execute this project. The available resources include two datasets, Optical and SAR, using to train, validate and test the models presented.

## 📈 Workflow Diagram of Deformable-DETR

The following diagram provides a visual overview of the workflow of the proposed model, **Deformable-DETR**. It highlights the key components of the architecture, including the CNN backbone, the multi-scale deformable attention modules, and the Transformer decoder responsible for predicting object classes and bounding boxes. This structure enables efficient and accurate object detection in high-resolution remote sensing imagery.
<div align="center" style="border: 2px solid black; padding: 10px; background-color: #f8f8f8;">
    <img src="assets/Deformable-DETR.png" alt="Workflow-DEFORMABLE-DETR" width="650">
</div>
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

Test results show a notable performance of Deformable-DETR model, on both datasets.

### **Pleiades Aircraft Dataset**

| Model             | Training Time (s) | Precision | Recall | F1-Score | mAP@50 | mAP@75 | mAP@[0.5:0.95] |
|------------------|-------------------|-----------|--------|----------|--------|--------|----------------|
| **YOLO V10**      | 365.32            | 96.34     | 91.43  | 93.82    | 97.34  | 76.00  | 65.36          |
| **Faster R-CNN**  | 435.22            | 93.33     | 93.33  | 93.33    | 81.66  | 78.97  | 73.77          |
| **RetinaNet**     | 719.46            | 80.80     | 73.30  | 76.87    | 74.76  | 69.56  | 55.80          |
| **DETR**          | 327.34            | 93.21     | 90.35  | 91.19    | 80.05  | 78.46  | 73.44          |
| **Deformable DETR** | **306.53**       | **97.76** | **88.59** | **95.12** | **98.42** | **89.42** | **76.75** |



### **SSDD SAR Dataset**

| Model             | Training Time (s) | Precision | Recall | F1-Score | mAP@50 | mAP@75 | mAP@[0.5:0.95] |
|------------------|-------------------|-----------|--------|----------|--------|--------|----------------|
| **YOLO V10**      | 3750.52           | 94.05     | 90.31  | 92.14    | 96.49  | 81.49  | 75.86          |
| **Faster R-CNN**  | 3452.22           | 90.36     | 87.23  | 88.77    | 91.61  | 73.93  | 62.53          |
| **RetinaNet**     | 3997.13           | 83.85     | 83.13  | 82.80    | 86.75  | 78.02  | 64.54          |
| **DETR**          | 3583.12           | 86.31     | 89.21  | 87.74    | 95.42  | 84.12  | 75.86          |
| **Deformable DETR** | **3370.16**       | **96.26** | **92.88** | **94.54** | **97.31** | **88.66** | **76.14** |

