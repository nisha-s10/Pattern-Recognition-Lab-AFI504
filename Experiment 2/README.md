# 🧪 Experiment 2: Gaussian Bayesian Classifier (From Scratch)

## 📌 Overview

This project implements a **Bayesian Classifier using Gaussian Class-Conditional Probability Density Functions** from scratch (without using any inbuilt classifier such as GaussianNB).

The classifier is applied to the **Breast Cancer Wisconsin Dataset** to perform binary classification (Malignant vs Benign).

---

## 🎯 Objective

To implement a Gaussian Bayesian classifier from scratch using Bayes' Theorem and apply it to a real-world medical dataset.

---

## 📊 Dataset

**Breast Cancer Wisconsin Dataset**

- Total Samples: 569  
- Features: 30 numerical features  
- Classes:
  - 0 → Malignant
  - 1 → Benign  

Dataset Source: `sklearn.datasets.load_breast_cancer`

---

## 🧠 Theory

The classifier is based on **Bayes’ Theorem**:

$$
P(\omega_k \mid x) = 
\frac{P(x \mid \omega_k) \, P(\omega_k)}
{P(x)}
$$

Where:

- $P(\omega_k \mid x)$ → Posterior probability  
- $P(x \mid \omega_k)$ → Likelihood  
- $P(\omega_k)$ → Prior probability  
- $P(x)$ → Evidence (normalizing constant)

---

### Gaussian Class-Conditional Density

$$
P(x \mid \omega_k) =
\frac{1}{\sqrt{2\pi\sigma^2}}
\exp\left(
-\frac{(x - \mu)^2}{2\sigma^2}
\right)
$$

---

### Decision Rule

$$
\text{Assign } x \text{ to class } 
\omega_k \text{ if } 
P(\omega_k \mid x) 
= \max_j P(\omega_j \mid x)
$$
Assign sample \(x\) to the class with the **maximum posterior probability**.

---

## ⚙️ Implementation Details

The classifier is implemented from scratch using:

- Mean estimation per class
- Variance estimation per class
- Prior probability computation
- Log-likelihood computation for numerical stability
- Posterior maximization

No inbuilt classification functions were used.

---

## 📈 Workflow

1. Import required libraries
2. Load dataset
3. Standardize features
4. Train-test split
5. Implement Gaussian Bayesian Classifier
6. Train model
7. Evaluate using accuracy
8. Generate confusion matrix
9. Visualize classification using PCA
10. Plot decision boundary

---

## 📊 Results

- High classification accuracy (~90–97%)
- Clear separation between malignant and benign classes
- Confusion matrix confirms strong predictive performance
- PCA visualization shows distinct class clusters

---

## 📷 Visualizations Included

- Accuracy Output
- Confusion Matrix
- PCA-based 2D Classification Plot
- Decision Boundary Visualization

---

## 📦 Technologies Used

- Python
- NumPy
- Matplotlib
- Scikit-learn (for dataset loading and preprocessing only)

---

## 🚀 How to Run

1. Clone this repository
2. Install required packages:

`pip install numpy matplotlib scikit-learn`


3. Run the notebook or Python script.

---

## 🎓 Academic Purpose

This experiment demonstrates:

- Bayesian decision theory
- Gaussian probability density modeling
- Log-likelihood computation
- Classification without built-in ML models
- Visualization of high-dimensional data using PCA

---

## 👩‍💻 Author

Nisha Singh  
M.tech(AFI) – Pattern Recognition Lab  

---

## 📜 License

This project is for academic and educational purposes.
