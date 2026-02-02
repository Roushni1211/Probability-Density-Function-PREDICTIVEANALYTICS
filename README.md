# Probability Density Function Learning using NO₂ Data

## 📌 Objective
The objective of this assignment is to learn the parameters of a probability density function using a roll-number-parameterized nonlinear transformation on NO₂ air quality data.

---

## 📊 Dataset
- Dataset: India Air Quality Data
- Source: Kaggle
- Feature Used: NO₂ concentration (`no2` column)

---

## 🔢 Roll Number Parameters
University Roll Number: **102316119**

Using the given formulas:
- aᵣ = 0.05 × (r mod 7) = **0.15**
- bᵣ = 0.3 × (r mod 5 + 1) = **1.5**

---

## 🔁 Data Transformation
Each value of NO₂ (x) is transformed using the nonlinear function:

z = x + aᵣ sin(bᵣ x)

This transformation introduces nonlinearity based on the roll number.

---

## 📈 Probability Density Function
The transformed variable z is modeled using the following PDF:

p̂(z) = c · exp(−λ (z − μ)²)

Where:
- μ → mean
- λ → parameter related to variance
- c → normalization constant

---

## 🧠 Parameter Estimation Methodology
- μ is estimated as the sample mean of z
- Variance (σ²) is calculated from z
- λ is computed as 1 / (2σ²)
- c is computed as √(λ / π)

This approach assumes a Gaussian-like distribution.

---

## 📋 Results

| Parameter | Value |
|---------|-------|
| μ (mean) | Computed from data |
| λ (lambda) | Computed from variance |
| c (constant) | Computed using normalization |

---

## 📉 Result Graph
- Histogram of transformed variable z
- Learned probability density function plotted over the histogram

The graph shows that the learned PDF closely fits the distribution of the transformed data.

---

## 🛠 Tools Used
- Google Colab
- Python
- NumPy
- Pandas
- Matplotlib

---

## 📎 Files Included
- `PDF_Estimation_NO2_Roll102316119.ipynb` – Complete solution notebook
- `README.md` – Explanation of methodology and results
