# Learn Probability Density Functions using Roll-Number-Parameterized Non-Linear Model

## Dataset
- Feature used: **NO₂ concentration (x)**
- Dataset: India Air Quality Dataset  
- Link: https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data

---

## Objective
To learn the probability density function (PDF) of a transformed variable using a non-linear transformation and estimate its parameters.

---

## Step 1: Data Transformation

Each value of \( x \) is transformed into \( z \) using:

z = x + a_r * sin(b_r * x)

Where:
- \( a_r = 0.05 * (r \mod 7) \)
- \( b_r = 0.3 * (r \mod 5 + 1) \)
- \( r \) = University Roll Number

For roll number **102303480**:
- \( r \mod 7 = 6 \) → \( a_r = 0.05 * 6 = 0.3 \)
- \( r \mod 5 = 0 \) → \( b_r = 0.3 * (0 + 1) = 0.3 \)

So,
z = x + 0.3 * sin(0.3 * x)

---

## Step 2: PDF Estimation

The probability density function is defined as:

p̂(z) = c * exp(-λ * (z - μ)²)

Where:
- \( μ \) = mean of z
- \( λ \) = spread parameter
- \( c \) = normalization constant

### Parameter Estimation

The parameters are estimated from the transformed data \( z \):

- \( μ \) = Mean of z
- \( σ^2 \) = Variance of z
- \( λ = 1 / (2 * σ^2) \)
- \( c = \sqrt{λ / π} \)

---

## Step 3: Output

The following parameters are computed:

- Mean (\( μ \)) = [Your Value]
- Lambda (\( λ \)) = [Your Value]
- Constant (\( c \)) = [Your Value]

These values are submitted as required.

---

## Results

- Transformed variable \( z \) is computed
- Histogram of \( z \) is plotted
- Estimated PDF is visualized using the learned parameters

---

## Observations

- Non-linear transformation introduces variation in data
- The distribution of \( z \) approximates a Gaussian-like shape
- Estimated PDF fits the data reasonably well
- Accuracy depends on parameter estimation

---

## Requirements

- Python
- NumPy
- Pandas
- Matplotlib

---
