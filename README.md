# Stratified Risk Profiling and Cognitive Decline Classification in Alzheimer's Disease

## Overview
This project applies machine learning and exploratory data analysis to identify cognitive decline patterns and patient risk profiles in Alzheimer's Disease using the NACC Uniform Data Set (UDS). The goal is to move beyond aggregated risk factors and uncover meaningful subgroup-level differences across demographic, cognitive, behavioral, and treatment-related variables.

## Dataset
- **Source:** National Alzheimer's Coordinating Center (NACC) Uniform Data Set (UDS)
- **Size:** ~250,000 visit-level records across ~50,000 unique participants
- **Key Variables:** MMSE, MoCA scores, diagnosis category (Normal / MCI / AD), NPI-Q behavioral symptoms, demographics, medication usage, APOE status

> The raw dataset is not included in this repository. Access can be requested directly from [NACC](https://naccdata.org/).

## Objectives
- Classify patients into cognitive decline stages: Cognitively Normal, Mild Cognitive Impairment (MCI), and Alzheimer's Disease
- Identify distinct patient subgroups using unsupervised clustering
- Analyze how cognitive decline varies across age, sex, education level, and diagnosis group

## Methodology

### Data Preparation
- Removed high-cardinality free-text variables
- Handled missing values using NACC coding conventions (e.g., -4, -6)
- Standardized categorical variables and constructed visit-level and participant-level datasets

### Exploratory and Stratified Analysis
- Distributions of cognitive scores across diagnostic groups
- Behavioral symptom prevalence across disease stages
- Stratified analysis by age, sex, education, and diagnosis

### Modeling
- **Classification:** Logistic Regression, Random Forest, XGBoost, LightGBM
- **Imbalance Handling:** SMOTE
- **Dimensionality Reduction:** PCA
- **Clustering:** K-Means, Hierarchical Clustering
- **Evaluation:** ROC-AUC, Confusion Matrix, Cross-Validation, Feature Importance

## Results
- Successfully classified cognitive decline stages with strong ROC-AUC performance across ensemble models
- Identified distinct patient subgroups with similar cognitive and behavioral profiles
- Feature importance analysis highlighted MMSE, MoCA, and behavioral symptom indicators as top predictors

## Tools and Technologies
- **Language:** Python
- **Libraries:** Pandas, NumPy, Scikit-Learn, XGBoost, LightGBM, Matplotlib, Seaborn, Plotly
- **Environment:** Google Colab

## Repository Structure
```
alzheimers-cognitive-classification/
├── alzheimers_cognitive_classification.ipynb   # Main analysis notebook
├── alzheimers_project_report.pdf               # Full project report
└── README.md
```

## Author
**Vaishnavi Tiwari**  
M.S. Data Science, DePaul University  
[LinkedIn](https://www.linkedin.com/in/vaishnavi-tiwari-1a18971ab) · [GitHub](https://github.com/tiwari-vaish)
