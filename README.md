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


