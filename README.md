Credit Card Default Prediction

This is a personal machine learning project where I worked on predicting whether a credit card client will default on their next payment. The dataset is from the UCI Machine Learning Repository and contains anonymized data on 30,000 credit card users in Taiwan.

Project Goal

The goal was to explore the data, understand the factors related to defaults, and build classification models to predict the target variable: default.payment.next.month (1 = default, 0 = no default).

Dataset Info

Source: UCI Credit Card Dataset

Rows: 30,000 customers

Features include: gender, age, education, marital status, payment history, bill amounts, and past payments

Steps I Followed

1. Data Cleaning

Removed the ID column (not useful for modeling)

Replaced unclear values in the EDUCATION column with "Other"

Filled missing values in the MARRIAGE column

2. Feature Engineering

Mapped numerical codes in SEX, MARRIAGE, and EDUCATION to meaningful labels

Used one-hot encoding for categorical features

Standardized numerical features using StandardScaler

3. Exploratory Data Analysis (EDA)

Looked at the distribution of the target variable

Compared default rates by gender, age group, education, and marital status

Checked for outliers using boxplots

Built a correlation heatmap

4. Modeling

I trained two models:

Logistic Regression

Accuracy: ~81%

Performance was decent, but recall for defaulters was low (due to imbalance)

Random Forest

Accuracy: ~81.3%

Better recall and F1-score on the positive class (defaults)

Gave useful feature importance insights

5. Feature Importance

The most important features in predicting default were:

PAY_0 (most recent payment status)

AGE

LIMIT_BAL (credit limit)

BILL_AMT1, BILL_AMT2, PAY_AMT1, etc.

Evaluation Metrics

Used accuracy, precision, recall, F1-score and confusion matrix to evaluate both models.

Observations

Most recent payment behavior (PAY_0) is the strongest indicator of default

Age and credit limit also affect the outcome

Random Forest performed better overall

Next Steps (Future Ideas)

Try techniques like SMOTE for handling class imbalance

Test additional models like XGBoost

Deploy a Streamlit or Power BI dashboard to make it interactive

Tech Stack

Python

pandas, numpy, matplotlib, seaborn

scikit-learn

Jupyter Notebook

Files

credit_default_prediction.ipynb – notebook with all code and outputs

requirements.txt – Python dependencies

README.md – this file

Author

Shynggys Torez – Data Analyst / ML enthusiast
My Upwork profile
