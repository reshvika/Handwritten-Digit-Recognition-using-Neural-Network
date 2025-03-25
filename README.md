![Screenshot (22)](https://github.com/user-attachments/assets/c0cfe4f8-d3a6-4fa3-8f7c-28f03271744e)
# Handwritten-Digit-Recognition-using-Neural-Network
Handwritten Digit Recognition using Neural Network
# Handwritten Digit Recognition with GUI

This project implements a handwritten digit recognition system using a neural network, trained on the MNIST dataset. It extends the basic recognition task by providing a graphical user interface (GUI) that allows users to draw digits directly on the screen for real-time recognition.

## Table of Contents

- [Introduction](#introduction)
- [Approach](#approach)
- [Methodology](#methodology)
- [Files](#files)
- [Dependencies](#dependencies)
- [Installation](#installation)
- [Usage](#usage)
- [Results](#results)
- [Dataset](#dataset)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project aims to recognize handwritten digits, both from scanned images (MNIST dataset) and from user-drawn input via a GUI. It leverages a three-layered neural network to achieve high accuracy in digit classification.

## Approach

The system employs a neural network with the following architecture:

-   **Input Layer:** 784 nodes (corresponding to the 28x28 pixel images).
-   **Hidden Layer:** 100 activation units.
-   **Output Layer:** 10 nodes (representing digits 0-9).

The neural network utilizes feedforward propagation for prediction and backpropagation for weight optimization.

## Methodology

1.  **Data Loading and Preprocessing:**
    -      The MNIST dataset is loaded from a `.mat` file.
    -      Features (pixel values) are normalized to the range [0, 1].
    -      Data is split into 60,000 training and 10,000 testing examples.
2.  **Neural Network Training:**
    -      Weights are randomly initialized.
    -      The neural network is trained using the L-BFGS-B optimization algorithm, minimizing the cost function.
    -   Regularization(lambda = 0.1) is used to prevent overfitting.
    -   The network is trained for 100 iterations.
3.  **Prediction and Evaluation:**
    -      The trained network is used to predict digits on both the training and testing sets.
    -      Accuracy and precision are calculated to evaluate performance.
4.  **GUI Implementation:**
    -      A Tkinter-based GUI allows users to draw digits on a canvas.
    -      The drawn image is preprocessed and fed into the trained neural network for recognition.

## Files

-   `Main.py`: Main script for training and testing the neural network.
-   `RandInitialize.py`: Initializes the weights of the neural network.
-   `Model.py`: Implements the neural network's feedforward and backpropagation algorithms.
-   `Prediction.py`: Predicts the digit from the input image.
-   `GUI.py`: Implements the graphical user interface for digit drawing and recognition.
-   `Theta1.txt`: Saved trained weights for the first layer.
-   `Theta2.txt`: Saved trained weights for the second layer.
-   `mnist-original.mat`: MNIST dataset file.

## Dependencies

-   `scipy`
-   `numpy`
-   `tkinter`
-   `Pillow (PIL)`
## Results
-  Training Set Accuracy: ~99.44%
-  Test Set Accuracy: ~97.32%
-  Precision: ~0.9944

You can install these dependencies using pip:

```bash
pip install scipy numpy pillow
