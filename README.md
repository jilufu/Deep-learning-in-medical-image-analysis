# Deep Learning for Medical Imaging – Assignments Overview

This repository contains my assignments for the **Deep Learning for Medical Imaging** course. 
In this README, I will summarize the key learnings from each assignment and the objectives achieved.


## == Abnormality Detection in Chest X-ray Images==

### **Objective**
- Develop a **deep learning model** to detect abnormal regions in **chest X-ray images** using **bounding boxes** and annotate possible **chest diseases**.

### **Methodology**
- **Data Preprocessing**:
  - Applied **log-transformation** to normalize intensity distribution and enhance abnormal structure visibility.
  - Used **contrast adjustment** to highlight critical structures for better model recognition.
- **Model Implementation**:
  - Utilized a **ResNet-50-based Faster R-CNN** as the object detection framework.
  - Replaced the **COCO pre-trained classification head** with a customized classification layer for the dataset.
  - Integrated **NMS (Non-Maximum Suppression)** to retain the most confident predictions per category.
- **Model Evaluation**:
  - Assessed performance using **mAP (Mean Average Precision)** and **total loss analysis** (classification loss, bounding box regression loss, RPN losses).
  - Applied **EigenCAM and AblationCAM** for model interpretability and visualization.

### **Results**
- Achieved a **test set mAP of 0.277**, surpassing the **baseline**.

### For a detailed report on this assignment, please refer to the [full report (PDF)](object_detection_annotation_final_report.pdf).


## Carotid Artery Segmentation from Sonography Images

### **Objective**
- Segment the **carotid artery** from **sonography images** using **semantic segmentation techniques**.

### **Methodology**
- Studied the **Fully Convolutional Network (FCN) architecture** and explored models suitable for **medical image segmentation**.
- Implemented **U-Net** as the primary model for segmentation.
- Evaluated model performance using the **Dice Coefficient**, selecting the most optimal model.

### **Results**
- Achieved a **Dice Coefficient of 0.95** on the test set, surpassing the **baseline by 0.03**.




## 3D MRI Image Classification for Brain Tumor Detection

### **Objective**
- Classify **brain tumor presence** using **3D MRI scans** from normal individuals and patients.

### **Methodology**
- **Preprocessing**: Applied **contrast adjustment, normalization**, and **trilinear interpolation** to standardize image depth and enhance feature visibility.
- **Model Exploration**: Tested four **pre-trained VGG16-based** approaches (**Single Slice, Late Fusion, Early Fusion**) and a **ResNet50-based 3D model**.
- **Final Model**: Selected **Late Fusion** for its superior performance on a small dataset.

### **Results**
- Achieved **nearly 20% higher accuracy than the baseline**, demonstrating the **effectiveness of Late Fusion for 3D MRI classification**.



## SPECT Image Classification for Parkinson’s Disease Staging
### **Objective**
- Classify **Parkinson’s disease (PD) stages (1, 2, 3)** from **SPECT images** based on disease severity.

### **Methodology**
- **Preprocessing**: Cropped images to **50×50 pixels**, applied **normalization** to enhance stability and feature extraction.
- **Class Imbalance Handling**: Used **Random Oversampling** and **Weighted Loss Adjustment** to balance training data.
- **Model Selection**: Evaluated **CNN-based (Redefined VGG16, ResNet)** and **Transformer-based (ViT)** models with **transfer learning** for improved accuracy.
- **Final Model**: Chose **Redefined VGG16** due to its efficiency in handling small datasets.

### **Results**
- Achieved **higher accuracy than the 25% baseline**, demonstrating **effective classification with a compact CNN model**.




## Handwritten Digit Recognition Using Fully Connected Neural Networks

### **Objective**
- Classify **handwritten digits (0-9)** from **16×16 grayscale images** scanned by the U.S. Postal Service.

### **Methodology**
- Implemented a **fully connected neural network (two hidden layers)** instead of CNNs to reduce computational cost.
- Applied **hyperparameter tuning** based on literature from similar datasets.
- Optimized network design to balance **efficiency and accuracy**.

### **Results**
- Achieved **95% validation accuracy** and **94.4% test accuracy**.
- Reduced **inference time, energy consumption, and training duration**, demonstrating the effectiveness of a compact network for small-scale image classification.


