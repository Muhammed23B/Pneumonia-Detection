# Pneumonia-Detection
🩺 Pneumonia Detection Using Deep Learning (Chest X-Ray Classification)
A deep learning project to classify chest X-ray images as Pneumonia or Normal using Convolutional Neural Networks (CNNs) in TensorFlow/Keras.

📌 Table of Contents

1.Overview

2.Dataset

3.Project Pipeline

4.Model Architecture

5.Results

6.How to Run

7.Future Improvements

8.Dependencies

9.References







✅ Overview   
Pneumonia is a potentially life-threatening lung infection. This project uses a Convolutional Neural Network (CNN) to detect pneumonia from chest X-ray images. The goal is to build a simple yet effective binary image classifier that distinguishes between Normal and Pneumonia-infected lungs.

📂 Dataset
Name: Chest X-Ray Images (Pneumonia)

Source: https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia

Classes:

NORMAL

PNEUMONIA




🔧 Project Pipeline
Download dataset using Kaggle API (kaggle.json)

Preprocess images:

Resize to 150x150

Normalize pixel values (rescale to [0, 1])

Augment training data (zoom, shear, flip)

Build CNN model using Keras Sequential API

Train model for 10 epochs with validation tracking

Evaluate model on test set

Visualize performance (accuracy/loss curves)



🧠 Model Architecture


Input: 150x150 RGB image
↓
Conv2D (32 filters) + ReLU
↓
MaxPooling2D
↓
Conv2D (64 filters) + ReLU
↓
MaxPooling2D
↓
Flatten
↓
Dense (128 units, ReLU)
↓
Dropout (rate = 0.5)
↓
Dense (1 unit, Sigmoid) → Binary Classification

Optimizer: Adam

Loss Function: Binary Crossentropy

Metric: Accuracy






📊 Results
Metric	         Value
Training Acc	    ~98%
Validation Acc	  ~90–93%
Test Acc       	  ~90%




▶️ How to Run
💡 Recommended to run in Google Colab

Step 1: Upload Kaggle API Key
Download kaggle.json from your Kaggle account

Upload it using:
from google.colab import files
files.upload()  # Select kaggle.json


Step 2: Install dependencies and download dataset
!pip install kaggle
!mkdir -p ~/.kaggle
!cp kaggle.json ~/.kaggle/
!chmod 600 ~/.kaggle/kaggle.json
!kaggle datasets download -d paultimothymooney/chest-xray-pneumonia
!unzip -q chest-xray-pneumonia.zip


Step 3: Train the model
code is available in pneumonia_detection_code


🚀 Future Improvements
Use transfer learning with pre-trained models like ResNet50 or EfficientNet

Add Grad-CAM visualizations for model interpretability

Implement Focal Loss to address class imbalance

Track training metrics with TensorBoard

Deploy as a web app using Streamlit or Flask













