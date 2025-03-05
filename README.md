# Deep Learning for Medical Imaging – Assignments Overview

This repository contains my assignments for the **Deep Learning for Medical Imaging** course. 
In this README, I will summarize the key learnings from each assignment and the objectives achieved.

## Assignment 1: Handwritten Digit Recognition Using Fully Connected Neural Networks

### **Objective**
- Analyze normalized handwritten digits from scanned envelopes by the U.S. Postal Service.
- Predict digit IDs (0-9) from **16×16 grayscale images**.

### **Key Learnings**
1. Explored **neural network architectures** for image classification, specifically using **fully connected layers instead of CNNs**.
2. Studied literature on similar handwritten digit datasets and applied **best practices in hyperparameter tuning**.
3. Designed a **compact neural network** with two hidden layers, balancing efficiency and accuracy.
4. Achieved **95% validation accuracy** and **94.4% test accuracy** while significantly reducing computational cost.
5. Demonstrated that a well-optimized fully connected network can perform efficiently for small-scale image classification tasks, reducing **inference time, energy consumption, and training duration**.

## Assignment 2: SPECT Image Classification for Parkinson’s Disease Staging

### **Objective**
- Analyze Single Photon Emission Computed Tomography (SPECT) images from individuals with Parkinson’s disease (PD).
- Classify patients into three illness stages based on disease severity.

### **Key Learnings**
1. **Image Preprocessing for Improved Feature Extraction**
   - Applied cropping to extract the central 50×50 pixels, focusing on the most relevant regions of the SPECT images.
   - Used normalization to standardize pixel intensity values, reducing input variance and improving model convergence.
   - These preprocessing steps enhanced the signal-to-noise ratio, leading to more stable and reliable training performance.
  
2. **Handling Imbalanced Classes**
   - Used Random Oversampling or Adjusted the Weighted Loss Function to ensure a more balanced contribution of different classes in the loss function.
   - To address insufficient sample size, applied image augmentation techniques to artificially increase dataset diversity.

3. **Exploring Model Architectures & Transfer Learning**
   - Tested various deep learning models for feature extraction and classification, including **CNN-based architectures (Redefined VGG16, Redefined ResNet) and Transformer-based models (Redefined ViT)**.
   - Leveraged transfer learning with pre-trained models to enhance generalization on the small dataset.
   - Transfer learning significantly improved training stability and boosted accuracy beyond what was achievable with training from scratch.

4. **Model Selection for Small Dataset Constraints**
   - Due to the limited number of training samples, opted for Redefined VGG16, a CNN model with fewer parameters, to prevent overfitting.
   - The reduced model complexity allowed for more efficient training while maintaining classification performance.
   - Achieved a final accuracy **exceeding the baseline of 25%**, demonstrating the effectiveness of a compact model when dealing with small medical datasets.



## Assignment 3: 3D MRI Image Classification for Brain Tumor Detection

### **Objective**
- Analyze and predict**3D Magnetic Resonance Imaging (MRI)** scans from **normal individuals and patients with brain tumors**.

### **Key Learnings**
1. **Data Preprocessing for Enhanced Model Performance**
   - Applied Contrast Adjustment and Normalization to **reduce brightness variations between images**, enhancing training stability and improving model learning efficiency.
   - Used Trilinear Interpolation for upsampling, ensuring **uniform depth dimensions** across different patients’ 3D MRI scans.

2. **Exploring Different 3D MRI Classification Approaches**
   - Tested four different methods based on **modified pre-trained VGG16 models** for **3D MRI brain tumor classification**:
     - Single Slice, Late Fusion, Early Fusion, 3D Model based on ResNet50
   - Compared the effectiveness of these approaches for extracting meaningful 3D features.

3. **Model Selection & Performance**
   - Selected **Late Fusion** as the final approach for classification, as it demonstrated superior performance in handling 3D MRI data with small sample size.
   - Achieved a final accuracy **nearly 20% higher than the baseline**, showcasing the effectiveness of this method for brain tumor detection.
