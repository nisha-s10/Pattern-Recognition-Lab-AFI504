# Experiment 4: Binary Hypothesis Testing Using Likelihood Ratio Test and ROC Curve Analysis

## Objective

To implement Binary Hypothesis Testing using the Likelihood Ratio Test (LRT) and evaluate classifier performance using Receiver Operating Characteristic (ROC) curve analysis.

---

## Dataset

This experiment uses the **Diabetes dataset** containing medical measurements of patients.

**Dataset Characteristics:**

* Number of samples: **442**
* Number of features: **10**
* Target type: Continuous (converted to binary classification)
* Classes:

  * **0** → Below median disease progression
  * **1** → Above median disease progression

Binary labels are created using:

$$
y_{binary} =
\begin{cases}
1 & \text{if } y > \text{median}(y) \
0 & \text{otherwise}
\end{cases}
$$

---

## Theory

### Binary Hypothesis Testing

Two competing hypotheses are defined:

$$
H_0 : \text{Class 0}
$$

$$
H_1 : \text{Class 1}
$$

---

### Likelihood Ratio Test (LRT)

The likelihood ratio is defined as:

$$
\Lambda(x) =
\frac{p(x \mid H_1)}
{p(x \mid H_0)}
$$

To improve numerical stability, the logarithmic form is used:

$$
\log \Lambda(x) =
\log p(x \mid H_1)
------------------

\log p(x \mid H_0)
$$

Decision rule:

$$
\text{Decide } H_1
\quad \text{if} \quad
\log \Lambda(x) > \eta
$$

where:

* $\eta$ is the decision threshold

---

### Gaussian Probability Density Function

$$
p(x) =
\frac{1}{\sqrt{2\pi\sigma^2}}
\exp
\left(
-\frac{(x-\mu)^2}{2\sigma^2}
\right)
$$

---

### Performance Evaluation Metrics

#### Accuracy

$$
Accuracy =
\frac{TP + TN}
{TP + TN + FP + FN}
$$

---

#### Sensitivity (True Positive Rate)

$$
TPR =
\frac{TP}
{TP + FN}
$$

---

#### Specificity (True Negative Rate)

$$
TNR =
\frac{TN}
{TN + FP}
$$

---

#### Area Under Curve (AUC)

The area under the ROC curve measures classifier performance:

$$
AUC =
\int_0^1 TPR(FPR), d(FPR)
$$

---

## Implementation Steps

1. Load dataset
2. Convert target into binary classes
3. Standardize features
4. Split dataset into training and testing sets
5. Estimate Gaussian parameters using Maximum Likelihood Estimation
6. Compute Log Likelihood Ratio
7. Evaluate classifier using threshold-based decision rule
8. Generate ROC curve
9. Compute Area Under Curve (AUC)
10. Calculate performance metrics

---

## Visualizations Generated

The following visualizations are produced:

### 1. Score Distribution

Shows separation between Class 0 and Class 1 using Log Likelihood Ratio.

### 2. ROC Curve

Displays True Positive Rate vs False Positive Rate.

Includes:

* Random classifier baseline
* AUC value

### 3. Confusion Matrix

Shows classification performance.

Structure:

$$
\begin{bmatrix}
TN & FP \
FN & TP
\end{bmatrix}
$$

### 4. TPR and FPR vs Threshold

Shows how classification performance changes with threshold selection.

---

## Results

Example output:

Dataset shape:

```
(442, 10)
```

Best threshold:

```
0.254
```

Performance metrics:

```
Accuracy: 0.827
Sensitivity (TPR): 0.787
Specificity (TNR): 0.861
AUC: 0.8636
```

---

## Interpretation

* The ROC curve lies above the diagonal reference line.
* The classifier demonstrates strong discriminative ability.
* The AUC value indicates very good classification performance.
* The selected threshold balances sensitivity and specificity.

---

## Conclusion

Binary hypothesis testing using the Likelihood Ratio Test was successfully implemented. The ROC curve and evaluation metrics demonstrate effective classification performance, confirming the suitability of the LRT framework for binary decision-making problems.

---

## Tools and Libraries

* Python
* NumPy
* Matplotlib
* Scikit-learn (for dataset loading and preprocessing)

---

## Author

Pattern Recognition Laboratory
Binary Hypothesis Testing using Likelihood Ratio Test and ROC Analysis
