# 🛒 Big Mart Sales Prediction

## 📌 Project Overview

This project aims to predict the sales of products at Big Mart outlets using machine learning techniques. Accurate sales prediction helps retail businesses optimize inventory, pricing strategies, and supply chain decisions.

The model leverages historical data containing product attributes and outlet characteristics to estimate the target variable: **Item Outlet Sales**.

## 📂 Dataset Description

The dataset consists of 8,523 records with 12 features, combining both numerical and categorical data.

### Key Features:

* **Product-level attributes**: weight, visibility, type, price (MRP), fat content
* **Outlet-level attributes**: size, location type, establishment year, outlet type
* **Target variable**: Item Outlet Sales

The dataset includes missing values and categorical inconsistencies, requiring preprocessing before model training.

## ⚙️ Methodology

### 1. Data Preprocessing

Data preprocessing was a critical step in preparing the dataset for machine learning:

* **Handling Missing Values**

  * Missing values in *Item Weight* were replaced using the mean.
  * Missing values in *Outlet Size* were filled using the mode, conditioned on outlet type to preserve contextual relevance.

* **Data Cleaning**

  * Inconsistent categorical values (e.g., “LF”, “low fat”, “reg”) were standardized into unified categories.

### 2. Exploratory Data Analysis (EDA)

EDA was performed to understand data distribution and patterns:

* Distribution analysis of numerical features such as price, visibility, and sales
* Identification of skewness and spread in data
* Frequency analysis of categorical variables
* Insights into how outlet characteristics influence sales

### 3. Feature Engineering & Encoding

Since machine learning models require numerical inputs:

* All categorical variables were converted into numerical format using encoding techniques
* Label encoding was applied to transform categories into integer representations

### 4. Model Building

The model used in this project is **XGBoost Regressor**, a powerful gradient boosting algorithm known for:

* High performance on structured/tabular data
* Ability to capture complex feature interactions
* Built-in regularization to reduce overfitting

### 5. Model Evaluation

The model performance was evaluated using the **R² (coefficient of determination)** metric.

* **Training Score**: ~0.98
* **Testing Score**: ~0.88

This indicates that:

* The model learns patterns very well from training data
* There is a slight drop in test performance, suggesting mild overfitting

## 📈 Key Insights

* Product price (MRP) has a strong influence on sales
* Outlet characteristics such as type and location significantly impact performance
* Data preprocessing and cleaning play a crucial role in improving model accuracy
* Gradient boosting models are highly effective for retail prediction problems


## 🧠 Tech Stack

* Python
* Pandas & NumPy
* Matplotlib & Seaborn
* Scikit-learn
* XGBoost

## 📌 Conclusion

This project demonstrates a complete machine learning workflow—from data preprocessing to model evaluation—for solving a real-world regression problem. It highlights the importance of data cleaning, feature transformation, and model selection in building accurate predictive systems.
