
# Pneumonia Classification using Deep Learning (Chest X-ray)

### 📌 Project Description

This project implements an automated pneumonia classification system using deep learning and chest X-ray images.
A pretrained DenseNet convolutional neural network is fine-tuned to classify chest X-ray scans into Normal and Pneumonia categories.

The main objective of this project is to assist doctors and radiologists by providing a fast, accurate, and AI-based preliminary diagnosis for pneumonia.

### 🎯 Project Objectives

- Automatically detect pneumonia from chest X-ray images
- Classify X-ray scans as Normal or Pneumonia
- Reduce manual diagnostic workload
- Improve diagnostic accuracy using transfer learning

### Disease Classes

*The model classifies chest X-ray images into two categories:*

- Normal
- Pneumonia

### 📊 Dataset Information

- Dataset Type: Chest X-ray Images
- Image Format: JPG / PNG
- Total Images: ~5,800+
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

### 🏗 Model Architecture

This project uses Transfer Learning with a pretrained DenseNet-121 model.

*🔹 Base Model*

- DenseNet-121 pretrained on ImageNet

- Used as a feature extractor

- Initial layers frozen during early training to preserve learned features

*🔹 Custom Classification Head*

- Global Average Pooling layer
- Dense layer with 128 neurons, ReLU activation, and L2 regularization
- Dropout layer with 60% rate
- Dense layer with 64 neurons, ReLU activation, and L2 regularization
- Dropout layer with 50% rate
- Output layer with 2 neurons and Softmax activation (Normal vs Pneumonia)


### ⚙ Training Configuration

- Optimizer: Adam
- Learning Rate: 0.0001
- Loss Function: Categorical Cross-Entropy
- Label Format: One-hot encoded
- Evaluation Metric: Accuracy
- Epochs: 50

### 📈 Model Performance

- Achieved high accuracy on test data
- Stable training with minimal overfitting
- Good generalization between Normal and Pneumonia cases

Classification Report:

<img src="results/Classification report.png" width="500" height="500">

Confusion Matrix:

<img src="results/Confusion matrix.png" width="500" height="500">

Normalized Confusion Matrix:

<img src="results/Normalized Confusion matrix.png" width="500" height="500">
