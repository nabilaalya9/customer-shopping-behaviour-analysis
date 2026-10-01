# Customer Shopping Behaviour Analysis

An end-to-end customer analytics project exploring purchasing behaviour, customer spending segments, and subscription patterns through exploratory analysis, statistical testing, and predictive modelling.

**Project Type:** Group Project
**Role:** Data Analyst
**Focus:** Customer Analytics · Statistical Analysis · Predictive Modelling
**Tools:** Python · Pandas · NumPy · Scikit-learn · XGBoost · Tableau

---

## 1. Project Overview

Understanding customer behaviour is important for identifying high-value customers, evaluating differences between customer groups, and understanding factors associated with subscription status.

This project analyzes customer shopping behaviour using an end-to-end analytical workflow based on the **CRISP-DM framework**.

The analysis covers:

* Data cleaning and preparation
* Exploratory Data Analysis (EDA)
* Customer spending segmentation
* Statistical hypothesis testing
* Subscription prediction
* Model evaluation
* Interactive Tableau visualization

The final output combines statistical evidence, machine learning evaluation, and business-oriented insights.

---

## 2. Business Questions

This project focuses on three main questions:

1. What patterns characterize customer purchasing behaviour?
2. How can customers be differentiated based on spending behaviour?
3. Can customer behaviour help predict subscription status?

---

## 3. Dataset

The dataset contains approximately **3,900 customer records** and **13 variables** describing customer demographics, purchasing behaviour, and subscription-related information.

The analysis uses variables related to:

* Customer demographics
* Purchase amount
* Purchase frequency
* Previous purchases
* Discount usage
* Subscription status
* Other customer behavioural attributes

The dataset is provided in the `data/` folder and can be used to reproduce the analysis and run the notebooks.

---

## 4. Analytical Workflow

The project follows an end-to-end analytical workflow:

```text
Raw Data
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Statistical Analysis
   ↓
Customer Segmentation
   ↓
Predictive Modelling
   ↓
Model Evaluation
   ↓
Business Insights
   ↓
Tableau Dashboard
```

---

## 5. Data Preparation

The data preparation stage focuses on ensuring that the dataset is suitable for statistical analysis and machine learning.

Key activities include:

* Checking data types
* Handling missing values
* Identifying inconsistencies
* Preparing categorical variables
* Preparing numerical variables
* Creating analysis-ready features
* Preparing the target variable for classification

---

## 6. Exploratory Data Analysis

EDA was conducted to understand customer purchasing behaviour and identify patterns across customer characteristics.

The analysis explored relationships between:

* Purchase amount
* Customer demographics
* Purchase frequency
* Previous purchases
* Discount usage
* Subscription status

The findings from EDA were then used to define further statistical and predictive analyses.

---

## 7. Customer Spending Segmentation

Customers were segmented based on purchase amount using the **75th percentile** as the threshold for identifying higher-spending customers.

| Segment         | Customers | Average Purchase |
| --------------- | --------: | ---------------: |
| Regular Spender |     2,922 |           $49.46 |
| High Spender    |       978 |           $90.55 |

The **75th percentile threshold was $81**.

This segmentation was used as a basis for comparing purchasing behaviour between Regular Spenders and High Spenders.

---

## 8. Statistical Analysis

Statistical testing was conducted to determine whether observed differences and relationships were supported by statistical evidence.

Methods included:

* Pearson / Spearman correlation
* Shapiro-Wilk test
* Chi-Square test
* Cramér's V
* ANOVA
* Kruskal-Wallis test
* Mann-Whitney U test
* Effect size analysis

### High Spender vs Regular Spender

A Mann-Whitney U test was used to compare purchase amounts between the two spending groups.

**Result:**

* p-value: **< 0.0001**
* Cohen's d: **3.12**

The result indicates a statistically significant difference in purchase amounts between the two groups, with a large effect size.

---

## 9. Subscription Prediction

The project also evaluates whether customer shopping behaviour can be used to predict subscription status.

Four classification models were evaluated:

* Logistic Regression
* Support Vector Machine (SVM)
* Random Forest
* XGBoost

### Modelling Approach

* Train-test split: **80/20**
* SMOTE applied to the training data
* Multiple classification models compared
* Cross-validation used for evaluation
* Model performance evaluated using multiple metrics

### Logistic Regression Results

The selected/tuned Logistic Regression model achieved:

| Metric                    | Result |
| ------------------------- | -----: |
| Accuracy                  | 86.41% |
| F1-Macro                  | 84.83% |
| Precision                 | 66.56% |
| Subscriber Recall         |   100% |
| AUC-ROC                   | 91.40% |
| Cross-Validation F1-Macro | 81.87% |
| Generalization Gap        |  2.98% |

These results indicate that customer shopping behaviour provides useful signals for predicting subscription status, while precision and generalization should still be considered when interpreting the model.

---

## 10. Key Findings

### Spending Segmentation

High Spenders had a higher average purchase amount than Regular Spenders.

* High Spender: **$90.55**
* Regular Spender: **$49.46**

### Statistical Evidence

The difference between the two spending groups was statistically significant:

**Mann-Whitney U: p < 0.0001**

The effect size was:

**Cohen's d = 3.12**

### Subscription Prediction

Customer behavioural variables provided useful predictive signals for subscription status.

The evaluated Logistic Regression model achieved an **AUC-ROC of 91.40%**.

### Customer Behaviour

EDA revealed patterns across purchasing behaviour, customer characteristics, and subscription status that were further evaluated through statistical analysis and predictive modelling.

---

## 11. Dashboard

The analytical findings were translated into an interactive Tableau dashboard.

**Tableau Public:**
https://public.tableau.com/app/profile/nabila.mukhbita/viz/CustomerShoppingBehaviorAnalysisDashboard/Line-AvgPurchaseSeason?publish=yes

The dashboard provides an interactive way to explore customer purchasing patterns and analytical findings.

---

## 12. Project Materials

### `data/`

Contains the dataset used in this project. The dataset can be used to reproduce the analysis and run the notebooks provided in this repository.

### `notebooks/`

Contains the complete analytical workflow, including:

* Data processing and cleaning
* Exploratory Data Analysis
* Statistical analysis
* Customer segmentation
* Predictive modelling
* Model evaluation

### `pitchdeck/`

Contains the project report and presentation materials summarizing the analytical results, key findings, and business insights.

---

## 13. Tools & Technologies

| Category             | Tools                 |
| -------------------- | --------------------- |
| Programming          | Python                |
| Data Manipulation    | Pandas, NumPy         |
| Statistical Analysis | SciPy                 |
| Machine Learning     | Scikit-learn, XGBoost |
| Data Visualization   | Matplotlib, Seaborn   |
| Dashboard            | Tableau               |
| Methodology          | CRISP-DM              |

---

## 14. Project Outcome

This project resulted in:

* Customer spending segmentation
* Statistical evaluation of differences between customer groups
* Evaluation of multiple subscription classification models
* A predictive modelling pipeline for subscription status
* An interactive Tableau dashboard
* Business insights derived from customer purchasing behaviour

The project demonstrates an end-to-end approach to transforming customer data into statistical evidence, predictive insights, and business-oriented visualization.

---

## 15. Related Portfolio

For the concise case-study version of this project, visit the project page on my portfolio.

**Portfolio:** https://nabilaalya.vercel.app/projects/customer-shopping-behaviour-analysis

**Tableau Dashboard:**
https://public.tableau.com/app/profile/nabila.mukhbita/viz/CustomerShoppingBehaviorAnalysisDashboard/Line-AvgPurchaseSeason?publish=yes
