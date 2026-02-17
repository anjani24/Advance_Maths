% ============================================================
% README: Learning Probability Density Function using GAN
% ============================================================

% Dataset:
% Feature used: NO2 concentration (x)
% Source: India Air Quality Dataset (Kaggle)

% ------------------------------------------------------------
% Step 1: Transformation
% ------------------------------------------------------------
% The data is transformed using:
% z = x + a_r * sin(b_r * x)

% For roll number: 102303480
% a_r = 0.05 * (r mod 7) = 0.3
% b_r = 0.3 * (r mod 5 + 1) = 0.3

% ------------------------------------------------------------
% Step 2: GAN Model
% ------------------------------------------------------------
% A Generative Adversarial Network (GAN) is used to learn the 
% unknown distribution of z.

% Generator:
% Input  : Noise ~ N(0,1)
% Output : Fake samples z_f

% Discriminator:
% Input  : Real samples (z) and fake samples (z_f)
% Output : Probability (real/fake)

% Loss Function:
% Binary Cross Entropy

% ------------------------------------------------------------
% Step 3: PDF Estimation
% ------------------------------------------------------------
% After training:
% 1. Generate samples using the generator
% 2. Estimate PDF using histogram density estimation

% ------------------------------------------------------------
% Results:
% ------------------------------------------------------------
% - Histogram of transformed data plotted
% - PDF estimated from generated samples
% - Visualization shows distribution learning

% ------------------------------------------------------------
% Observations:
% ------------------------------------------------------------
% - Transformation introduces non-linearity
% - GAN learns the distribution from data samples
% - Training stability affects performance
% - Mode coverage depends on generator quality

% ------------------------------------------------------------
% Requirements:
% ------------------------------------------------------------
% Python / MATLAB
% NumPy, Pandas, Matplotlib
% TensorFlow / PyTorch (for GAN)

% ============================================================
