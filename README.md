# Chest-Disease-Detection
This repository contains code and results for a deep learning assignment focused on detecting multiple chest diseases from chest X-ray images using the Faster R-CNN object detection model.

## 📑 Table of Contents

- [Overview](#overview)
- [📂 Part 1: Data Preprocessing](#part-1-data-preprocessing)
- [🚀 Part 2: Disease Detection using Faster R-CNN](#part-2-disease-detection-using-faster-r-cnn)
- [🎯 Part 3: Model Interpretation and Visualization](#part-3-model-interpretation-and-visualization)

---

## 🧠 Overview

The goal of this project is to apply **Faster R-CNN** to detect thoracic diseases in chest X-ray images. The model is used to identify one or more of the following conditions per image:
- Aortic calcification
- Aortic curvature
- Increased pulmonary markings
- Degenerative joint disease of the spine
- Scoliosis
- Apical pleural thickening
- Cardiomegaly
- Normal (no disease)

By assisting with early disease detection, such a model can help reduce diagnostic workload and improve clinical outcomes.

---

## 📂 Part 1: Data Preprocessing

- Converted file names from Chinese to English to avoid encoding issues
- Visualized and annotated X-ray images with bounding boxes for disease areas
- Applied two preprocessing methods:
  - **Intensity Log-Transformation** – enhanced contrast by compressing pixel range
  - **Simplest Color Balance Algorithm** – improved brightness and contrast
- Converted annotations to COCO format for object detection
- Split dataset into training and testing sets based on volunteer IDs

---

## 🚀 Part 2: Disease Detection using Faster R-CNN

- Used **pretrained Faster R-CNN** with **ResNet50** as the backbone
- Resized all X-ray images to **1024×1024** for consistent input size
- Adjusted bounding boxes accordingly to match resized images
- Tuned hyperparameters including:
  - Learning rate: compared 0.001 vs. 0.0005
  - Weight decay
  - Momentum (set to 0.9 to help escape local minima)
- Evaluated model using **mAP@0.5 (mAP50)** on training and validation data

---

## 🎯 Part 3: Model Interpretation and Visualization

Implemented two CAM-based visualization techniques:

### Eigen CAM
- Fast and highlights key discriminative regions
- Useful for identifying the most influential parts of the image

### Ablation CAM
- Suppresses parts of the feature map to assess regional importance
- Captures more contextual and related anatomical regions
- Slower and can introduce noise, but gives richer interpretability
