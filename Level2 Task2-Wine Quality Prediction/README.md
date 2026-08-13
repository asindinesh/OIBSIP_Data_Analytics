#  Wine Quality Prediction
##  Project Overview

Wine quality is influenced by several physicochemical properties such as acidity, density, sulphates, and alcohol content. This project applies machine learning classification techniques to predict the quality category of wine based on these measurable properties.
The original wine quality scores were transformed into three categories to address the significant class imbalance in the dataset:
- **Low:** Quality scores 3–5
- **Medium:** Quality score 6
- **High:** Quality scores 7–8

Three classification algorithms were implemented and compared:

- Random Forest Classifier
- SGD Classifier
- Support Vector Classifier (SVC)

The models were evaluated using accuracy, precision, recall, F1-score, and confusion matrices.

##  Objectives

The primary objectives of this project are to:

- Explore and understand the Wine Quality dataset.
- Analyze the distribution of wine quality scores.
- Identify and discuss class imbalance.
- Perform exploratory data analysis on physicochemical features.
- Engineer a meaningful target variable for classification.
- Train and compare multiple machine learning classifiers.
- Evaluate model performance using multiple classification metrics.
- Analyze Random Forest feature importance.
- Select the most suitable model for wine quality classification.

##  Dataset

The dataset contains physicochemical measurements of wine along with an associated quality score.

### Features

| Feature | Description |
|---|---|
| Fixed Acidity | Concentration of fixed acids in the wine |
| Volatile Acidity | Concentration of volatile acids |
| Citric Acid | Amount of citric acid present |
| Residual Sugar | Amount of sugar remaining after fermentation |
| Chlorides | Chloride concentration |
| Free Sulfur Dioxide | Free sulfur dioxide concentration |
| Total Sulfur Dioxide | Total sulfur dioxide concentration |
| Density | Density of the wine |
| pH | Acidity level of the wine |
| Sulphates | Sulphate concentration |
| Alcohol | Alcohol content |
| Quality | Original wine quality score |

The `Id` column was excluded from model training because it serves only as an identifier and does not represent a meaningful physicochemical property.

##  Class Distribution and Imbalance

The original quality scores were distributed as follows:

| Quality Score | Samples |
|---:|---:|
| 3 | 6 |
| 4 | 33 |
| 5 | 483 |
| 6 | 462 |
| 7 | 143 |
| 8 | 16 |

The dataset is highly imbalanced, with quality scores **5 and 6 accounting for the majority of observations**, while scores 3 and 8 contain very few samples.

This imbalance can cause classification models to favor majority classes and perform poorly on minority classes. Therefore, evaluation was not based on accuracy alone; macro-averaged precision, recall, F1-score, and confusion matrices were also considered.

##  Feature Engineering

To reduce the effect of the severe class imbalance while retaining meaningful quality information, the original quality scores were grouped into three classes:

| Quality Scores | Category | Encoded Value |
|---|---|---:|
| 3–5 | Low | 0 |
| 6 | Medium | 1 |
| 7–8 | High | 2 |

A three-class classification problem was selected instead of binary classification because it preserves more information about the quality level of the wine.

##  Exploratory Data Analysis

The following analyses were performed:

- Dataset structure and dimensionality analysis
- Descriptive statistical analysis
- Missing-value inspection
- Duplicate-value inspection
- Quality score distribution
- Distribution plots for physicochemical features
- Boxplots for feature analysis and outlier identification
- Correlation heatmap

The correlation analysis was used to understand relationships between physicochemical properties and identify potentially influential features.

## Data Preparation

The dataset was prepared for machine learning using the following steps:

1. Loaded the dataset using Pandas.
2. Inspected the dataset structure and data types.
3. Checked for missing values and duplicates.
4. Removed the identifier column.
5. Created the three-class target variable.
6. Separated features and target.
7. Split the dataset into training and testing sets.
8. Used **stratified sampling** to preserve class proportions.
9. Standardized features for models requiring feature scaling.

The dataset was divided into:

- **80% Training Data**
- **20% Testing Data**

## 🤖 Machine Learning Models

### 1.  Random Forest Classifier

Random Forest is an ensemble learning algorithm that combines multiple decision trees to produce robust classification predictions.

It was selected because it can model nonlinear relationships and provides feature importance values that help interpret the model.

### 2.  SGD Classifier

The Stochastic Gradient Descent (SGD) Classifier is an efficient linear classification algorithm suitable for large datasets.

Feature standardization was applied before training the model.

### 3.  Support Vector Classifier (SVC)

Support Vector Classification identifies decision boundaries that separate different classes.

An RBF kernel was used to capture nonlinear relationships between the physicochemical features and wine quality categories.

Feature scaling was applied before training.

##  Model Evaluation

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Macro Precision
- Macro Recall
- Macro F1-score
- Confusion Matrix

Macro-averaged metrics were particularly important because of the class imbalance in the dataset.

##  Model Comparison

| Model | Accuracy | Macro Precision | Macro Recall | Macro F1 |
|---|---:|---:|---:|---:|
| **Random Forest** | **72.5%** | **74.6%** | **70.9%** | **72.4%** |
| SVC | 61.1% | 57.2% | 60.9% | 58.2% |
| SGD Classifier | 53.7% | 49.7% | 54.1% | 49.5% |

### Performance Summary

The **Random Forest Classifier** achieved the highest performance among the three evaluated models.

It obtained:

- **Accuracy:** 72.5%
- **Macro Precision:** 74.6%
- **Macro Recall:** 70.9%
- **Macro F1-score:** 72.4%

The results indicate that Random Forest provided the best overall balance between precision and recall for the three wine quality categories.

##  Feature Importance

Random Forest feature importance was analyzed to understand the relative contribution of each physicochemical feature to the model's predictions.

A feature importance table and visualization were generated in the Jupyter Notebook.

This analysis improves model interpretability by showing which wine properties contribute most strongly to classification decisions.

##  Prediction

The trained Random Forest model can be used to classify a new wine based on its physicochemical properties.

The model produces one of three quality categories:
Low
Medium
High

# Conclusion :

This project demonstrates the application of machine learning classification techniques to wine quality prediction.

Exploratory analysis revealed significant class imbalance in the original quality scores. To address this issue, the quality scores were transformed into three meaningful categories: Low, Medium, and High.

Three classification algorithms—Random Forest, SGD, and SVC—were trained and evaluated using a stratified train-test split.

Among the evaluated models, Random Forest achieved the best performance, with an accuracy of 72.5% and a Macro F1-score of 72.4%.

Therefore, Random Forest was selected as the most suitable model among the tested approaches for this dataset. Its feature importance analysis also provides useful insight into the physicochemical factors influencing wine quality classification.
