# Predicting and Understanding Healthcare Utilization Among Older Adults:
## A Machine Learning and Causal Inference Analysis of the National Poll on Healthy Aging (NPHA)

![Python](https://img.shields.io/badge/Python-3.10+-blue)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange)
![DoWhy](https://img.shields.io/badge/DoWhy-Causal%20Inference-green)
![SHAP](https://img.shields.io/badge/SHAP-Explainable%20AI-red)
![Status](https://img.shields.io/badge/Status-Research%20Project-success)

---

# Overview

Healthcare utilization is influenced by a combination of physical, psychological, and behavioral factors. Understanding these relationships is important for improving healthcare planning, identifying vulnerable populations, and supporting evidence-based policy decisions.

This project investigates healthcare utilization among older adults using data from the National Poll on Healthy Aging (NPHA). The study combines traditional machine learning techniques with causal inference methods to explore both predictive and potential causal relationships between health-related factors and the number of doctor visits.

The project follows a research-oriented workflow including data preprocessing, exploratory data analysis, predictive modeling, explainable AI, and causal effect estimation.

---

# Research Questions

### RQ1
Can machine learning models accurately predict the number of doctor visits among older adults?

### RQ2
Which health-related factors contribute most to healthcare utilization?

### RQ3
What is the estimated causal effect of mental health on the number of doctor visits?

### RQ4
To what extent do sleep-related factors mediate the relationship between mental health and healthcare utilization?

---

# Dataset

**National Poll on Healthy Aging (NPHA)**

The dataset contains information about older adults, including:

- Number of Doctors Visited
- Mental Health Status
- Physical Health Indicators
- Stress Levels
- Sleep Quality
- Prescription Sleep Medication Usage
- Demographic Variables

Target Variable:

```text
Number of Doctors Visited
```

---

# Methodology

The project consists of five main stages.

## 1. Data Preprocessing

- Missing value analysis
- Outlier detection using IQR
- Outlier treatment through capping
- Data cleaning and feature preparation

---

## 2. Exploratory Data Analysis (EDA)

Exploratory analysis is performed to understand:

- Feature distributions
- Variable relationships
- Correlation patterns
- Potential predictors of healthcare utilization

Visualizations include:

- Boxplots
- Histograms
- Pairplots
- Correlation heatmaps

---

## 3. Predictive Modeling

Several machine learning models are trained and compared.

### Linear Regression

Used as a baseline interpretable model.

### Random Forest Regression

Used to capture nonlinear relationships and feature interactions.

### Gradient Boosting Regression

Used to improve predictive performance through sequential learning.

### Evaluation Metrics

- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R² Score

---

## 4. Explainable AI

To understand model behavior, SHAP (SHapley Additive exPlanations) is used.

### Objectives

- Identify influential predictors
- Explain individual predictions
- Understand feature contributions

Visualizations include:

- SHAP Summary Plot
- Feature Importance Ranking
- Dependence Plots

---

## 5. Causal Inference

While predictive models identify associations, causal inference aims to estimate potential causal effects.

### Treatment

```text
Mental Health
```

### Outcome

```text
Number of Doctors Visited
```

### Potential Confounders

- Age
- Physical Health
- Stress
- Sleep Quality
- Medication Usage

### Causal Framework

A Directed Acyclic Graph (DAG) is constructed to represent assumed causal relationships.

The analysis uses:

- DoWhy
- Backdoor Adjustment
- Refutation Tests

---

# Project Structure

```text
npha-healthcare-utilization/
│
├── data/
│   └── NPHA-doctor-visits.csv
│
├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_predictive_modeling.ipynb
│   ├── 03_shap_analysis.ipynb
│   └── 04_causal_inference.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── modeling.py
│   ├── explainability.py
│   └── causal_analysis.py
│
├── outputs/
│   ├── figures/
│   ├── metrics/
│   └── reports/
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

# Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn
- SHAP
- DoWhy
- NetworkX

---

# Key Findings

The project aims to identify:

- The strongest predictors of healthcare utilization.
- The role of mental health in influencing doctor visits.
- The interaction between stress, sleep quality, and healthcare outcomes.
- Potential causal mechanisms behind healthcare utilization patterns.

---

# Limitations

This study is based on observational survey data.

Therefore:

- Results from machine learning models represent predictive associations.
- Causal estimates depend on the assumed causal graph and observed confounders.
- Findings should not be interpreted as definitive proof of causality.

---

# Future Work

Potential extensions include:

- Structural Causal Models (SCM)
- Bayesian Networks
- Counterfactual Analysis
- Causal Discovery Algorithms
- Longitudinal Healthcare Modeling
- Reinforcement Learning for Personalized Healthcare Interventions

---

# Reproducibility

Install dependencies:

```bash
pip install -r requirements.txt
```

Run preprocessing:

```bash
python src/preprocessing.py
```

Train models:

```bash
python src/modeling.py
```

Generate SHAP explanations:

```bash
python src/explainability.py
```

Run causal analysis:

```bash
python src/causal_analysis.py
```



---


