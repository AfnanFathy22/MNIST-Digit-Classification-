# MNIST-Digit-Classification-

Project Overview
The notebook implements a deep learning solution for the classic MNIST Handwritten Digit Classification task using the Keras library. 
The goal is to correctly identify digits (0-9) from grayscale images.

Dataset Details

Source: The standard MNIST dataset provided by Keras.

Size: 60,000 training samples and 10,000 test samples.

Input Format: 28x28 pixel grayscale images.

Key Steps & Methodology

Data Preprocessing:

Flattening: The 2D image matrices (28x28) are reshaped into 1D vectors of 784 elements to serve as input for the dense layers.

Normalization: Pixel values are scaled from the range [0] [255] to [0] [1] to improve training stability.

One-Hot Encoding: Target labels are converted into categorical vectors.

Model Architecture:
A Sequential neural network with the following structure:

Dense Layer 1: 128 units, ReLU activation.

Dense Layer 2: 256 units, ReLU activation.

Dense Layer 3: 256 units, ReLU activation.

Dense Layer 4: 64 units, ReLU activation.

Output Layer: 10 units, Softmax activation (for probability distribution over 10 classes).

Total Parameters: 216,394 trainable parameters.

Training Configuration:

Optimizer: Stochastic Gradient Descent (SGD).

Loss Function: Categorical Crossentropy.

Hyperparameters: 50 epochs, batch size of 64, and a 10% validation split.

Performance Results

Training Accuracy: ~99.7%

Validation Accuracy: ~97.8%

Final Test Accuracy: 97.6%

Evaluation & Visualization

The notebook concludes with a Confusion Matrix generated using Seaborn, providing a detailed breakdown of the model's predictions across all ten digit classes.
