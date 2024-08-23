
# Bank Personal Loan Prediction

## Project Overview

This project involves building a machine learning model to predict the likelihood of a bank customer accepting a personal loan offer. The dataset used contains information on 5000 customers, including demographic details, relationship with the bank, and response to previous personal loan offers. The goal is to create an effective predictive model that the bank can use to target customers more likely to accept loan offers.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset Description](#dataset-description)
- [Objective](#objective)
- [Approach](#approach)
  - [Exploratory Data Analysis](#exploratory-data-analysis)
  - [Data Preparation](#data-preparation)
  - [Modeling](#modeling)
  - [Evaluation](#model-evaluation)
- [Conclusion](#conclusion)
- [Files in Repository](#files-in-repository)
- [How to Run](#how-to-run)
- [Contributing](#contributing)

## Dataset Description

The dataset `Bank_Personal_Loan_Dataset.csv` contains the following columns:

- **ID**: Customer ID
- **Age**: Customer's age in completed years
- **Experience**: Number of years of professional experience
- **Income**: Annual income of the customer (in $000)
- **ZIP Code**: Home address ZIP code
- **Family**: Family size of the customer
- **CCAvg**: Average spending on credit cards per month (in $000)
- **Education**: Education level (1: Undergrad, 2: Graduate, 3: Advanced/Professional)
- **Mortgage**: Value of house mortgage, if any (in $000)
- **Personal Loan**: Target variable indicating if the customer accepted the personal loan (1: Yes, 0: No)
- **Securities Account**: Does the customer have a securities account with the bank? (1: Yes, 0: No)
- **CD Account**: Does the customer have a certificate of deposit (CD) account with the bank? (1: Yes, 0: No)
- **Online**: Does the customer use internet banking facilities? (1: Yes, 0: No)
- **Credit Card**: Does the customer use a credit card issued by UniversalBank? (1: Yes, 0: No)

## Objective

The primary objective of this project is to build a classification model that can accurately predict whether a bank customer is likely to accept a personal loan offer. This will enable the bank to improve its marketing strategies and focus on customers with a higher likelihood of conversion.

## Approach

### Exploratory Data Analysis

- Analyzed the distribution of key variables such as Age, Income, Family Size, etc.
- Investigated the target variable `Personal Loan` to understand the class distribution.
- Identified and handled any anomalies or data quality issues, such as negative experience values.

### Data Preparation

- Split the dataset into training (70%) and testing (30%) sets to evaluate model performance on unseen data.
- Performed data cleaning and transformation, including handling categorical variables and scaling features where necessary.

### Modeling

Trained multiple classification models to predict the likelihood of a customer accepting a personal loan:

1. **Logistic Regression**
2. **K-Nearest Neighbors (K-NN)**
3. **Naïve Bayes**
4. **Support Vector Machine (SVM)** - The best-performing model

## Model Evaluation

For model evaluation, we used `GridSearchCV` to find the best hyperparameters for each model. The evaluation metrics included:

- **Accuracy Score**: The accuracy of the model on the test set.
- **Best Score**: The best cross-validated score obtained during the grid search.

The results were tabulated as follows:

| Model               | Accuracy Score | Best Score |
|---------------------|----------------|------------|
| Logistic Regression | 0.8811         | 0.9010     |
| K-Nearest Neighbors | 0.8881         | 0.9084     |
| Naïve Bayes         | 0.8147         | 0.8394     |
| SVM                 | 0.9336         | 0.9414     |

Finally, the best scores for each model were visualized using a bar graph to provide a clear comparison.


- Evaluated each model using accuracy score, cross-validated best score and confusion matrix.
- The **SVM model** achieved an accuracy of 94%, outperforming the other models, making it the most suitable choice for this dataset.

## Conclusion

The Support Vector Machine (SVM) model emerged as the best performer in this project due to its strong accuracy, particularly on a small dataset. This model is recommended for predicting customer likelihood to accept personal loan offers, helping the bank to target its marketing efforts more effectively.

## Files in Repository

- `Bank_Personal_Loan_Datasetg.csv`: The dataset used in the project.
- `loan_prediction.ipynb`: Jupyter notebook containing the full analysis, modeling, and evaluation process.
- `README.md`: This file providing an overview of the project.

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/siyamsiza/loan-prediction.git
   cd bank-personal-loan-prediction
   ```

2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Open the Jupyter notebook `loan_prediction.ipynb` to view the full analysis or run the code.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any changes or improvements.


