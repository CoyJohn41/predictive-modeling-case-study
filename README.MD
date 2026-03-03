# Predictive Modeling Case Study

> End-to-end data science workflow on real-world housing data — from raw dataset to deployed predictions.

**Live Project Page:** [coyjohnson25.github.io/predictive-modeling-case-study](https://coyjohnson25.github.io/predictive-modeling-case-study)  
**Portfolio:** [coyjohnson25.github.io](https://coyjohnson25.github.io)

---

## Overview

A complete data science pipeline applied to the Ames Housing dataset — 2,930 observations, 79 features. Every decision at every stage is justified: how to handle missing data, which features to engineer, which models to trust, and how to communicate predictions clearly.

---

## What's Inside

```
predictive-modeling-case-study/
├── README.md
├── requirements.txt
├── data/
│   └── ames_housing.csv             ← Raw dataset
├── notebooks/
│   ├── 01_eda.ipynb                 ← Exploratory data analysis
│   ├── 02_cleaning.ipynb            ← Missing values & preprocessing
│   ├── 03_features.ipynb            ← Feature engineering
│   ├── 04_modeling.ipynb            ← Model training & selection
│   └── 05_interpretation.ipynb      ← Results & insights
├── src/
│   ├── features.py                  ← Feature engineering functions
│   ├── models.py                    ← Model training pipeline
│   └── evaluate.py                  ← CV scoring and comparison
├── results/
│   ├── model_comparison.png
│   ├── feature_importance.png
│   └── residual_analysis.png
└── docs/
    └── index.html                   ← Project detail page
```

---

## Pipeline

| Step | Description |
|------|-------------|
| EDA | Distribution analysis, correlation heatmaps, outlier detection |
| Cleaning | Median/mode imputation, domain-knowledge missing value fills |
| Feature Engineering | TotalSF, HouseAge, RemodAge, QualSF interaction term |
| Model Selection | 5-fold CV comparison across 5 model classes |
| Interpretation | Feature importance, partial dependence, plain-language summary |

---

## Model Results

| Model | CV RMSE ($) |
|-------|-------------|
| Linear Regression | $28,400 |
| Ridge | $21,200 |
| Lasso | $21,350 |
| Random Forest | $20,050 |
| **Gradient Boosting** | **$18,320** ✓ |

---

## Quickstart

```bash
git clone https://github.com/coyjohnson25/predictive-modeling-case-study.git
cd predictive-modeling-case-study
pip install -r requirements.txt
jupyter notebook notebooks/01_eda.ipynb
```

---

## Key Findings

- TotalSF × OverallQual explains more variance than all other features combined
- Log-transforming the target reduced test RMSE by ~22%
- Lasso auto-selected 45 of 79 features, zeroing out the rest
- Final model explains 92.6% of variance (R² = 0.926)

---

## Tech Stack

`Python` `Pandas` `Scikit-learn` `Matplotlib` `Seaborn` `Jupyter`

---

## Author

**Coy Johnson** — [coyjohnson25@gmail.com](mailto:coyjohnson25@gmail.com)  
M.S. Mathematics Candidate | Applied Mathematician# predictive-modeling-case-study
