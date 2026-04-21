Handwritten Digit Recognition with MLP and CNN

Overview

This project explores handwritten digit recognition using the MNIST dataset by implementing and comparing two deep learning approaches:

Multi-Layer Perceptron (MLP): a fully connected neural network for baseline performance.
Convolutional Neural Network (CNN): a more powerful architecture designed to capture spatial features in images.

Both models are trained on 28×28 grayscale images representing digits from 0 to 9.
An interactive interface built with Gradio allows users to draw digits and obtain real-time predictions.

Key Features

Data preprocessing: normalization, reshaping, and one-hot encoding.
Two model architectures:
MLP: Flatten → Dense(128, ReLU) → Dense(10, Softmax)
CNN: Conv2D(32, 3×3) → MaxPooling(2×2) → Conv2D(64, 3×3) → MaxPooling(2×2) → Flatten → Dense(128, ReLU) → Dense(10, Softmax)
Training setup: 10 epochs with a 10% validation split.

Model evaluation:
Accuracy and loss curves
Classification reports
Confusion matrices
F1-scores (macro and micro)
Interactive demo: draw digits using Gradio’s Sketchpad and get instant predictions.

Installation
1.Clone the repository:

git clone https://github.com/SihamBouzagrar/MNIST-Handwritten-Digit-Classifier.git
cd MNIST-Handwritten-Digit-Classifier

2.Install dependencies:
pip install tensorflow numpy matplotlib scikit-learn gradio pillow

3.Run the notebook in Jupyter (or any compatible environment).
The MNIST dataset will be downloaded automatically.

Usage
Training & Evaluation

Run all notebook cells to:

Load and preprocess the dataset
Train both MLP and CNN models
Visualize training and validation performance
Evaluate models using multiple metrics

Saved models:
model_mlp.keras
mnist_cnn.keras

Project Structure
.
├── mnist_mlp_cnn.ipynb
├── model_mlp.keras
├── mnist_cnn.keras
└── README.md

Dependencies
Python 3.x
TensorFlow 2.21
NumPy
Matplotlib
scikit-learn
Gradio
Pillow