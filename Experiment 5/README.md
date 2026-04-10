# Experiment 5: Logistic Regression Classifier Using Gradient Descent Optimization from Scratch

## Overview

This project implements a **Logistic Regression classifier from scratch** using **Gradient Descent optimization** without using any built-in machine learning models.

The classifier is trained on the **Digits dataset**, a multi-class dataset of handwritten digit images. The experiment demonstrates how gradient descent minimizes the loss function and how model performance is evaluated using standard classification metrics and visualization techniques.

---

## Objective

To implement Logistic Regression from scratch using Gradient Descent optimization and evaluate classification performance using visualization techniques such as loss curves, confusion matrix, and ROC curve.

---

## Dataset

### Digits Dataset

The experiment uses the **Digits dataset**, which contains images of handwritten digits.

**Dataset Characteristics**

* Number of samples: **1797**
* Number of features: **64**
* Image size: **8 × 8 pixels**
* Number of classes: **10 (digits 0–9)**
* Feature type: Numerical pixel intensity values

Dataset Source:

```python
from sklearn.datasets import load_digits
```

---

## Theory

### Logistic Regression

Logistic Regression is a supervised learning algorithm used for classification. It models the probability of a class using the **sigmoid function**.

---

### Sigmoid Function

$$
\sigma(z) =
\frac{1}{1 + e^{-z}}
$$

---

### Logistic Regression Model

$$
h_\theta(x) =
\frac{1}{1 + e^{-\theta^T x}}
$$

---

### Cost Function (Log Loss)

The loss function used in Logistic Regression is the binary cross-entropy loss:

$$
J(\theta) =

* \frac{1}{m}
  \sum_{i=1}^{m}
  \left[
  y_i \log(\hat{y}_i)

-

(1 - y_i)
\log(1 - \hat{y}_i)
\right]
$$

---

### Gradient Descent Update Rule

The model parameters are updated iteratively using Gradient Descent:

$$
\theta =
\theta
------

\alpha
\frac{\partial J(\theta)}{\partial \theta}
$$

Where:

* $\alpha$ = learning rate
* $J(\theta)$ = cost function
* $\theta$ = model parameters

---

## Implementation Steps

1. Import required libraries
2. Load Digits dataset
3. Standardize feature values
4. Split dataset into training and testing sets
5. Add bias term to input features
6. Initialize model weights
7. Implement sigmoid function
8. Train model using Gradient Descent
9. Track loss during training
10. Generate predictions
11. Evaluate model performance
12. Visualize results

---

## Visualizations Generated

The experiment produces the following visualizations:

### 1. Loss vs Iterations

Shows convergence of Gradient Descent optimization.

### 2. Confusion Matrix

Displays classification performance across classes.

### 3. ROC Curve

Plots True Positive Rate vs False Positive Rate.

### 4. Probability Distribution

Shows predicted probability separation between classes.

### 5. Accuracy vs Threshold

Demonstrates how classification accuracy changes with decision threshold.

---

## Performance Metrics

The following metrics are computed:

* Accuracy
* Sensitivity (True Positive Rate)
* Specificity (True Negative Rate)
* Area Under Curve (AUC)

---

## Example Output

Dataset shape:

```text
(1797, 64)
```

Typical performance:

```text
Accuracy: 0.92 – 0.97
AUC: 0.95 – 0.99
```

---

## Key Concepts Demonstrated

* Logistic Regression
* Sigmoid activation function
* Gradient Descent optimization
* Loss minimization
* Probability-based classification
* Threshold-based decision making
* Model evaluation using ROC and AUC

---

## Technologies Used

* Python
* NumPy
* Matplotlib
* Scikit-learn (dataset loading and preprocessing only)

---

## How to Run

1. Clone the repository

```bash
git clone <repository-link>
```

2. Install required packages

```bash
pip install numpy matplotlib scikit-learn
```

3. Run the notebook or Python script.

---

## Conclusion

Logistic Regression was successfully implemented from scratch using Gradient Descent optimization. The model demonstrated strong classification performance on the Digits dataset, and visualization of the loss curve confirmed proper convergence of the optimization process.

---

## 👩‍💻 Author

Nisha Singh  
M.Tech (AFI) – Pattern Recognition Lab 
