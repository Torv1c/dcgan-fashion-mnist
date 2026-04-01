# Deep Convolutional GAN (DCGAN): Fashion MNIST

## Project Overview
This repository contains a Deep Convolutional Generative Adversarial Network (DCGAN) built from scratch to generate synthetic, high-fidelity images of clothing items. 

Unlike standard classification models, this project explores the generative domain by pitting two neural networks against each other:
* **The Generator:** Learns to create increasingly realistic images from random noise (latent space).
* **The Discriminator:** Acts as an AI detective, learning to distinguish between real images from the Fashion MNIST dataset and the fake images produced by the Generator.

Through this adversarial zero-sum game, the Generator eventually learns to produce images that are virtually indistinguishable from real data.

## Tech Stack & Architecture
* **Framework:** `TensorFlow 2.x` / `Keras`
* **Custom Training:** Implemented via `tf.GradientTape` for manual backpropagation and fine-grained gradient calculation.
* **Generator Architecture:** Utilizes `Conv2DTranspose` for upsampling, `BatchNormalization` for stability, and `tanh` activation to output normalized pixel values [-1, 1].
* **Discriminator Architecture:** A Convolutional Neural Network (CNN) classifier utilizing `LeakyReLU` and `Dropout` layers to prevent overfitting.
* **Hardware:** Pipeline optimized for parallel processing on NVIDIA T4 GPUs.

## Visualizing the Evolution
One of the most fascinating aspects of training a GAN is watching the Generator's learning process. What starts as pure static noise gradually morphs into recognizable spatial structures (shirts, shoes, bags) as the epochs progress.

### Early Stages (Noise to Shapes)
*(In the beginning, the Generator is simply mapping random noise to pixels, slowly figuring out the basic outlines).*
<img width="581" height="593" alt="image" src="https://github.com/user-attachments/assets/dcf10b37-0d8e-4d29-a7a3-ca457854e97b" />


### Final Stages (Synthetic Generation)
*(After extended training, the network successfully imagines and renders clothing items that do not exist in the real dataset).*
<img width="581" height="593" alt="image" src="https://github.com/user-attachments/assets/5bb31fcb-4cf4-4990-b5de-38fca21d1f10" />


---
**Author:** Victor Cesar de Mecê Prando
**LinkedIn:** [victor-prando1](https://www.linkedin.com/in/victor-prando1/)
