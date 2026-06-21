🛍️ Customer Segmentation Analysis Using Machine Learning
📖 Introduction

Understanding customers is essential for every business. Different customers have different purchasing habits, spending capacities, and preferences. Treating all customers the same often leads to ineffective marketing and reduced customer engagement.

This project uses Customer Segmentation Analysis to divide customers into meaningful groups based on their purchasing behavior and demographic characteristics. Using the K-Means Clustering Algorithm, customers are grouped into distinct segments, enabling businesses to create targeted marketing strategies and improve customer satisfaction.

🎯 Objective

The main objective of this project is to:

Analyze customer purchasing behavior.
Identify patterns in customer data.
Segment customers into meaningful groups.
Generate business insights for personalized marketing.
Improve customer retention and revenue generation.
📂 Dataset Overview

The dataset contains customer information such as:

Column Name	Description
CustomerID	Unique customer identifier
Gender	Gender of customer
Age	Age of customer
Annual Income (k$)	Annual income of customer
Spending Score (1-100)	Spending behavior score assigned by the business
🛠️ Tools and Technologies
Programming Language
Python
Libraries Used
Pandas
NumPy
Matplotlib
Seaborn
Scikit-Learn
Development Environment
Jupyter Notebook
🔄 Project Workflow
Step 1: Import Libraries

Required Python libraries were imported for data analysis, visualization, and machine learning.

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.cluster import KMeans

Step 2: Load Dataset
The dataset was loaded into a Pandas DataFrame.
df = pd.read_csv("Customer_Segmentation.csv")

Step 3: Data Understanding
The dataset structure was explored.

Tasks Performed
Displayed first few records
Checked dataset shape
Examined column names
Verified data types
df.head()
df.shape
df.info()

Step 4: Data Cleaning
Data preprocessing was performed to improve data quality.

Cleaning Activities

✔ Removed duplicate records

✔ Checked missing values

✔ Validated data types

✔ Corrected inconsistent entries

df.isnull().sum()
df.duplicated().sum()

Step 5: Exploratory Data Analysis (EDA)
EDA was performed to understand customer demographics and purchasing behavior.

Customer Gender Distribution
sns.countplot(x='Gender', data=df)
plt.show()
Age Distribution
sns.histplot(df['Age'], bins=20)
plt.show()
Annual Income Distribution
sns.histplot(df['Annual Income (k$)'])
plt.show()
Spending Score Distribution
sns.histplot(df['Spending Score (1-100)'])
plt.show()
📊 Descriptive Statistics

Statistical measures were calculated to summarize customer data.

Metrics Analyzed
Mean Age
Average Income
Average Spending Score
Minimum and Maximum Values
Standard Deviation
df.describe()
Findings
Majority of customers belong to middle-age groups.
Income levels vary significantly.
Spending behavior differs across customer groups.
🤖 Machine Learning Approach
K-Means Clustering

K-Means is an unsupervised machine learning algorithm used to divide data into clusters based on similarity.

Why K-Means?
Simple and efficient
Easy to interpret
Widely used for customer segmentation
📈 Finding Optimal Number of Clusters

The Elbow Method was used to determine the ideal number of customer segments.

wcss = []

for i in range(1,11):
    kmeans = KMeans(n_clusters=i)
    kmeans.fit(X)
    wcss.append(kmeans.inertia_)
Elbow Curve

The point where the curve bends sharply represents the optimal number of clusters.

Result:

Optimal Clusters = 5

🎯 Customer Segmentation

The K-Means model was trained using:

Annual Income
Spending Score
X = df[['Annual Income (k$)',
        'Spending Score (1-100)']]

Model Training:

kmeans = KMeans(n_clusters=5,
                random_state=42)

df['Cluster'] = kmeans.fit_predict(X)
📉 Cluster Visualization

Scatter plots were created to visualize customer groups.

plt.scatter(
    df['Annual Income (k$)'],
    df['Spending Score (1-100)'],
    c=df['Cluster']
)
plt.show()

The visualization clearly shows distinct customer segments.

👥 Customer Segments Analysis
Cluster 1: Premium Customers

Characteristics:

High Income
High Spending Score

Business Strategy:

VIP membership
Exclusive offers
Premium services
Cluster 2: Careful Customers

Characteristics:

High Income
Low Spending

Business Strategy:

Personalized recommendations
Special promotions
Loyalty campaigns
Cluster 3: Standard Customers

Characteristics:

Average Income
Average Spending

Business Strategy:

Regular engagement
Product recommendations
Cluster 4: Budget Customers

Characteristics:

Low Income
Low Spending

Business Strategy:

Discount campaigns
Affordable product bundles
Cluster 5: Enthusiastic Customers

Characteristics:

Low Income
High Spending

Business Strategy:

Cashback offers
Reward programs
Seasonal discounts
🔍 Key Insights
Insight 1

A small group of premium customers contributes significantly to overall sales.

Insight 2

Many high-income customers are not actively spending.

Insight 3

Some low-income customers show strong purchasing interest.

Insight 4

Targeted marketing can improve conversion rates and customer satisfaction.

Insight 5

Customer behavior varies more by spending habits than demographics.

💼 Business Recommendations
Marketing Team
Create segment-specific campaigns.
Personalize customer communication.
Sales Team
Focus on premium customer retention.
Increase engagement among inactive customers.
Management
Allocate resources based on customer value.
Develop customer loyalty programs.
📊 Results

Successfully completed:

✅ Data Collection

✅ Data Cleaning

✅ Exploratory Data Analysis

✅ Descriptive Statistics

✅ K-Means Clustering

✅ Customer Segmentation

✅ Data Visualization

✅ Business Recommendations

📚 Skills Demonstrated
Data Analysis
Data Cleaning
Exploratory Data Analysis (EDA)
Machine Learning
K-Means Clustering
Customer Analytics
Data Visualization
Business Intelligence
Python Programming
🚀 Future Scope
RFM Analysis (Recency, Frequency, Monetary)
Customer Lifetime Value Prediction
Advanced Clustering Techniques
Tableau Dashboard Development
Real-Time Customer Segmentation
🏁 Conclusion

This project successfully applied Customer Segmentation Analysis using K-Means Clustering to identify different customer groups based on income and spending behavior. The insights obtained can help businesses create targeted marketing campaigns, improve customer retention, and maximize revenue through data-driven decision-making.

⭐ If you found this project helpful, consider giving this repository a star and connecting with me on LinkedIn!
