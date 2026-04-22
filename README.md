# 🖊️ Handwritten Digit Recognition — MLP vs CNN

> Comparing a fully connected neural network and a convolutional neural network on the MNIST dataset, with an interactive drawing interface for real-time predictions.

---

## 📌 Overview

This project implements and compares two deep learning approaches for handwritten digit recognition using the classic **MNIST dataset** (70,000 grayscale images of digits 0–9, 28×28 pixels):

| Model | Description |
|-------|-------------|
| **MLP** | Fully connected network — fast baseline |
| **CNN** | Convolutional network — captures spatial features |

Both models are evaluated on accuracy, loss curves, confusion matrices, and F1-scores. A **Gradio interface** lets you draw digits and get instant predictions.

---

## 🗂️ Project Structure

```
MNIST-Handwritten-Digit-Classifier/
├── mnist_mlp_cnn.ipynb     # Main notebook (training, evaluation, demo)
├── model_mlp.keras         # Saved MLP model
├── mnist_cnn.keras         # Saved CNN model
└── README.md
```

---

## 🧠 Model Architectures

### 🔹 MLP (Baseline)

```
Input (784)
  └─► Flatten
      └─► Dense(128, ReLU)
          └─► Dense(10, Softmax)
```

### 🔸 CNN (Main Model)

```
Input (28×28×1)
  └─► Conv2D(32, 3×3, ReLU) → MaxPooling(2×2)
      └─► Conv2D(64, 3×3, ReLU) → MaxPooling(2×2)
          └─► Flatten
              └─► Dense(128, ReLU)
                  └─► Dense(10, Softmax)
```

---

## ✨ Features

- **Data preprocessing** — normalization, reshaping, one-hot encoding
- **Training** — 10 epochs, 10% validation split
- **Evaluation** — accuracy/loss curves, classification reports, confusion matrices, macro & micro F1-scores
- **Interactive demo** — draw a digit on a Gradio sketchpad and get a live prediction

---

## ⚙️ Installation

**1. Clone the repository**
```bash
git clone https://github.com/SihamBouzagrar/MNIST-Handwritten-Digit-Classifier.git
cd MNIST-Handwritten-Digit-Classifier
```

**2. Install dependencies**
```bash
pip install tensorflow numpy matplotlib scikit-learn gradio pillow
```

**3. Launch the notebook**
```bash
jupyter notebook
```

> The MNIST dataset downloads automatically on first run.

---

## 🚀 Usage

Run all cells in `mnist_mlp_cnn.ipynb` to:

1. Load and preprocess the MNIST dataset
2. Train both MLP and CNN models
3. Visualize training curves and evaluation metrics
4. Launch the Gradio interface to draw and classify digits live

---

## 📦 Dependencies

| Package | Version |
|---------|---------|
| Python | 3.x |
| TensorFlow | 2.x |
| NumPy | latest |
| Matplotlib | latest |
| scikit-learn | latest |
| Gradio | latest |
| Pillow | latest |

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
