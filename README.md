# bank-customer-churn-prediction
Bank Customer Churn Prediction End to End Project.
# Bank Customer Churn Prediction

## Project Overview

This project aims to **predict customer churn** using machine learning models. The goal is to analyze customer behavior, preprocess data, and compare multiple models to determine the best-performing one for churn prediction. This workflow includes:

- **Data Preprocessing**: Cleaning and transforming raw customer data.
- **Exploratory Data Analysis (EDA)**: Understanding patterns and relationships in the dataset.
- **Model Training & Evaluation**: Training Decision Tree, Random Forest, XGBoost, Logistic Regression, SVM, Neural Networks, and KNN models.
- **Model Comparison & Assessment**: Evaluating and ranking models based on performance metrics.

## Project Structure

```
bank-customer-churn-prediction/
│── data/                          <- Processed datasets used for training
│── notebooks/                      <- Jupyter Notebooks for each stage
│   ├── Data_preprocessing.ipynb     <- Data cleaning, encoding, and transformation
│   ├── EDA_bank_customer_churn.ipynb <- Exploratory Data Analysis (EDA)
│   ├── Modeling_DT_RF_XG.ipynb      <- Decision Tree, Random Forest, XGBoost training
│   ├── Modeling_LogReg_SVM_NN_KNN.ipynb <- Logistic Regression, SVM, Neural Network, KNN training
│   ├── Model Comparison and Assessment.ipynb <- Comparing model performance & selecting the best
│── reports/                         <- Model evaluation reports
│── README.md                         <- Project Overview & How-to-Run Instructions
│── LICENSE                           <- Project License
```

## Model Comparison Results (Test)

| Model               | Accuracy | Precision | Recall | F1 Score | Rank |
| ------------------- | -------- | --------- | ------ | -------- | ---- |
| XGBoost             | 73.10%   | 69.21%    | 83.14% | 75.54%   | #1   |
| Decision Tree       | 75.14%   | 75.21%    | 74.96% | 75.10%   | #2   |
| Random Forest       | 74.33%   | 74.07%    | 74.80% | 74.43%   | #3   |
| SVM                 | 79.26%   | 49.42%    | 77.25% | 60.28%   | #4   |
| Neural Network      | 78.80%   | 48.67%    | 74.79% | 58.97%   | #5   |
| KNN                 | 74.43%   | 42.84%    | 76.43% | 54.91%   | #6   |
| Logistic Regression | 75.00%   | 42.65%    | 65.96% | 51.79%   | #7   |

Best Performing Model: ` XGBoost `\
Key Features Influencing Churn: `[Age, Number of Products Purchased/Used, Balanced, Active Member]`\
![image](https://github.com/user-attachments/assets/7d4e4adf-45b1-48e8-848b-8478339acd81)

Business Impact: `"This model helps identify at-risk customers early, allowing targeted retention strategies."`

## How to Run the Notebooks

1. **Clone this repository:**
   ```bash
   git clone https://github.com/ColbyRobinson/bank-customer-churn-prediction.git
   cd bank-customer-churn-prediction
   ```
2. **Open Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
3. **Run the notebooks in the following order:**
   - `Data_preprocessing.ipynb`
   - `EDA_bank_customer_churn.ipynb`
   - `Modeling_DT_RF_XG.ipynb`
   - `Modeling_LogReg_SVM_NN_KNN.ipynb`
   - `Model Comparison and Assessment.ipynb`

## Key Takeaways

- **Best Performing Model:** `[Insert Model Name]`
- **Churn Prediction Can Help Businesses:** `[Explain how it helps business decision-making]`

## Contact

For any questions, reach out via:

- **GitHub Issues**
- **LinkedIn / Email**
GitHub Issues

LinkedIn / Email

