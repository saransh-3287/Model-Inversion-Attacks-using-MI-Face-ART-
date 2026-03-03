# Model Inversion Attack on AT&T Face Dataset using MI-Face (ART)

## Project Overview

This project implements a **Model Inversion Attack** using the MI-Face algorithm from the Adversarial Robustness Toolbox (ART) to reconstruct training data representations from a trained neural network.

The attack is performed on the **AT&T (ORL) Face Dataset**, which contains 40 subjects with 10 images each.

The goal is to demonstrate how trained neural networks can leak sensitive training information through output predictions.

---

## Dataset

- Dataset: AT&T Face Dataset (ORL Database of Faces)
- Number of Subjects: 40
- Images per subject: 10
- Image Size: 92 × 112 (grayscale)

The dataset contains frontal face images with variations in expression and lighting.

---

## Model Architecture

A custom Convolutional Neural Network (CNN) was implemented:

- 2 Convolutional layers
- MaxPooling
- Fully Connected layers
- Output layer with 40 classes

The model was trained to classify the identity of each subject.

---

## Attack Method

The **MI-Face algorithm** from ART was used to perform model inversion.

The attack:

- Does not require access to original training images
- Uses model gradients
- Optimizes input pixels to maximize class confidence
- Produces reconstructed class prototypes
