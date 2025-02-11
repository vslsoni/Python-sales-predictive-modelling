# Python-sales-predictive-modelling
# Retail Sales Prediction

## Project Overview
This project focuses on building and evaluating predictive models for forecasting **sales in Rossmann drug stores**. Given historical sales data and various influencing factors such as promotions, competition, holidays, and store attributes, the goal is to develop a robust predictive model. The best-performing model is integrated into a **Gradio-based interface**, allowing users to input store features and obtain sales predictions.

## Business Context
Rossmann operates over **3,000 stores** across **7 European countries**. Store managers manually predict daily sales weeks in advance, leading to inconsistencies in accuracy. This project aims to automate and improve sales forecasting using **machine learning models** trained on historical sales data for **1,115 stores**.

## Objectives
- Clean and preprocess historical sales data.
- Train multiple machine learning models and evaluate their performance.
- Optimize hyperparameters to improve prediction accuracy.
- Deploy the best model using **Gradio** for interactive sales forecasting.

## Key Components

### Data Preparation
- Merged **sales data** (`rossman.csv`) with **store details** (`store.csv`).
- Handled missing values, outliers, and incorrect data formats.
- Extracted **date-based features** (day, month, year) from the `Date` column.
- One-hot encoded categorical variables for model compatibility.

### Model Training & Evaluation
Implemented and compared multiple regression models:

1. **Linear Regression**
2. **Decision Tree Regressor**
3. **Random Forest Regressor**
4. **K-Nearest Neighbors (KNN) Regressor**
5. **XGBoost Regressor**
6. **Random Forest with PCA**
7. **XGBoost with PCA**

Metrics used for evaluation:
- **Root Mean Squared Error (RMSE)**
- **Mean Absolute Error (MAE)**
- **R² Score**

### Hyperparameter Tuning
- Performed **Randomized Search Cross-Validation** to fine-tune `RandomForestRegressor`.
- Selected the best hyperparameters to improve model performance.

### Feature Engineering
- Applied **Principal Component Analysis (PCA)** for dimensionality reduction.
- Analyzed variance contribution of principal components.

### Model Deployment
- Developed a **Gradio-based interface** for real-time sales prediction.
- Users input store attributes, promotions, and date information to receive **predicted sales figures**.

## Gradio Interface
The deployed model is accessible via a **Gradio web interface**, where users provide the following inputs:
- **Store ID** (1-1115)
- **Customer Count**
- **Promotion Status** (Promo, Promo2)
- **State Holiday Type**
- **School Holiday Indicator**
- **Store Type & Assortment**
- **Competition Distance**
- **Date (YYYY-MM-DD)**

The model processes these inputs and returns an estimated sales figure.

## Conclusion
By leveraging machine learning techniques, this project enhances **sales forecasting accuracy** for Rossmann stores. The integration of a **user-friendly Gradio interface** allows store managers to **quickly predict sales** based on relevant factors, improving business decision-making. Hyperparameter tuning and feature engineering further **optimize model performance**, ensuring reliable predictions.

