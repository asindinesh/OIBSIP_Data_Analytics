# Task 3 – Data Cleaning Using Python

##  Project Overview

This project was completed as part of my **Data Analytics Internship at OASIS Infobyte**.

The objective of this task is to demonstrate professional data cleaning skills by taking a dataset containing missing values, duplicate records, inconsistent formatting, and potential outliers, and transforming it into a clean, analysis-ready dataset.

For this project, the **Titanic dataset** was used to perform systematic data quality assessment and preprocessing using Python.

##  Objective

The main objective is to:

* Identify data quality issues
* Handle missing values appropriately
* Remove duplicate records
* Standardize inconsistent data
* Detect and treat outliers
* Correct data types
* Compare the dataset before and after cleaning
* Export the final cleaned dataset as a CSV file

##  Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Jupyter Notebook**

##  Dataset

The **Titanic dataset** contains information about passengers, including:

* Passenger ID
* Survival status
* Passenger class
* Name
* Sex
* Age
* Number of siblings/spouses aboard
* Number of parents/children aboard
* Ticket
* Fare
* Cabin
* Port of Embarkation

##  Data Cleaning Process

### 1. Data Quality Assessment

The dataset was examined to identify:

* Missing values
* Duplicate rows
* Incorrect data types
* Numerical range anomalies
* General data inconsistencies

### 2. Missing Value Handling

Different strategies were applied depending on the nature of each column:

* **Age:** Missing values were replaced using the median.
* **Embarked:** Missing categorical values were replaced using the mode.
* **Cabin:** The column was removed because it contained a large proportion of missing values.

### 3. Duplicate Removal

Duplicate records were identified using Pandas and removed to ensure that each observation was unique.

### 4. Data Standardization

Inconsistent text formatting was standardized in columns such as:

* `Sex`
* `Embarked`
* `Name`

Whitespace was removed and categorical values were normalized.

### 5. Outlier Detection

The **Interquartile Range (IQR)** method was used to identify potential outliers in numerical data.

The IQR was calculated as:

`IQR = Q3 - Q1`

Values outside:

`Q1 - 1.5 × IQR`

and

`Q3 + 1.5 × IQR`

were considered potential outliers and treated appropriately.

### 6. Data Type Correction

Data types were reviewed and corrected where necessary to ensure that the dataset was suitable for further analysis.

### 7. Before vs After Comparison

A summary comparison was created to evaluate the improvement in data quality after cleaning, including:

* Row count
* Null values
* Duplicate records
* Data types

##  Key Outcome

The dataset was successfully transformed from a raw dataset into a cleaner and more analysis-ready dataset.

The cleaning process improved data consistency, handled missing information, removed duplicate records, and addressed potential outliers.

##  Project Files

```text
Task3_Data_Cleaning/
│
├── Task3_DataCleaning.ipynb
├── Titanic.csv
├── cleaned_titanic.csv
└── README.md
```

### Files Description

* **Task3_DataCleaning.ipynb** – Complete Jupyter Notebook containing the data cleaning process.
* **Titanic.csv** – Original dataset used for the project.
* **cleaned_titanic.csv** – Final cleaned dataset.
* **README.md** – Project documentation.

##  Conclusion

This project provided practical experience in **data preprocessing and data quality management using Python**. It strengthened my understanding of handling missing data, duplicate records, inconsistent values, outliers, and data types.

The resulting cleaned dataset can now be used confidently for further **exploratory data analysis and machine learning applications**.

##  Author

**Asin D**

Data Analytics Intern – OASIS Infobyte

