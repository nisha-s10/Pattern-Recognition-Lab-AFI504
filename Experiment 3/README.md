# 🧪 Experiment 3: Maximum Likelihood (MLE) and Maximum A Posteriori (MAP) Estimation for Gaussian Models

## 📌 Overview

This project demonstrates the implementation of:

- Maximum Likelihood Estimation (MLE)
- Maximum A Posteriori (MAP) Estimation

for Gaussian models using a real-world dataset.

All parameter estimation is implemented **from scratch**, without using built-in estimation functions.

---

## 📊 Dataset Used

Wine Dataset  
Source: `sklearn.datasets.load_wine`

- Total Samples: 178
- Features: 13 continuous features
- Classes: 3 (used only for dataset context)
- This experiment focuses on parameter estimation, not classification.

---

## 🎯 Objective

To estimate the mean and variance parameters of a Gaussian distribution using:

- Maximum Likelihood Estimation (MLE)
- Maximum A Posteriori Estimation (MAP)

and analyze the effect of prior information on parameter estimation.

---

## 🧠 Theory

### Gaussian Distribution

For a Gaussian random variable:

X ~ N(μ, σ²)

---

### 🔹 Maximum Likelihood Estimation (MLE)

MLE estimates parameters by maximizing the likelihood function:

$$
\hat{\mu}_{MLE} = \frac{1}{N} \sum_{i=1}^{N} x_i
$$

$$
\hat{\sigma}_{MLE}^2 = \frac{1}{N} \sum_{i=1}^{N} (x_i - \hat{\mu})^2
$$

MLE depends only on observed data.

---

### 🔹 Maximum A Posteriori (MAP)

MAP incorporates prior belief about parameters.

Assume prior:

μ ~ N(μ₀, τ²)

Then the MAP estimate becomes:

$$
\hat{\mu}_{MAP} =
\frac{\frac{N}{\sigma^2}\bar{x} + \frac{1}{\tau^2}\mu_0}
{\frac{N}{\sigma^2} + \frac{1}{\tau^2}}
$$

MAP shrinks the estimate toward the prior mean.

---

## ⚙️ Implementation Details

Steps performed:

1. Load Wine dataset
2. Select one feature for Gaussian modeling
3. Standardize data
4. Compute MLE mean and variance
5. Compute MAP mean using Gaussian prior
6. Compare estimates for:
   - Full dataset
   - Small sample subset
7. Visualize:
   - Histogram of data
   - Gaussian curves (MLE vs MAP)
   - Log-likelihood function
   - Log-posterior function
   - Effect of prior strength

All computations are performed manually using NumPy.

---

## 📈 Visualizations Included

- Histogram of standardized feature
- Gaussian curve (MLE)
- Gaussian curve (MAP)
- Log-Likelihood vs Mean plot
- Log-Posterior vs Mean plot
- Small sample MLE vs MAP comparison
- Prior variance impact visualization

---

## 📊 Key Observations

- For large sample sizes:
  MAP ≈ MLE (likelihood dominates prior)

- For small sample sizes:
  MAP shifts toward prior mean (shrinkage effect)

- As N → ∞:
  MAP → MLE

This demonstrates the theoretical relationship between likelihood and posterior estimation.

---

## 🧮 Concepts Demonstrated

- Likelihood maximization
- Bayesian parameter estimation
- Effect of prior distribution
- Shrinkage behavior
- Bias-variance tradeoff
- Log-likelihood and log-posterior optimization

---

## 🛠 Technologies Used

- Python
- NumPy
- Matplotlib
- Scikit-learn (dataset loading only)

---

## 🚀 How to Run

1. Clone the repository
2. Install required packages:

pip install numpy matplotlib scikit-learn

3. Run the notebook or Python script.

---

## 🎓 Academic Context

This experiment is part of a Pattern Recognition lab and focuses on understanding:

- Parameter estimation techniques
- Differences between frequentist and Bayesian approaches
- Practical behavior of MLE and MAP estimators

---

## 👩‍💻 Author

Nisha Singh  
B.Tech – Pattern Recognition Lab  

---

## 📜 License

This project is intended for academic and educational use.
