# bank-customer-churn-prediction
Bank Customer Churn Prediction End to End Project.
# Bank Customer Churn Prediction

## Project Overview

Dataset: https://www.kaggle.com/datasets/radheshyamkollipara/bank-customer-churn

This project aims to **predict customer churn** using machine learning models. The goal is to analyze customer behavior, preprocess data, and compare multiple models to determine the best-performing one for churn prediction. This workflow includes:

- **Exploratory Data Analysis (EDA)**: Understanding patterns and relationships in the dataset.
- **Data Preprocessing**: Cleaning and transforming raw customer data.
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
# Methodology
## Exploratory Data Analysis

The Exploratory Data Analysis (EDA) phase began by loading and inspecting the Bank Customer Churn dataset. A comprehensive analysis was conducted, starting with an assessment of missing values, duplicate records, and data types. Detailed descriptive statistics and visualizations were used to understand feature distributions and identify potential outliers. The churn rate distribution was visualized to understand class imbalance. Relationships between variables were explored using correlation analysis, boxplots, histograms, and density plots to detect meaningful patterns or anomalies. Important insights regarding correlations and potential predictive factors of churn were identified, guiding subsequent preprocessing and modeling decisions.

### Churn Distribution:

![image](https://github.com/user-attachments/assets/77351637-6b50-4d67-9211-ab6dc036f188)



### Summary Statistics:

![image](https://github.com/user-attachments/assets/4044397c-6d31-4097-bf4a-01389d53c815)



### Correlation Matrix:

![image](https://github.com/user-attachments/assets/ff30de1a-21d3-4912-ba1d-607091dabd66)



### Feature Distributions:

![image](https://github.com/user-attachments/assets/523fac64-f43d-449d-9810-bfd130f5d3d3)


### Churn Rate by Categorical Variables:

![image](https://github.com/user-attachments/assets/b3428cb8-12cc-44a5-9afb-48d5622893eb)



![image](https://github.com/user-attachments/assets/79bc9237-1da8-4754-a77a-640185d6e90f)



![image](https://github.com/user-attachments/assets/26de5475-e1a0-4064-b3ba-6918472a60a7)



### Feature Distributions by Churn Status:

![image](https://github.com/user-attachments/assets/f4e53d49-7abb-4d88-bd9a-ab8c1dd27fcd)



![image](https://github.com/user-attachments/assets/fb202486-0d4d-4a3e-919c-b04765b16110)



### Boxplots for Outlier Detection:

![image](https://github.com/user-attachments/assets/057f8994-a4fc-4cea-a6a7-1470691a0266)


### Data Preprocessing

The data preprocessing phase involved several critical steps to ensure the data was suitable for modeling. First, Categorical variables underwent one-hot encoding, label encoding, and ordinal encoding to transform them into numeric formats compatible with machine learning models. Feature scaling was applied to normalize numeric variables, specifically using Min-Max scaling, ensuring uniformity across the dataset. Furthermore, the dataset was split into training and test sets, maintaining stratified sampling to preserve the original class distribution of the churn variable. This careful preprocessing facilitated optimal model performance and comparability across various algorithms.

Label Encoding was done for the following variables:
[Gender]

One-Hot Encoding was done for the following variables:
[Geography]

Ordinal Encoding was done for the following variables:
[Card Type]

Identify Outliers & Applied Winsorization:
Outliers were detected for [Credit Score], [Age], and [NumOfProducts] to apply winsorization and cap the extreme values.

Feature Scaling & Transformation:
Standard Scaler from sklearn was used to apply scaling to: [Credit Score], [Age], [Tenure], [Balance], [NumOfProducts], [Estimated Salary], [PointEarned]

## Training & Tuning Models

The training phase utilized a wide array of machine learning algorithms, including Logistic Regression, Support Vector Machines (SVM), Neural Networks (NN), K-Nearest Neighbors (KNN), Decision Trees, Random Forests, and XGBoost. Random Undersampling was performed on the preprocessed dataset to resolve the issue of having an imbalanced dataset. Feature selection was performed using Recursive Feature Elemination (RFE). Hyperparameter tuning was performed using Grid Search with cross-validation, optimizing each model’s predictive performance. Evaluation metrics such as Accuracy, Precision, Recall, and F1-score were systematically employed to assess model performance. The Decision Tree, Random Forest, and XGBoost algorithms particularly benefited from tuning and emerged among the top-performing models based on Recall, F1 scores, and balanced accuracy metrics. Since acquiring new customers is more expensive than retaining your current customers, the models were tuned to optimize Recall while maintaining a proficient score for all other assessment measures. The best-performing models were identified based on test dataset results, with XGBoost notably outperforming others on recall and overall F1-score, establishing it as the final model choice for predicting customer churn.

### Logistic Regression:

![image](https://github.com/user-attachments/assets/b0341b9c-6fbd-4388-8088-90d8511a79c3)



![image](https://github.com/user-attachments/assets/7777a534-e694-4976-8132-7dc090936f53)



### SVM:

![image](https://github.com/user-attachments/assets/003a3c9f-32a3-4fd0-9216-ef9e8f3943eb)



![image](https://github.com/user-attachments/assets/a4d8be99-6c83-4ccb-8a17-f9c5f11f944e)



### Neural Network:

![image](https://github.com/user-attachments/assets/83a19df8-3b34-4bb4-82cf-bf8b50a0bc03)



![image](https://github.com/user-attachments/assets/db46b3c4-a273-452b-9343-53328503e465)



### KNN: 

![image](https://github.com/user-attachments/assets/e24458b1-a99b-4fc8-9393-02a4925ff07d)



![image](https://github.com/user-attachments/assets/03ec9ffe-2cda-4f80-9a3f-34d125bebd7c)


### Decision Tree:

![image](https://github.com/user-attachments/assets/44cdccb0-1885-49a7-933d-c0141d546863)



![image](https://github.com/user-attachments/assets/a6f22ea4-4e56-4142-ad49-9ba19d0e71da)



### Random Forest:

![image](https://github.com/user-attachments/assets/3a9b095f-2cbd-4bdb-9e56-75bf9093ce93)



![image](https://github.com/user-attachments/assets/a6c9accd-6c74-4dc3-b108-ca35d10f2e9b)



### XGBoost:

![image](https://github.com/user-attachments/assets/644b3805-aef8-42eb-968d-f087b000007f)



![image](https://github.com/user-attachments/assets/b2aa80b5-62ca-4386-9afb-ff89d9c6c975)



# Model Comparison Results (Test)

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

#1. Clone this repository:

git clone https://github.com/ColbyRobinson/bank-customer-churn-prediction.git
cd bank-customer-churn-prediction

#2. (Optional) Install dependencies:
If you have a requirements.txt file, install the necessary dependencies using:

pip install -r requirements.txt

#3. Open Jupyter Notebook:

jupyter notebook

#4. Run the notebooks in the following order:

EDA_bank_customer_churn.ipynb  (Exploratory Data Analysis & visualization)

Data_preprocessing.ipynb  (Data cleaning, encoding, transformation)

Modeling_DT_RF_XG.ipynb  (Training Decision Tree, Random Forest, XGBoost)

Modeling_LogReg_SVM_NN_KNN.ipynb  (Training Logistic Regression, SVM, Neural Network, KNN)

Model Comparison and Assessment.ipynb  (Comparing model performance & selecting the best model)


## Key Takeaways

- **Best Performing Model:** `XGBoost`
- **Churn Prediction Can Help Businesses:** `Churn prediction allows businesses to identify customers at risk of leaving, providing insights that enable proactive retention strategies. By leveraging machine learning models, companies can:

- Reduce Customer Attrition: By detecting churn patterns early, businesses can implement personalized retention efforts such as special offers, loyalty programs, or improved customer support.
- Optimize Marketing Strategies: Focus marketing efforts on high-risk customers with targeted engagement campaigns instead of spending resources on customers who are unlikely to churn.
- Enhance Customer Experience: Identifying key pain points and dissatisfaction factors helps businesses refine their products, pricing, and service offerings to improve overall satisfaction.
- Increase Revenue & Profitability: Retaining existing customers is 5x cheaper than acquiring new ones. Churn prediction helps boost customer lifetime value (CLV) and minimize revenue loss.
- Data-Driven Decision-Making: Businesses can leverage churn insights to improve operational strategies, refine product offerings, and prioritize high-value customers.
- By implementing a churn prediction model, companies can make data-driven decisions, reduce churn rates, and maximize customer retention, leading to sustainable growth and profitability.`

## Contact

For any questions, reach out via:

- **GitHub Issues**
- **LinkedIn / Email**

GitHub Issues:

Email:
@ thecolbyrobinson@gmail.com

LinkedIn:
linkedin.com/in/colby-robinson-869148172

