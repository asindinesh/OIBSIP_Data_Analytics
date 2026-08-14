
#  House Price Prediction using Linear Regression

##  Project Overview

This project was completed as **Level 2 – Task 1** during my **Data Analytics Internship at OASIS Infobyte (OIBSIP)**.

The objective of this project is to build a **Machine Learning model using Linear Regression** to predict house prices based on various property features from the **Ames Housing Dataset**.

The project covers the complete workflow from **data exploration and preprocessing to model training, evaluation, visualization, and interpretation**.

---

##  Objective

To develop and evaluate a Linear Regression model that can predict the **sale price of houses** using features such as:

* Overall quality
* Living area
* Number of bedrooms and bathrooms
* Garage capacity
* Year built
* Neighborhood
* Basement features
* And other property characteristics

---

##  Dataset

The project uses the **Ames Housing Dataset**, which contains information about residential properties and their corresponding sale prices.

* **Rows:** 1,460
* **Features:** 80 input features
* **Target Variable:** `SalePrice`

### Important Features

| Feature        | Description                         |
| -------------- | ----------------------------------- |
| `OverallQual`  | Overall material and finish quality |
| `GrLivArea`    | Above-ground living area            |
| `GarageCars`   | Garage car capacity                 |
| `GarageArea`   | Garage area                         |
| `YearBuilt`    | Original construction year          |
| `FullBath`     | Number of full bathrooms            |
| `BedroomAbvGr` | Bedrooms above ground               |
| `Neighborhood` | Physical location of the property   |
| `SalePrice`    | Target house selling price          |

---

##  Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Jupyter Notebook**

---

##  Project Workflow

### 1. Exploratory Data Analysis

Performed:

* Dataset inspection
* Data types analysis
* Missing-value analysis
* Descriptive statistics
* Target variable distribution

### 2. Data Preprocessing

* Handled missing values
* Used median imputation for numerical features
* Used mode imputation for categorical features
* Applied **One-Hot Encoding** to categorical variables

### 3. Correlation Analysis

A correlation heatmap was created to identify relationships between numerical features and `SalePrice`.

Features such as **Overall Quality** and **Living Area** showed strong relationships with house prices.

### 4. Train-Test Split

The dataset was divided into:

* **80% Training Data**
* **20% Testing Data**

### 5. Model Building

A **Linear Regression** model was trained using Scikit-learn.

### 6. Model Evaluation

The model was evaluated using:

* **Mean Squared Error (MSE)**
* **Root Mean Squared Error (RMSE)**
* **R² Score**

### 7. Visualization

Created:

* Actual vs. Predicted Price Scatter Plot
* Residual Plot
* Correlation Heatmap

### 8. Coefficient Analysis

Analyzed Linear Regression coefficients to identify features with the highest positive and negative influence on predicted house prices.

### 9. Ridge Regression

As a bonus, **Ridge Regression** was implemented and compared with the Linear Regression model to understand the effect of regularization.

---

##  Model Evaluation

The following metrics were used:

### Mean Squared Error (MSE)

Measures the average squared difference between actual and predicted prices.

**Lower MSE indicates better performance.**

### Root Mean Squared Error (RMSE)

RMSE is the square root of MSE and represents the prediction error in the same unit as house price.

**Lower RMSE indicates better performance.**

### R² Score

R² measures how much of the variation in house prices is explained by the model.

**Higher R² indicates better model performance.**

---

##  Visualizations

### Actual vs. Predicted Prices

The scatter plot compares actual house prices with predicted prices. Points closer to the diagonal reference line indicate better predictions.

### Residual Plot

The residual plot helps identify whether prediction errors are randomly distributed around zero.

### Correlation Heatmap

The heatmap helps identify features that have stronger relationships with the target variable.

---

##  Key Learnings

Through this project, I gained practical experience in:

* Exploratory Data Analysis
* Data cleaning and preprocessing
* Handling missing values
* Categorical feature encoding
* Correlation analysis
* Linear Regression
* Model evaluation
* Residual analysis
* Feature coefficient interpretation
* Ridge Regression
* Data visualization using Matplotlib and Seaborn

---

##  Project Structure

```text
Level2 Task 1 - Predicting House Prices/
│
├── Predicting House Prices.ipynb
├── train.csv
└── README.md
```



##  Internship

**Program:** Data Analytics Internship
**Organization:** OASIS Infobyte
**Level:** Level 2
**Task:** Task 1 – Predicting House Prices with Linear Regression

---

##  Author

**Asin D**

---

⭐ *This project was developed as part of my learning journey in Data Analytics and Machine Learning.*
