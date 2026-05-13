# CNN-Based Surface Defect Classification

## Project Overview

This project builds a Convolutional Neural Network (CNN) model to classify surface defect images into four categories:

- Normal
- Dent
- Scratch
- Stain

The objective is to automatically identify product surface defects using deep learning and computer vision.

---

## Dataset Source

The dataset used in this project was provided as part of the academic assignment materials. The data set are taken from:
- `images/normal/`
- `images/scratch/`
- `images/dent/`
- `images/stain/`

---

## Problem Identification

This dataset represents an Image Classification problem.

Each image belongs to exactly one defect category:

- normal
- dent
- scratch
- stain

Since the dataset contains class folders and no bounding boxes or segmentation masks, image classification is the most appropriate problem type.

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

Total Images: **480**

---

## Image Dimensions

All images have dimensions:

**96 × 96 pixels**

---

## Dataset Balance

Each class contains an equal number of images, so the dataset is balanced.

---

## Image Preprocessing

The following preprocessing steps were performed:

- Resized images to 96 × 96 pixels
- Normalized pixel values from 0–255 to 0–1
- Split dataset into training and testing sets
- Applied data augmentation for better generalization

Dataset split:

- Training Images: **384**
- Testing Images: **96**

---

## CNN Model Architecture

The CNN model was implemented using TensorFlow and Keras in Python.

### Architecture:

1. Convolution Layer
2. ReLU Activation
3. Max Pooling Layer
4. Flatten Layer
5. Dense Layer
6. Output Layer (Softmax)

### Optimizer

Adam

### Loss Function

Categorical Crossentropy

---

## Model Performance

### Training Performance

- Accuracy: **83.85%**
- Loss: **0.4774**

### Validation Performance

- Accuracy: **83.33%**
- Loss: **0.4854**

### Testing Performance

- Accuracy: **86.46%**
- Loss: **0.4733**

---

## Observations

The CNN model successfully learned visual defect patterns from the images.

The model improved significantly during training and achieved strong testing performance.

Training and validation accuracy remained close, which indicates good generalization and minimal overfitting.

Some confusion between defect classes was observed because dents, scratches, and stains can appear visually similar.

---

# CNN Concept Explanation

## What is convolution?

Convolution is the process where filters scan across an image to detect important visual patterns such as edges, textures, and defects.

## Why is pooling used?

Pooling reduces the size of feature maps while keeping important information. It reduces computational cost and helps prevent overfitting.

## Why is ReLU used?

ReLU introduces non-linearity, allowing the network to learn complex visual patterns efficiently.

## Why are CNNs better than regular neural networks for image data?

CNNs preserve spatial relationships between pixels and automatically learn image features, making them highly effective for image classification.

---
# Business Use Case

## Manufacturing Industry

This solution can be used in manufacturing for automated quality inspection.

The model can detect:

- Surface scratches
- Dents
- Stains
- Product defects

### Business Benefits

- Reduced manual inspection
- Faster quality control
- Lower operational costs
- Improved product quality
- Higher customer satisfaction
