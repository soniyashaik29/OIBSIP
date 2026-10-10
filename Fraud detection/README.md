# Credit Card Fraud Detection

## OASIS INFOBYTE Internship — Task 3

## Project Overview

This project focuses on detecting fraudulent credit card transactions using machine learning. The dataset contains legitimate and fraudulent transactions, with fraudulent cases representing a very small proportion of the total data.

The objective is to build and evaluate classification models that can identify suspicious transactions while addressing the challenges of highly imbalanced data.

## Objectives

- Analyze credit card transaction data.
- Explore the distribution of legitimate and fraudulent transactions.
- Handle class imbalance using **SMOTE (Synthetic Minority Over-sampling Technique)**.
- Build and compare Logistic Regression and Random Forest models.
- Evaluate model performance using appropriate classification metrics.
- Visualize results using ROC curves and confusion matrices.
- Discuss how the solution could scale to process approximately one million transactions per hour.

## Dataset

**Dataset:** Credit Card Fraud Detection

The dataset is commonly available on Kaggle.

- [Credit Card Fraud Detection Dataset on Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud)

The original dataset contains 284,807 transactions and 31 columns, including the `Time`, `Amount`, and `Class` columns.

- `Time`: Seconds elapsed between each transaction and the first transaction in the dataset.
- `Amount`: Transaction amount.
- `Class`: Target variable, where `0` represents a legitimate transaction and `1` represents a fraudulent transaction.
- `V1` to `V28`: Anonymized transaction features.

**Note:** The dataset contains 492 fraudulent transactions, making it highly imbalanced. These counts refer to the original dataset; verify them against the file used in this project.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Imbalanced-learn
- Jupyter Notebook
- Visual Studio Code

## Machine Learning Models

### 1. Logistic Regression

A classification algorithm used as a baseline model to estimate the probability that a transaction is fraudulent.

### 2. Random Forest

An ensemble learning algorithm that combines multiple decision trees to classify transactions and capture potentially complex relationships in the data.

### Handling Class Imbalance

SMOTE is applied to the training data to increase representation of the minority fraud class. Resampling is performed only on the training data to avoid data leakage into the test set.

## Project Workflow

1. Import the required Python libraries.
2. Load and inspect the dataset.
3. Check missing values, duplicate records, and class distribution.
4. Perform exploratory data analysis.
5. Visualize transaction amounts and fraud distribution.
6. Split the data into training and testing sets using stratified sampling.
7. Apply feature scaling and SMOTE within the training pipeline, where appropriate.
8. Train Logistic Regression and Random Forest classifiers.
9. Generate predictions and fraud probabilities.
10. Evaluate the models using precision, recall, F1-score, ROC-AUC, and confusion matrices.
11. Compare the models and discuss their suitability for fraud detection.

## Evaluation Metrics

The following metrics are used to assess model performance:

- **Precision:** The proportion of transactions predicted as fraud that are actually fraudulent.
- **Recall:** The proportion of actual fraudulent transactions correctly detected.
- **F1-score:** The harmonic mean of precision and recall.
- **ROC-AUC:** Measures how well a model distinguishes between the two classes across classification thresholds.
- **Confusion Matrix:** Shows correctly and incorrectly classified transactions.

Accuracy alone is insufficient for this problem because a model may classify nearly every transaction as legitimate and still achieve high accuracy while missing fraudulent transactions.

## Scalability Considerations

To support approximately one million transactions per hour, a production system could use:

- Stream processing tools such as Apache Kafka.
- Automated feature engineering and an online feature store.
- A scalable model inference service.
- Horizontal scaling and load balancing.
- Real-time monitoring for latency, data drift, and model performance.
- Periodic model retraining and fraud-pattern updates.

One million transactions per hour is approximately 278 transactions per second on average. Actual production capacity would need to account for peak traffic, latency requirements, and infrastructure overhead.

## Expected Outcomes

The project demonstrates how machine learning can be applied to imbalanced transaction data and how different classification models can be evaluated for fraud detection.

The final model comparison should be based on the actual results produced by the notebook, particularly fraud-class precision, recall, F1-score, and ROC-AUC.

## How to Run the Project

### 1. Clone or download the repository

Download the project files to your computer.

### 2. Create and activate a virtual environment

On Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install dependencies

```bash
python -m pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn jupyter
```

### 4. Add the dataset

Download `creditcard.csv` from Kaggle and place it in the project directory, alongside the notebook.

### 5. Launch Jupyter Notebook

```bash
python -m jupyter notebook
```

Alternatively, open the notebook directly in Visual Studio Code and select the project's virtual environment as the Python interpreter.

### 6. Run the notebook

Open `fraud_detection.ipynb` and execute the cells in order, from data loading through model evaluation.

## Project Structure

```text
OASIS/
├── creditcard.csv
├── fraud_detection.ipynb
├── README.md
└── venv/
```

The `venv/` folder is a local virtual environment and generally should not be uploaded to GitHub.

## Conclusion

This project explores the use of Logistic Regression and Random Forest for credit card fraud detection. It demonstrates exploratory data analysis, class-imbalance handling, model training, and performance evaluation.

The results highlight the importance of detecting fraudulent transactions effectively rather than relying solely on accuracy. In a real-world deployment, the selected model would also require testing for inference speed, reliability, false-positive costs, and performance on new transaction data.

## Acknowledgements

- OASIS INFOBYTE for the internship opportunity.
- Kaggle and the dataset contributors for providing the credit card fraud detection dataset.
- The Python open-source community for the machine learning and data analysis libraries used in this project.
