# Learning Probability Density Function using GAN

## Dataset
- Feature: NO₂ concentration (x)
- Source: India Air Quality Dataset (Kaggle)

## Transformation
The data is transformed using:
z = x + a_r * sin(b_r * x)

For roll number: 102303480
- a_r = 0.05 * (r mod 7) = 0.3
- b_r = 0.3 * (r mod 5 + 1) = 0.3

## GAN Model
A Generative Adversarial Network (GAN) is used to learn the distribution of z.

- Generator:
  - Input: Noise ~ N(0,1)
  - Output: Fake samples z_f

- Discriminator:
  - Input: Real (z) and Fake (z_f)
  - Output: Real/Fake classification

- Loss: Binary Cross Entropy

## PDF Estimation
After training:
1. Generate samples from the generator
2. Estimate PDF using histogram density estimation

## Results
- Histogram of transformed variable z
- Estimated probability density function

## Observations
- Transformation introduces non-linearity
- GAN learns distribution from data samples
- Mode coverage depends on training
- Training stability affects results

## Requirements
- Python
- NumPy, Pandas, Matplotlib
- TensorFlow / PyTorch
