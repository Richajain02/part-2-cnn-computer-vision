# CNN-Based Surface Defect Classification

## Project Overview

This project implements a Convolutional Neural Network (CNN) to classify product surface images into defect categories.

The objective is to automatically identify surface conditions such as:

- Normal
- Dent
- Scratch
- Stain

This project demonstrates how CNNs can learn visual defect patterns from images.

---

## Dataset Source

The dataset used in this project was provided as part of the academic assignment materials. Dataset are taken from:
`images/normal/`
`images/scratch/`
`images/dent/`
`images/stain/`

---

## Problem Identification

This dataset represents an image classification problem.

The dataset contains images grouped into four folders:

- normal
- dent
- scratch
- stain

Each image belongs to exactly one class. Since no bounding boxes or segmentation masks are provided, image classification is the most appropriate computer vision task.

---

## Dataset Exploration

### Number of Classes

4 classes:

- normal
- dent
- scratch
- stain

### Images per Class

| Class | Number of Images |
normal: 120 images
dent: 120 images
scratch: 120 images
stain: 120 images

Total Images: 480

### Image Dimensions

All images have dimensions:

96 × 96 pixels

### Dataset Balance

Each class contains the same number of images, so the dataset is balanced.

---

## Image Preprocessing

The following preprocessing steps were performed:

- Images resized to 96 × 96 pixels
- Pixel normalization (0–255 scaled to 0–1)
- Training/testing split using 80:20 ratio
- Data augmentation:
  - Rotation
  - Horizontal flipping
  - Zooming

Dataset split:

- Training Images: 384
- Testing Images: 96

---

## CNN Model Architecture

The CNN model consists of:

1. Convolution Layer (32 filters, 3×3)
2. ReLU Activation Function
3. Max Pooling Layer
4. Flatten Layer
5. Dense Layer (128 neurons)
6. Output Layer (4 neurons with Softmax)

### Optimizer

Adam

### Loss Function

Categorical Crossentropy

---

## Model Performance

### Training Performance

- Accuracy: 76.56%
- Loss: 0.7212

### Validation Performance

- Accuracy: 76.04%
- Loss: 0.7531

### Testing Performance

- Accuracy: 73.96%
- Loss: 0.7647

---

## Observations

The CNN model successfully learned defect-related visual patterns.

The model improved from approximately 25% accuracy (random guessing) to nearly 76% accuracy.

Some confusion between classes was observed because dents, scratches, and stains share visually similar patterns.

No significant overfitting was observed because training and validation accuracy remained close.

---

# CNN Concept Explanation

## What is convolution?

Convolution uses small filters to scan an image and detect features such as edges, textures, and defect patterns.

## Why is pooling used?

Pooling reduces image size while preserving important features. It reduces computation and helps prevent overfitting.

## Why is ReLU used?

ReLU introduces non-linearity, allowing the CNN to learn complex image patterns efficiently.

## Why are CNNs better than regular neural networks for images?

CNNs preserve spatial information and automatically learn image features, making them highly effective for image classification tasks.

---

# Business Use Case

## Manufacturing Industry

This solution can be used in manufacturing for automated quality inspection.

The model can detect:

- Surface scratches
- Dents
- Stains
- Product defects

Business benefits:

- Reduced manual inspection
- Faster quality control
- Lower operational costs
- Improved product quality
