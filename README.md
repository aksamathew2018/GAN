# 🧠 Generative Adversarial Network (GAN) - MNIST

## 📌 Overview
This project implements a **Generative Adversarial Network (GAN)** using **TensorFlow 2.x (Keras API)** to generate handwritten digit images similar to the MNIST dataset.

The GAN consists of two neural networks:
- **Generator**: Generates fake images from random noise
- **Discriminator**: Classifies images as real or fake

Both networks are trained together in an adversarial manner.

---

## 🎯 Objective
- To build and train a GAN model
- To generate realistic 28×28 grayscale digit images
- To analyze training behavior using loss curves and generated outputs

---

## 📂 Dataset
- **MNIST Dataset**
- 60,000 training images
- Image size: 28×28 (grayscale)

---

## ⚙️ Preprocessing
- Normalized pixel values to range **[-1, 1]**
- Reshaped images to **(28, 28, 1)**
- Used TensorFlow Dataset API for batching and shuffling

---

## 🏗️ Model Architecture

### 🔹 Generator
- Input: 100-dimensional noise vector
- Dense layer → reshape (7×7×256)
- Conv2DTranspose layers for upsampling
- Activation: LeakyReLU
- Output: 28×28×1 image (tanh activation)

### 🔹 Discriminator
- Input: 28×28 image
- Convolutional layers with stride
- Activation: LeakyReLU
- Dropout for regularization
- Output: Single neuron (real/fake classification)

---

## 📉 Loss Functions
- Binary Cross-Entropy Loss

- **Generator Loss**: Measures ability to fool discriminator  
- **Discriminator Loss**: Measures ability to classify real vs fake  

---

## 🚀 Training Details
- Optimizer: Adam (learning rate = 1e-4)
- Batch size: 64 / 128
- Epochs: 10–50 (adjustable)
- Noise dimension: 100

---

## 📊 Results
- Generator loss stabilizes over time
- Discriminator loss fluctuates as both networks compete
- Generated images improve gradually across epochs

---

## 🖼️ Outputs
- Grid of generated images displayed every few epochs
- Loss curves for generator and discriminator

---

## ⚠️ Challenges
- Training instability
- Slow convergence
- Balancing generator and discriminator
- Mode collapse (similar outputs)

---


## ▶️ How to Run

1. Install dependencies:
```bash
pip install tensorflow matplotlib
