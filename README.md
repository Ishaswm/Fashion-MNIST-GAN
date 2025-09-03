# Fashion MNIST GAN

This project implements a **Generative Adversarial Network (GAN)** trained on the **Fashion-MNIST** dataset using TensorFlow and Keras. The goal is to generate realistic fashion images (shirts, shoes, bags, etc.) from random noise vectors.

---

## Overview

The project builds and trains:
- A **Generator** that creates new fashion images from random noise.
- A **Discriminator** that distinguishes between real Fashion-MNIST images and generated ones.
- A **custom training loop** for adversarial training, with loss tracking and image generation at each epoch.

---

## Features

- Data preprocessing and batching using **TensorFlow Datasets (TFDS)**  
- **Generator model** with Dense, Conv2D, and UpSampling2D layers  
- **Discriminator model** with Conv2D, LeakyReLU, and Dropout layers  
- Custom **FashionGAN class** with overridden `train_step`  
- Training monitored with a **custom callback** that saves generated images at each epoch  
- Loss visualization for both generator and discriminator  
- Model saving (`generator.h5`, `discriminator.h5`) for reuse  

---

## Project Structure
- `Fashion_GAN_.ipynb` - Main Colab Notebook
- `images/` - Generated images saved during training
- `generator.h5` - Saved generator model
- `discriminator.h5` - Saved discriminator model

---

## Requirements

The following libraries are required (already included in Colab):

- TensorFlow
- Matplotlib
- TensorFlow Datasets
- NumPy
- Ipywidgets

Install (if running locally):

```bash
pip install tensorflow matplotlib tensorflow-datasets ipywidgets
```
---

## Results

- Generator progressively learns to create more realistic fashion images  
- Training history of discriminator and generator loss is visualized  
- Example generated images are saved after each epoch for inspection  

<img width="500" height="300" alt="Screenshot 2025-09-03 at 11 14 18 PM" src="https://github.com/user-attachments/assets/c2947c72-6149-432e-8508-e2dbfddbd17c" />


---

## Future Improvements

- Experiment with different architectures (DCGAN, Conditional GANs)  
- Try higher resolution datasets beyond Fashion-MNIST  
- Implement FID/IS scores for quantitative evaluation  
- Add latent space interpolation for smooth transitions between generated images  

---

## References

- [Fashion-MNIST Dataset](https://github.com/zalandoresearch/fashion-mnist)  
- [Generative Adversarial Networks (Goodfellow et al.)](https://arxiv.org/abs/1406.2661)  
- [TensorFlow Documentation](https://www.tensorflow.org/)  
- [Keras Documentation](https://keras.io/)  
