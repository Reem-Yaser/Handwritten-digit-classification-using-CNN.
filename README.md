# 🧠 Handwritten Digit Recognition using CNN (MNIST)

## Problem Description
This project implements a Deep Learning model using Convolutional Neural Networks (CNN) to classify handwritten digits (0–9) from the MNIST dataset.

The goal is to compare two CNN architectures:
- Simple CNN
- Deep CNN with Dropout

and evaluate their performance based on accuracy and loss.

---

## Dataset
- Dataset: MNIST
- Source: torchvision.datasets.MNIST
- Image size: 28x28 grayscale
- Classes: 10 digits (0–9)
- Training samples: 60,000
- Testing samples: 10,000

---

## Models Used

### 1️Simple CNN
Architecture:
- Conv2D → ReLU → BatchNorm → MaxPool
- Conv2D → ReLU → BatchNorm → MaxPool
- Fully Connected Layers

### 2️Deep CNN
Architecture:
- More convolutional layers
- Batch Normalization
- Dropout (0.5) for regularization
- Fully Connected Layers

---

## Training Details
- Optimizer: Adam
- Loss Function: CrossEntropyLoss
- Epochs: 5
- Batch Size: 32
- Framework: PyTorch

---

## Results

### Simple CNN Results

| Epoch | Train Acc | Test Acc | Train Loss | Test Loss |
|------|----------|----------|------------|-----------|
| 1 | 99.04% | 99.00% | 0.0343 | 0.0364 |
| 2 | 99.34% | 99.12% | 0.0216 | 0.0350 |
| 3 | 99.51% | 98.91% | 0.0161 | 0.0452 |
| 4 | 99.49% | 98.88% | 0.0164 | 0.0523 |
| 5 | 99.58% | 98.80% | 0.0135 | 0.0532 |

---

### Deep CNN Results

| Epoch | Train Acc | Test Acc | Train Loss | Test Loss |
|------|----------|----------|------------|-----------|
| 1 | 94.92% | 98.70% | 0.1745 | 0.0397 |
| 2 | 97.56% | 98.73% | 0.0888 | 0.0499 |
| 3 | 98.12% | 98.84% | 0.0718 | 0.0505 |
| 4 | 98.48% | 99.04% | 0.0576 | 0.0378 |
| 5 | 98.66% | 99.19% | 0.0492 | 0.0399 |

---

## Final Comparison

| Model | Best Test Accuracy | Final Test Loss |
|------|-------------------|----------------|
| Simple CNN | 99.12% | 0.0532 |
| Deep CNN | **99.19%** | 0.0399 |

---

## Observations
- Deep CNN achieved slightly better generalization due to Dropout and deeper architecture.
- Simple CNN converges faster but slightly overfits at later epochs.
- Both models perform very well on MNIST dataset.

---

## How to Run

1. Open notebook in Google Colab or Jupyter Notebook  
2. Install dependencies:
```bash
pip install torch torchvision matplotlib