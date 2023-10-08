# DNN-MNIST Classification

## Overview

This project focuses on implementing a deep neural network for classifying handwritten digits using the TensorFlow library. It serves as both a practical exercise in mastering TensorFlow and an exploration of data preprocessing techniques to enhance model performance.

## Project Structure

1. **Data**
2. **Model**
3. **Objective Function**
4. **Optimization Algorithm**

The project is organized into key components:

## Data

### Data Collection

- Utilizes the popular MNIST dataset from TensorFlow, consisting of handwritten digit images with corresponding labels.
- Data is stored in npz format for TensorFlow compatibility.

### Data Preprocessing

- Splits data into training, validation, and test datasets.
- Implements shuffling for randomness, avoiding homogeneous datasets during mini-batch gradient descent.

## Model

### Deep Neural Network (DNN)

- Constructs a DNN with 784 input layers, 2 hidden layers of 50 depths each, and 10 output layers for classification.
- Utilizes linear combinations, activation functions (ReLU), and softmax for classification.
- Achieves a validation accuracy of 99% with minimal training and validation loss (approximately 2% and 3%, respectively).
- Attains a test accuracy of 97%, demonstrating robust model performance.
- Hyperparameters, including input layers, hidden layers, output layers, and epochs, are fine-tuned for optimal predictions.

## Objective Function

- Implements the Sparse Categorical Cross-Entropy (Sparse CCE) loss function for effective encoding of categorical variables.
- Particularly useful in classification tasks with more than two classes and sparse target values.
- Describes the training process within an epoch, emphasizing weight and bias updates, loss function values, and training accuracy.

## Optimization Algorithm

- Employs the ADAM (Adaptive Moment Estimation) optimizer.
- ADAM adapts learning rates for each parameter, incorporating momentum and RMSprop techniques.
- Known for efficiency, stability, and fast convergence to optimal solutions.

## Usage

To utilize the MNIST classification system:

1. Ensure required libraries (NumPy, TensorFlow) are installed.
2. Load dataset npz files containing training, validation, and test data.
3. Execute data preprocessing for cleaning and formatting.
4. Train the DNN model on the balanced dataset for accurate predictions.
