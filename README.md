# OIBSIP – Data Analytics Internship Portfolio

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?logo=scikitlearn&logoColor=white)](https://scikit-learn.org/)

A collection of data analytics and machine learning projects completed during the **Oasis Infobyte (OIBSIP) Data Analytics Internship**. The projects span exploratory data analysis, unsupervised learning, and supervised classification on imbalanced data. Each project folder contains a Jupyter notebook, a dedicated README, and exported visual outputs.

---

## Table of Contents

1. [Project Summary](#project-summary)
2. [Repository Structure](#repository-structure)
3. [Project Details](#project-details)
4. [Technology Stack](#technology-stack)
5. [Installation and Usage](#installation-and-usage)
6. [Skills Demonstrated](#skills-demonstrated)
7. [Author](#author)
8. [Acknowledgements](#acknowledgements)

---

## Project Summary

| Level | Project | Approach | Dataset | Documentation |
| :---: | ------- | -------- | ------- | ------------- |
| L1 | Retail Sales Analysis | Exploratory Data Analysis | Superstore sales (9,800 records, 18 columns) | [README](DataAnalytics/L1/EDARetailSales/README.md) |
| L1 | Customer Segmentation | K-Means Clustering | Customer demographics (8,068 train / 2,627 test) | [README](DataAnalytics/L1/CustomerSegmentation/README.md) |
| L2 | Credit Card Fraud Detection | Logistic Regression, Random Forest, SMOTE | Kaggle Credit Card Fraud (284,807 transactions) | [README](<DataAnalytics/L2/Fraud detection/README.md>) |

---

## Repository Structure

```text
OIBSIP/
└── DataAnalytics/
    ├── L1/
    │   ├── EDARetailSales/
    │   │   ├── data/                 # Superstore sales dataset
    │   │   ├── outputs/              # Charts and result screenshots
    │   │   ├── notebook.ipynb
    │   │   └── README.md
    │   └── CustomerSegmentation/
    │       ├── dataset/              # Train, test, and sample submission files
    │       ├── outputs/              # Elbow, silhouette, and cluster plots
    │       ├── notebook.ipynb
    │       └── README.md
    └── L2/
        └── Fraud detection/
            ├── outputs/              # Class distribution, ROC, and feature plots
            ├── notebook.ipynb
            └── README.md
```

---

## Project Details

### 1. Retail Sales Analysis (Level 1)

**Objective:** Analyse retail sales data to understand customer segments, product performance, regional trends, and shipping patterns.

**Approach**
- Data inspection, type conversion, missing-value and duplicate checks
- Descriptive statistics for sales and shipping duration
- Monthly and quarterly sales trend analysis
- Customer segment analysis and top-10 product ranking
- Correlation analysis, shipping-mode comparison, and regional sales comparison

**Deliverables:** Visualisations, business observations, and recommendations on inventory, marketing, and shipping.

---

### 2. Customer Segmentation (Level 1)

**Objective:** Group customers into distinct segments using demographic and spending-related attributes to support targeted marketing.

**Approach**
- Cleaning: median imputation for numeric fields, fallback category for categorical fields
- Preprocessing: `StandardScaler` for numeric features, `OneHotEncoder` for categorical features (32 encoded features)
- Cluster selection: Elbow Method and silhouette analysis
- Modelling: K-Means with **k = 4**
- Profiling: cluster-level statistics compared against existing segment labels

**Selected Results**

| Cluster | Customers | Avg. Age | Avg. Family Size | Profile Highlight |
| :-----: | --------: | -------: | ---------------: | ----------------- |
| 0 | 2,511 | 42.7 | 2.00 | 100% low spending score |
| 1 | 1,533 | 61.4 | 2.72 | Predominantly high spending score (78.4%) |
| 2 | 1,959 | 46.7 | – | Mid-age group |
| 3 | 2,065 | 28.0 | – | Youngest group |

**Outputs:** `train_customer_segments.csv`, `customer_cluster_profile.csv`, `test_customer_clusters.csv`, `submission.csv`

---

### 3. Credit Card Fraud Detection (Level 2)

**Objective:** Detect fraudulent transactions in a highly imbalanced dataset and compare classification models.

**Approach**
- Class-distribution and transaction-time analysis
- Imbalance handling with **SMOTE**, applied to the training set only to prevent data leakage
- Models: Logistic Regression (baseline) and Random Forest
- Evaluation: Precision, Recall, F1-score, ROC-AUC, and confusion matrices
- Discussion of scaling the solution to roughly one million transactions per hour

**Results**

| Model | ROC-AUC |
| ----- | :-----: |
| Logistic Regression | 0.971 |
| Random Forest | 0.964 |

The most influential features in the Random Forest model were **V14, V10, V4, V12, and V17**.

> The dataset (`creditcard.csv`) is not included due to its size. Download it from [Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) and place it beside the notebook.

---

## Technology Stack

| Category | Tools |
| -------- | ----- |
| Language | Python |
| Data processing | Pandas, NumPy |
| Visualisation | Matplotlib, Seaborn |
| Machine learning | Scikit-learn, Imbalanced-learn |
| Environment | Jupyter Notebook, Visual Studio Code |

---

## Installation and Usage

```bash
# 1. Clone the repository
git clone https://github.com/soniyashaik29/OIBSIP.git
cd OIBSIP

# 2. (Optional) Create and activate a virtual environment
python -m venv venv
venv\Scripts\activate          # Windows
# source venv/bin/activate     # macOS / Linux

# 3. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn jupyter

# 4. Open a project notebook
cd DataAnalytics/L1/CustomerSegmentation
jupyter notebook
```

Run the notebook cells in order. If a dataset fails to load, update the file path in the data-loading cell to match your local directory.

---

## Skills Demonstrated

- Data cleaning, preprocessing, and feature engineering
- Exploratory data analysis and data visualisation
- Unsupervised learning and cluster validation (Elbow, Silhouette)
- Handling class imbalance (SMOTE) and model evaluation beyond accuracy
- Communicating analytical findings as business recommendations

---

