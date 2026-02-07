
# 🧠 Brain Tumor Classification using Deep Learning (MRI)

### 📌 Project Description

This project implements an automated brain tumor classification system using deep learning and medical MRI images.
A pretrained DenseNet convolutional neural network is fine-tuned to classify brain MRI scans into multiple tumor categories.
The goal of this project is to assist medical professionals by providing a fast and reliable AI-based diagnostic support system.


### 🎯 Project Objectives

- Automatically classify brain tumors from MRI images
- Distinguish between different tumor types
- Reduce dependency on manual diagnosis
- Improve accuracy using transfer learning



### 🧠 Tumor Classes

The model classifies MRI images into four categories:

- Glioma Tumor

- Meningioma Tumor

- Pituitary Tumor

- No Tumor


### 📊 Dataset Information

Dataset Type: Brain MRI Images

- Image Format: JPG / PNG
- Total Images: 7,023
- Data Split:
- Training Set: 70%
- Validation Set: 20%
- Test Set: 10%
  
### 🖼 Image Preprocessing

*To improve model performance, the following preprocessing steps are applied:*

- Resize images to 224 × 224 pixels
- Normalize pixel values to range 0–1
- Convert images to NumPy arrays
- Apply data augmentation:
- Rotation
- Zoom
- Horizontal flipping
