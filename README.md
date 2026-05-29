# Handwritten Digit Recognition using CNN (MNIST)

## Problem Description

This project implements Deep Learning models using Convolutional Neural Networks (CNNs) to classify handwritten digits (0–9) from the MNIST dataset.

The main objective is to compare:

* Simple CNN
* Deep CNN with Dropout

and evaluate their performance using accuracy and loss metrics.

---

# Dataset

* Dataset: MNIST
* Source: torchvision.datasets.MNIST
* Image Size: 28×28 grayscale
* Number of Classes: 10 digits (0–9)
* Training Samples: 60,000
* Testing Samples: 10,000

---

# Models Used

## 1️ Simple CNN

Architecture:

* Conv2D → ReLU → BatchNorm → MaxPool
* Conv2D → ReLU → BatchNorm → MaxPool
* Fully Connected Layers

## 2️ Deep CNN + Dropout

Architecture:

* Multiple Convolutional Layers
* Batch Normalization
* Dropout (0.5) for regularization
* Fully Connected Layers

---

# Training Details

* Optimizer: Adam
* Loss Function: CrossEntropyLoss
* Epochs: 5
* Batch Size: 32
* Framework: PyTorch

---

# Training Results

## Simple CNN Results

| Epoch | Train Accuracy | Test Accuracy | Train Loss | Test Loss |
| ----- | -------------- | ------------- | ---------- | --------- |
| 1     | 97.21%         | 98.02%        | 0.0901     | 0.0682    |
| 2     | 98.70%         | 98.76%        | 0.0413     | 0.0396    |
| 3     | 99.15%         | 98.64%        | 0.0275     | 0.0451    |
| 4     | 99.34%         | 98.84%        | 0.0227     | 0.0461    |
| 5     | 99.44%         | 98.69%        | 0.0186     | 0.0581    |

---

## Deep CNN Results

| Epoch | Train Accuracy | Test Accuracy | Train Loss | Test Loss |
| ----- | -------------- | ------------- | ---------- | --------- |
| 1     | 95.62%         | 98.70%        | 0.1533     | 0.0426    |
| 2     | 97.83%         | 98.89%        | 0.0798     | 0.0354    |
| 3     | 98.16%         | 99.21%        | 0.0675     | 0.0252    |
| 4     | 98.56%         | 98.96%        | 0.0535     | 0.0341    |
| 5     | 98.83%         | 99.23%        | 0.0424     | 0.0236    |

---

# Final Comparison

| Model      | Final Test Accuracy | Final Test Loss |
| ---------- | ------------------- | --------------- |
| Simple CNN | 98.69%              | 0.0581          |
| Deep CNN   | **99.23%**          | **0.0236**      |

---

# Observations

* The Deep CNN achieved better generalization performance due to the deeper architecture and Dropout regularization.
* The Simple CNN converged faster but showed slight overfitting during later epochs.
* Both models achieved excellent performance on the MNIST dataset.

---

# Visualization

The project includes:

* Training vs Testing Accuracy Curves
* Training vs Testing Loss Curves

These visualizations help analyze:

* Model convergence
* Overfitting behavior
* Generalization performance

---

# Additional Feature

The model can also predict custom handwritten digit images uploaded by the user using image preprocessing and inference techniques.

---

# How to Run

1. Open the notebook in Google Colab or Jupyter Notebook

2. Install dependencies:

```bash
pip install torch torchvision matplotlib
```

3. Run all notebook cells

4. Upload a handwritten digit image for prediction

---

# Conclusion

This project demonstrates the effectiveness of CNN architectures in image classification tasks.
The Deep CNN with Dropout achieved the best overall performance with:

* Higher test accuracy
* Lower test loss
* Better generalization on unseen data
