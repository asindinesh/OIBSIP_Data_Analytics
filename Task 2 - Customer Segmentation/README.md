#  Customer Segmentation Analysis Using K-Means Clustering

##  Project Overview

This project focuses on **Customer Segmentation Analysis** for an e-commerce business using **RFM (Recency, Frequency, Monetary) Analysis** and the **K-Means Clustering** algorithm.

The goal is to identify distinct groups of customers based on their purchasing behaviour and provide **targeted marketing strategies** for each customer segment.

This project was completed as **Task 2 of my Data Analytics Internship at Oasis Infobyte**.

##  Objective

The main objectives of this project are to:

* Analyze customer purchasing behaviour.
* Perform data cleaning and preprocessing.
* Calculate RFM metrics for each customer.
* Standardize the behavioural features.
* Determine the optimal number of clusters using the **Elbow Method**.
* Apply **K-Means Clustering** to segment customers.
* Visualize and profile the identified customer groups.
* Provide actionable marketing recommendations for each segment.

##  Dataset

The project uses an **Online Retail / E-commerce transaction dataset** containing customer purchase information.

### Important Features

* `CustomerID` – Unique customer identifier
* `InvoiceNo` – Transaction/invoice number
* `InvoiceDate` – Date and time of transaction
* `Quantity` – Number of products purchased
* `UnitPrice` – Price per product
* `Country` – Customer's country

A new feature, `TotalPrice`, was calculated as:

**TotalPrice = Quantity × UnitPrice**

##  RFM Analysis

RFM analysis was used to represent customer purchasing behaviour through three important metrics:

### Recency

Measures how recently a customer made a purchase.

**Lower Recency indicates more recent activity.**

### Frequency

Measures how frequently a customer makes purchases.

**Higher Frequency indicates more repeated purchases.**

### Monetary

Measures the total amount spent by a customer.

**Higher Monetary value indicates greater customer value.**


##  Methodology

The project follows these steps:

1. Load and inspect the dataset.
2. Handle missing and inconsistent data.
3. Remove cancelled and invalid transactions.
4. Calculate total purchase value.
5. Perform RFM analysis.
6. Select Recency, Frequency, and Monetary features.
7. Standardize the features using `StandardScaler`.
8. Apply the Elbow Method to determine the optimal number of clusters.
9. Perform K-Means clustering.
10. Visualize the customer segments.
11. Profile each cluster using average RFM values.
12. Develop marketing recommendations.


##  Machine Learning Algorithm

### K-Means Clustering

K-Means is an **unsupervised machine learning algorithm** used to group similar data points into clusters.

In this project, customers were grouped based on their:

* Recency
* Frequency
* Monetary value

The **Elbow Method** was used to determine the appropriate number of clusters.

The analysis identified **3 customer segments**.

##  Customer Segments

| Cluster   | Customer Type      | Key Characteristics                                                |
| --------- | ------------------ | ------------------------------------------------------------------ |
| Cluster 0 | At-Risk / Inactive | High recency, low frequency, low monetary value                    |
| Cluster 1 | Regular / Loyal    | Moderate recency, frequency, and monetary value                    |
| Cluster 2 | VIP / High-Value   | Very recent purchases, extremely high frequency and monetary value |

###  Cluster 0 – At-Risk / Inactive Customers

These customers have not purchased recently and show relatively low purchasing activity.

**Recommended Strategy:**

* Re-engagement campaigns
* Personalized discounts
* Reminder emails
* Limited-time offers

### 🟡 Cluster 1 – Regular / Loyal Customers

This is the largest customer segment and represents customers with regular purchasing behaviour.

**Recommended Strategy:**

* Loyalty programs
* Personalized recommendations
* Cross-selling
* Upselling
* Retention campaigns

###  Cluster 2 – VIP / High-Value Customers

This segment contains a small number of customers with exceptionally high purchasing frequency and monetary value.

**Recommended Strategy:**

* VIP loyalty programs
* Exclusive offers
* Early access to new products
* Personalized services
* Premium customer support

##  Visualizations

The project includes:

* RFM distribution plots
* Elbow Method plot
* Recency vs Frequency scatter plot
* Frequency vs Monetary scatter plot
* Customer count per cluster bar chart
* Cluster profiling

##  Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Matplotlib**
* **Seaborn**
* **Jupyter Notebook**

##  Key Insights

The analysis demonstrates that customers have significantly different purchasing behaviours.

A large portion of customers belong to the regular/loyal segment, while a small group of highly valuable customers shows exceptionally high purchase frequency and spending.

The segmentation enables businesses to move from a **one-size-fits-all marketing strategy** to a more targeted approach based on customer behaviour.


## Project Structure

text
Customer-Segmentation-Analysis/
│
├── Customer Segmentation.ipynb
├── online_retail.csv.zip
└── README.md

##  Conclusion

This project demonstrates how **RFM analysis and K-Means clustering** can be combined to understand customer behaviour and create actionable customer segments.

The resulting segments can help an e-commerce business improve:

* Customer retention
* Personalized marketing
* Customer loyalty
* Revenue generation
* Marketing resource allocation

##  Internship

**Internship:** Data Analytics Internship
**Organization:** Oasis Infobyte
**Task:** Task 2 – Customer Segmentation Analysis

---

## ⭐ Acknowledgement

I would like to thank **Oasis Infobyte** for providing this opportunity to apply data analytics and machine learning concepts to a practical business problem.

