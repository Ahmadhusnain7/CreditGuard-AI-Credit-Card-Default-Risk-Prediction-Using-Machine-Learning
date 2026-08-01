# CreditGuard AI — Credit Card Default Risk Prediction

A Machine Learning classification project that predicts whether a credit card customer is likely to default on their next payment.

##  Project Overview

**CreditGuard AI** is a supervised Machine Learning project focused on credit card default prediction.

The project uses customer financial and demographic information, repayment history, bill statements, and previous payment information to train and compare multiple classification algorithms.

The main objective is to evaluate different Machine Learning models and identify the model with the strongest overall performance on the test dataset.

---

##  Project Objective

The goal of this project is to predict:

* `0` → No Default
* `1` → Default

The project also compares different Machine Learning algorithms using standard classification metrics.

---

##  Dataset

The dataset contains:

* **30,000 records**
* **24 predictive features**
* **1 target variable**

### Main feature categories

* Credit limit
* Gender
* Education
* Marital status
* Age
* Monthly repayment status
* Monthly bill statements
* Previous payment amounts

### Target

`default_payment_next_month`

The target indicates whether a customer defaulted on their next month's payment.

### Dataset Distribution

* No Default: **23,364 (77.88%)**
* Default: **6,636 (22.12%)**

This shows that the target variable is imbalanced, which is important when interpreting model performance.

---

##  Data Preprocessing

The following preprocessing steps were performed:

1. Dataset loading and inspection
2. Missing-value detection
3. Missing-value handling
4. Duplicate-value checking
5. Feature and target separation
6. Categorical feature encoding
7. Numerical feature standardization
8. Train/Test split

### Missing Values

The dataset initially contained **600 missing values**, which were handled during preprocessing.

There were **no duplicate rows**.

### Train/Test Split

* Training samples: **24,000**
* Testing samples: **6,000**
* Test size: **20%**

---

##  Machine Learning Models

Six classification algorithms were trained and evaluated:

### 1. Logistic Regression

Used as a strong baseline classification algorithm.

### 2. K-Nearest Neighbors (KNN)

Classifies observations based on their nearest neighboring data points.

### 3. Decision Tree

Uses a sequence of decision rules to classify customers.

### 4. Random Forest

Uses multiple decision trees to produce a more robust prediction.

### 5. Support Vector Machine (SVM)

Finds a decision boundary that separates the classes.

### 6. Naive Bayes

Uses probabilistic classification based on Bayes' theorem.

---

## 📈 Model Results

| Model                  |   Accuracy |  Precision |     Recall | Weighted F1-Score |
| ---------------------- | ---------: | ---------: | ---------: | ----------------: |
|  Logistic Regression | **81.78%** | **80.00%** | **81.78%** |        **79.58%** |
| SVM                    |     81.73% |     80.01% |     81.73% |            79.05% |
| Random Forest          |     81.55% |     79.68% |     81.55% |            79.43% |
| KNN                    |     79.63% |     77.24% |     79.63% |            77.57% |
| Naive Bayes            |     79.02% |     76.10% |     79.02% |            72.98% |
| Decision Tree          |     71.92% |     72.81% |     71.92% |            72.34% |

---

##  Best Performing Model

Based on the overall test-set comparison, **Logistic Regression** achieved the strongest overall result.

### Logistic Regression

* **Accuracy:** 81.78%
* **Precision:** 80.00%
* **Recall:** 81.78%
* **Weighted F1-Score:** 79.58%

It slightly outperformed Random Forest and SVM in the overall comparison.

---

##  Important Observation

Although Logistic Regression achieved **81.78% accuracy**, the model's performance on the actual default class was more limited:

* Default-class Precision: **67%**
* Default-class Recall: **35%**
* Default-class F1-Score: **46%**

This is an important finding because the dataset contains significantly more non-default than default cases.

Therefore, a model with high overall accuracy does not necessarily mean that it is highly effective at identifying customers who will actually default.

For a real-world credit-risk system, additional techniques such as class-imbalance handling, threshold optimization, and hyperparameter tuning could be explored in future work.

---

##  Technologies Used

* Python
* Google Colab
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

##  Project Structure

```text
CreditGuard-AI/
│
├── CreditGuard_AI_Credit_Card_Default_Prediction.ipynb
├── creditguard_model_comparison.csv
├── README.md
└── dataset/
```

---

##  Evaluation Metrics

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Classification Report

---

##  Key Learnings

Through this project, I practiced:

* Data preprocessing
* Handling missing values
* Categorical encoding
* Feature scaling
* Train/Test splitting
* Supervised Machine Learning
* Classification algorithms
* Model comparison
* Confusion matrix analysis
* Understanding class imbalance
* Interpreting classification metrics

---

##  Future Improvements

This project can be further improved by exploring:

* Class imbalance techniques
* Hyperparameter tuning
* Cross-validation
* ROC-AUC and PR-AUC analysis
* Threshold optimization
* Feature selection
* Advanced ensemble methods

These improvements were intentionally kept outside the current project scope to focus on implementing and comparing the core Machine Learning classification models.

---
### Conclusion

Logistic Regression achieved the best overall performance with **81.78% accuracy** and **79.58% weighted F1-score**, closely followed by SVM and Random Forest. However, its **35% recall for the default class** shows that accuracy alone is not sufficient for reliable credit-risk prediction. Future improvements could focus on **class imbalance handling, hyperparameter tuning, and threshold optimization** to improve default detection.

##  Project

**CreditGuard AI — Credit Card Default Risk Prediction Using Machine Learning**

Built as a practical Machine Learning project to understand and compare multiple classification algorithms on a financial risk prediction problem.
