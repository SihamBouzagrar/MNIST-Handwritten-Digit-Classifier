Handwritten Digit Recognition with MLP and CNN
📌 Overview

This project explores handwritten digit recognition using the MNIST dataset by implementing and comparing two deep learning approaches:

Multi-Layer Perceptron (MLP): a fully connected neural network used as a baseline model
Convolutional Neural Network (CNN): a more advanced architecture designed to capture spatial features in images

Both models are trained on 28×28 grayscale images representing digits from 0 to 9.

An interactive interface built with Gradio allows users to draw digits and obtain real-time predictions.

✨ Key Features
📊 Data Preprocessing
Normalization
Reshaping
One-hot encoding
🧠 Model Architectures
🔹 MLP
Flatten → Dense(128, ReLU) → Dense(10, Softmax)
🔹 CNN
Conv2D(32, 3×3) → MaxPooling(2×2)
Conv2D(64, 3×3) → MaxPooling(2×2)
Flatten → Dense(128, ReLU) → Dense(10, Softmax)
🏋️ Training Setup
10 epochs
10% validation split
📈 Model Evaluation
Accuracy & loss curves
Classification reports
Confusion matrices
F1-scores (macro & micro)
🎨 Interactive Demo
Gradio Sketchpad interface
Draw a digit → get instant prediction
⚙️ Installation
1️⃣ Clone the repository
git clone https://github.com/SihamBouzagrar/MNIST-Handwritten-Digit-Classifier.git
cd MNIST-Handwritten-Digit-Classifier
2️⃣ Install dependencies
pip install tensorflow numpy matplotlib scikit-learn gradio pillow
3️⃣ Run the project

Open Jupyter Notebook:

jupyter notebook

The MNIST dataset will be downloaded automatically.

🚀 Usage
📊 Training & Evaluation

Run all notebook cells to:

Load and preprocess the dataset
Train MLP and CNN models
Visualize training performance
Evaluate models
💾 Saved Models
model_mlp.keras
mnist_cnn.keras
📁 Project Structure
.
├── mnist_mlp_cnn.ipynb
├── model_mlp.keras
├── mnist_cnn.keras
└── README.md
📦 Dependencies
Python 3.x
TensorFlow 2.x
NumPy
Matplotlib
scikit-learn
Gradio
Pillow