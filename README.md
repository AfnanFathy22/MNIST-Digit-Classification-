
# MNIST Digit Classification

## Project Overview

This project implements a deep learning solution for the classic MNIST handwritten digit classification task using the Keras library. The goal is to correctly identify digits (0–9) from grayscale images.

---

## Dataset Details

* **Source:** The standard MNIST dataset provided by Keras
* **Training Set Shape:** (60000, 28, 28)
* **Test Set Shape:** (10000, 28, 28)
* **After Flattening:**

  * Training: (60000, 784)
  * Test: (10000, 784)
* **Image Size:** 28 × 28 pixels
* **Input Type:** Grayscale (single channel)

---

## Key Steps & Methodology

### Data Preprocessing

* **Flattening:**
  Each image is reshaped from (28, 28) into a vector of shape (784,) to be compatible with Dense layers.

* **Normalization:**
  Pixel values are scaled from [0, 255] to [0, 1] by dividing by 255.0 to improve training stability.

* **One-Hot Encoding:**
  Labels are converted into categorical vectors of shape (10,).

  * Before encoding: (60000,)
  * After encoding: (60000, 10)

---

## Model Architecture

A Sequential neural network with the following structure:

* Dense Layer 1: 128 units, ReLU activation

* Dense Layer 2: 256 units, ReLU activation

* Dense Layer 3: 256 units, ReLU activation

* Dense Layer 4: 64 units, ReLU activation

* Output Layer: 10 units, Softmax activation

* **Total Parameters:** 216,394 trainable parameters

---

## Training Configuration

* **Optimizer:** Stochastic Gradient Descent (SGD)
* **Loss Function:** Categorical Crossentropy
* **Hyperparameters:**

  * Epochs: 50
  * Batch Size: 64
  * Validation Split: 0.1

---

## Performance Results

* **Training Accuracy:** ~99.7%
* **Validation Accuracy:** ~97.8%
* **Test Accuracy:** 97.6%

---

## Evaluation & Visualization

The model is evaluated using a confusion matrix generated with Seaborn, providing a detailed breakdown of predictions across all digit classes.
