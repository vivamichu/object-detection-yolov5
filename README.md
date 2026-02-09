# Person Detection in Low-Light Conditions

This repository implements an **object detection pipeline for identifying people in low-light environments** using a YOLO-based model.  
The project focuses on dataset analysis, preprocessing, training, and evaluation tailored specifically for dark and low-visibility scenes.

---

## 📌 Project Overview

Detecting humans in low-light conditions is challenging due to noise, low contrast, and poor visibility.  
This project addresses these challenges by:

- Performing exploratory data analysis (EDA) on low-light images
- Converting annotations to **YOLO format**
- Training a **YOLOv5s-based detector**
- Applying augmentations suitable for dark environments
- Evaluating detection performance using **mAP metrics**

---

## 🧠 Pipeline Overview

The project follows the steps below:

1. **Exploratory Data Analysis (EDA)**
   - Visual inspection of low-light images
   - Detection of corrupted or low-quality samples
   - Analysis of bounding box distributions and image sizes

2. **Data Preparation**
   - Conversion of annotations to YOLO format
   - Train/validation split
   - Dataset organization for YOLO training

3. **Model Architecture**
   - Base model: **YOLOv5s**
   - Custom hyperparameters optimized for low-light detection

4. **Training**
   - Data augmentations tailored for dark scenes
   - Optimized learning rate and batch size
   - Validation monitoring during training

5. **Evaluation**
   - Quantitative evaluation using:
     - mAP@0.5
     - mAP@0.5:0.95
   - Qualitative analysis of detection results

---

## 📂 Repository Structure

```text
├── task.ipynb                 # Main notebook (EDA → training → evaluation)
├── data/
│   ├── images/
│   │   ├── train/
│   │   └── val/
│   └── labels/
│       ├── train/
│       └── val/
├── README.md
