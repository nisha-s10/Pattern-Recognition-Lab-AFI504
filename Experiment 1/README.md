# 🧪 Experiment 1: Linear and Quadratic Discriminant Analysis (LDA & QDA) from Scratch

## 📌 Overview

This project implements **Linear Discriminant Analysis (LDA)** and **Quadratic Discriminant Analysis (QDA)** from scratch for multi-class pattern classification.

The models are developed without using built-in LDA/QDA functions and are applied to real-world datasets to demonstrate classification performance and decision boundary behavior.

---

## 🎯 Objective

To implement Linear Discriminant Analysis (LDA) and Quadratic Discriminant Analysis (QDA) from scratch and apply them to multi-class classification problems.

---

## 📊 Datasets Used

### 1. Iris Dataset
- Samples: 150
- Features: 4
- Classes: 3 flower species
- Used for visualization of decision boundaries

### 2. MNIST Dataset
- Samples: 70,000 handwritten digits
- Features: 784 pixels per image
- Classes: 10 digits (0–9)
- Used to demonstrate high-dimensional classification

Dataset Sources:
`sklearn.datasets.load_iris`
`sklearn.datasets.fetch_openml`


---

## 🧠 Theory

### Linear Discriminant Analysis (LDA)

LDA assumes that:

- Data from each class follows a Gaussian distribution
- All classes share the same covariance matrix
- Decision boundary is linear

Discriminant Function:

$$ g_k(x) = x^T \Sigma^{-1} \mu_k - \frac{1}{2} \mu_k^T \Sigma^{-1} \mu_k + \log P(\omega_k) $$

---

### Quadratic Discriminant Analysis (QDA)

QDA assumes:

- Gaussian class distributions
- Each class has its own covariance matrix
- Decision boundary is quadratic

Discriminant Function:

$$ g_k(x) = - \frac{1}{2} \log |\Sigma_k| - \frac{1}{2} (x-\mu_k)^T \Sigma_k^{-1} (x-\mu_k) + \log P(\omega_k) $$

---

## ⚙️ Implementation Details

The following components were implemented manually:

- Class-wise mean estimation
- Prior probability calculation
- Covariance matrix computation
- Matrix inversion
- Log-probability calculation
- Class prediction using maximum discriminant score
- Regularization for numerical stability
- Dimensionality reduction using PCA (for MNIST)

No built-in classifiers were used.

---

## 📈 Workflow

1. Import required libraries
2. Load dataset
3. Standardize features
4. Split data into training and testing sets
5. Implement LDA from scratch
6. Implement QDA from scratch
7. Train models
8. Predict class labels
9. Compute classification accuracy
10. Visualize results

---

## 📊 Visualizations Included

- Decision Boundary Plot (Iris dataset)
- PCA Projection Visualization (MNIST dataset)
- Confusion Matrix
- Classification Scatter Plot
- Model Accuracy Output

---

## 📊 Results

Typical performance:

| Dataset | LDA Accuracy | QDA Accuracy |
|--------|-------------|-------------|
| Iris | ~95–100% | ~95–100% |
| MNIST | ~80–88% | ~70–85% |

Observations:

- LDA performs well for both low and high-dimensional data
- QDA provides flexible decision boundaries
- Regularization improves numerical stability
- PCA helps handle high-dimensional datasets

---

## 🧮 Key Concepts Demonstrated

- Multivariate Gaussian modeling
- Bayesian classification
- Linear vs quadratic decision boundaries
- Covariance estimation
- Regularization
- Dimensionality reduction
- Multi-class classification

---

## 🛠 Technologies Used

- Python
- NumPy
- Matplotlib
- Scikit-learn (dataset loading and preprocessing only)

---

## 🚀 How to Run

1. Clone the repository
`git clone <repository-link>`

2. Install dependencies
`pip install numpy matplotlib scikit-learn`


3. Run the notebook or Python script

---

## 🎓 Academic Context

This experiment is part of a **Pattern Recognition Lab** and demonstrates:

- Discriminant analysis techniques
- Probabilistic classification
- Decision boundary modeling
- Practical implementation of statistical classifiers

---

## 👩‍💻 Author

Nisha Singh  
M.tech(AFI) – Pattern Recognition Lab  

---

## 📜 License

This project is intended for academic and educational purposes.
