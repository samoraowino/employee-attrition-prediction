# Employee Attrition Classification

This project explores employee attrition prediction using three classification models:
- Neural Network (MLP Classifier)
- K-Nearest Neighbors (KNN)
- Decision Tree

The dataset used is from Kaggle: **[IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)**

---

##  Project Objective

To predict whether an employee is likely to leave the company using machine learning models and compare their performance using accuracy based on confusion matrix values.

---

##  Models Used

| Model               | Notes                                     |
|--------------------|-------------------------------------------|
| Neural Network      | Two hidden layers, uses scaled inputs     |
| KNN (k=5)           | Distance-based, sensitive to scaling      |
| Decision Tree       | Rule-based, easy to interpret             |

All models were trained using a 50–50 train-test split and evaluated using:

> **Accuracy = (True Positives + True Negatives) / Total Test Cases**

---

##  Evaluation Summary

| Model               | Accuracy (%) | Recall on leavers (%) | Notes                                              |
|--------------------|--------------|-----------------------|----------------------------------------------------|
| KNN (k=5)           | 84.35        | 16.81                 | Highest accuracy, but misses most leavers          |
| Neural Network      | 83.13        | 36.97                 | Best at catching leavers; handles non-linear patterns |
| Decision Tree       | 82.86        | 32.77                 | Most interpretable                                 |

**Note on class imbalance:** 83.9% of employees stayed, so a model that always predicts "stay" would score about 83.9% accuracy. Recall on the leaver class (119 leavers in the 735-record test set) gives a better comparison of the models.

---

##  Key Insights

- **Top predictors** of attrition (Decision Tree feature importance) were: `TotalWorkingYears`, `MonthlyIncome`, `YearsWithCurrManager`, `OverTime`.
- **Decision Trees** provided explainable rules useful for HR policy.
- KNN achieved the highest accuracy (84.35%), but the Neural Network identified the most leavers (36.97% recall), making it the more useful model for flagging at-risk employees.

---

## Tools Used

- Python 3.x
- scikit-learn
- pandas, numpy
- matplotlib, seaborn
- Jupyter Notebook
- GitHub + VS Code

---
