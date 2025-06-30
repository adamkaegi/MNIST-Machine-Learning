# MNIST Classification with VGG11 and Multiclass Perceptron

This repository contains two Jupyter Notebooks that explore multiclass classification on the MNIST digit dataset using two distinct approaches:

1. A **Multiclass Perceptron**, implemented through both reduction-based and direct multiclass formulations.
2. A **VGG11 Convolutional Neural Network (CNN)** trained on both original and augmented MNIST data, with robustness testing.

---

## Contents

### `MultiClassPerceptron.ipynb` – Multiclass Perceptron Approaches

This notebook implements and evaluates perceptron-based methods for multiclass classification on the MNIST dataset.

#### Key Features:
- **One-vs-All Perceptron**:
  - Trains 10 binary perceptrons, one for each digit class.
  - Each perceptron learns to distinguish its digit from all others.
  
- **Direct Multiclass Perceptron**:
  - On a misclassification, updates the weight vectors for both predicted and correct classes.

- Trains both models for **10 epochs**.
- Reports final **training and test errors**.
---

### `NeuralNetworkVGG11.ipynb` – VGG11 with Data Augmentation and Robustness Testing

This notebook trains a deep CNN model (VGG11) on MNIST with data augmentation and evaluates its robustness to image transformations.

#### Key Features:
- **Implemented VGG11 Architecture**:
  - Adapted VGG11 architecture for grayscale MNIST images.
  - Trained on resized 32×32 inputs.

- **Tested Robustness to Input Variations**:
  - Evaluated model performance on:
    - **Horizontally flipped** images.
    - **Vertically flipped** images.
    - Images with **Gaussian noise** at varying intensities.

- **Data Augmentation with Rotations**:
  - Augmented training data by rotating each image **±10°**.
  - Retrained the VGG11 model on the **augmented dataset**.

- **Post-Augmentation Robustness Testing**:
  - Re-evaluated the retrained model on:
    - Flipped images.
    - Noisy images.
  - Compared performance with the baseline (non-augmented) model.
