# Chest-Disease-Detection
This repository contains code and results for a deep learning assignment focused on detecting multiple chest diseases from chest X-ray images using the Faster R-CNN object detection model.

📑 Table of Contents
Overview

Part 1: Data Preprocessing

Part 2: Disease Detection using Faster R-CNN

Part 3: Model Interpretation and Visualization

Results & Discussion

References

🧠 Overview
Brief explanation of the project goals: applying Faster R-CNN to chest X-rays to detect seven disease types and normal cases, emphasizing the model's clinical utility.

📂 Part 1: Data Preprocessing
Renaming files for compatibility

Visualizing disease regions with bounding boxes

Applying image enhancement methods:

Intensity Log-Transformation

Simplest Color Balance Algorithm

Generating COCO-format annotations for training

🚀 Part 2: Disease Detection using Faster R-CNN
Model setup using pretrained Faster R-CNN with ResNet50

Image resizing strategy (1024x1024)

Bounding box alignment

Training strategy and hyperparameter tuning (learning rate, momentum, etc.)

Evaluation using mAP@0.5 (mAP50)

🎯 Part 3: Model Interpretation and Visualization
Application of Eigen CAM for key feature localization

Application of Ablation CAM for interpretability and deeper analysis

Comparisons of visualization results between normal and disease cases
