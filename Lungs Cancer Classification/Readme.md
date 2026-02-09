

# Pneumonia Classification using Deep Learning (Chest X-ray)

### 📌 Overview
This project focuses on automated lung cancer classification from CT scan images using a fine-tuned DenseNet CNN architecture. The system aims to assist radiologists by providing reliable predictions and explainability through Grad-CAM heatmaps.


### Disease Class
Classify CT scans into four categories:

- Normal
- Adenocarcinoma
- Large Cell Carcinoma
- Squamous Cell Carcinoma

Build a Streamlit web interface for doctors to upload scans and view predictions.

### 🏗️ System Architecture
- Image Upload
- Preprocessing (resize, normalize, augment)
- Model Inference (DenseNet + custom classifier head)

### ⚙️ Technology Stack
- Python – Core programming language
- TensorFlow / Keras – Deep learning framework
- OpenCV & PIL – Image preprocessing
- NumPy – Numerical operations
- Streamlit – Web interface
- DenseNet (CNN) – Pretrained model fine-tuned for CT scans

### 📊 Dataset Information
- CT Scan Dataset Size: 1730 images
- Classes:
   > Normal
   > Adenocarcinoma
   > Large Cell Carcinoma
   > Squamous Cell Carcinoma

Split: Train 70%, Validation 20%, Test 10%

### 🖼 Image Preprocessing
*To improve model performance, the following preprocessing steps are applied:*
- Resize images to 224 × 224 pixels
- Normalize pixel values to range 0–1
- Convert images to NumPy arrays
- Apply data augmentation:
- Rotation
- Zoom
- Horizontal flipping

### 🧠 Model Architecture
Base Model: Pretrained DenseNet

Classifier Head:

- Global Average Pooling
- Dense Layers (128 → 64 neurons, ReLU, L2 regularization)
- Dropout (60%, 50%)
- Output Layer: 4 neurons, Softmax activation
  
Training Config:
- Optimizer: Adam (lr = 0.0001)
- Loss: Categorical Cross-Entropy
- Metric: Accuracy
- Epochs: 50 with Early Stopping

### 🚀 Results
- Achieved high accuracy on validation and test sets.
- Confusion matrix highlights strong classification performance across all four categories.

### Classification Report:



###🌐 Web Application

The trained pneumonia detection model is integrated into a Streamlit web application, which allows users to:

- Upload chest X-ray images
- Get real-time predictions (Normal / Pneumonia)
- View prediction confidence scores

### 🛠 Technologies Used

- Python
- TensorFlow / Keras
- DenseNet-121 (CNN)
- OpenCV
- NumPy
- PIL
- Streamlit


⚠ Disclaimer

This project is developed for educational and research purposes only.
It should not be used as a replacement for professional medical diagnosis.
