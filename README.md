# MNIST Classification with MLP and CNN
An image classification project comparing **Multilayer Perceptron (MLP)** and **Convolutional Neural Network (CNN)** approaches on the **MNIST handwritten digits dataset**, using **PyTorch**.

## Project Overview
In this project, I implemented **a multilayer perceptron (MLP) from scratch** using NumPy and then **built and optimized a convolutional neural network (CNN) in PyTorch** to classify handwritten digits.

The project demonstrates how different neural network architectures influence classification performance, while also covering model training with loss functions and optimizers, as well as defining neural network architectures in PyTorch.


This project was completed as part of the **Machine Learning and Neural Networks** course in the **M.Sc. in Neuroscience & Data Science** program at **Bar-Ilan University**.

## Dataset

This project uses the **MNIST** dataset, a standard benchmark in computer vision containing grayscale images of handwritten digits from `0` to `9`.

- Image size: `28x28`
- Number of classes: `10`
- Task: multiclass image classification
<img width="989" height="273" alt="image" src="https://github.com/user-attachments/assets/0e2cad6f-f712-4369-93bc-a6ec0a27af6c" />

## Model Architectures

### 1. MLP (Multilayer Perceptron)
A fully connected feedforward network featuring a 784-unit input layer, two hidden layers (128 and 64 units, respectively) using ReLU activations, and a final 10-unit output layer with a log-softmax activation for digit classification.

<img width="787" height="397" alt="image" src="https://github.com/user-attachments/assets/80ba97e3-7e92-4907-8426-b8ba5e14e259" />

### 2. CNN (Convolutional Neural Network)
A Convolutional Neural Network utilizing two 5x5 convolutional layers (10 and 20 channels, respectively), each followed by 2x2 Max Pooling and ReLU activations. The extracted features are passed through two fully connected hidden layers (320 and 50 units) before a final 10-unit output layer for digit classification.

### 3. Improved CNN
An optimized Convolutional Neural Network incorporating Batch Normalization for training stability and 1x1 convolutions for feature projection.

Conv2D (10 5x5 filters) ➔ BatchNorm2D ➔ Max Pooling (2x2) ➔ ReLU ➔ Conv2D (20 5x5 filters) ➔ BatchNorm2D ➔ Max Pooling (2x2) ➔ ReLU ➔ Conv2D (20 1x1 filters) ➔ BatchNorm2D ➔ Fully Connected (50 units) ➔ BatchNorm1D ➔ ReLU ➔ Output (10 classes, Log-Softmax)

## Performance & Results
* **MLP Validation Accuracy:** 88.25%
* **CNN Validation Accuracy:** 95.9%
* **Improved CNN Validation Accuracy:** 98.9%

## Conclusion
The CNN architecture demonstrated superior performance and faster convergence due to its ability to capture spatial hierarchies and local pixel dependencies within the image data, which the flattened MLP approach discards.
