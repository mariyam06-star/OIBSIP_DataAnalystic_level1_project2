Customer Segmentation Analysis using K-Means Clustering
📌 Project Overview

Customer segmentation is one of the most important applications of data analytics in modern business. This project focuses on analyzing customer purchasing behavior and grouping customers into distinct segments using machine learning techniques.

The objective is to help businesses understand different customer groups, enabling them to create personalized marketing campaigns, improve customer retention, increase sales, and enhance customer satisfaction.

By applying data cleaning, exploratory data analysis (EDA), clustering algorithms, and visualization techniques, this project uncovers meaningful patterns within customer data.

🎯 Project Aim

The primary aim of this project is to perform customer segmentation analysis for an e-commerce business using customer demographic information and purchasing behavior.

The project helps answer questions such as:

Who are the most valuable customers?
Which customers require retention strategies?
Which customers are likely to become loyal buyers?
How can marketing campaigns be personalized for different customer groups?
📂 Dataset Information

The dataset contains customer-related information such as:

Feature	Description
Customer ID	Unique identifier for customers
Gender	Customer gender
Age	Customer age
Annual Income	Customer yearly income
Spending Score	Score assigned based on purchasing behavior
Purchase Frequency	Number of purchases made
Other Variables	Additional customer behavior metrics
🛠️ Technologies Used
Python
Jupyter Notebook
Pandas
NumPy
Matplotlib
Seaborn
Scikit-Learn
📋 Project Workflow
1️⃣ Data Collection

The first step involved collecting customer data containing demographic and purchasing information.

Objectives:
Understand customer behavior.
Identify variables useful for segmentation.
Prepare data for analysis.
2️⃣ Data Exploration

Exploratory Data Analysis (EDA) was performed to understand the dataset structure.

Tasks Performed:
Checked dataset dimensions.
Examined feature types.
Reviewed summary statistics.
Identified missing values.
Detected duplicate records.
Sample Code
df.info()
df.describe()
df.isnull().sum()
3️⃣ Data Cleaning

To ensure accurate results, the dataset was cleaned before analysis.

Cleaning Steps:

✅ Removed duplicate entries

✅ Handled missing values

✅ Corrected inconsistent data

✅ Verified data types

Benefits:
Improved data quality
Reduced noise
Enhanced model performance
4️⃣ Descriptive Statistical Analysis

Important business metrics were calculated to understand customer purchasing behavior.

Metrics Calculated:
Average Annual Income
Average Spending Score
Purchase Frequency
Maximum Spending Customer
Minimum Spending Customer
Example:
df['Spending Score'].mean()
5️⃣ Data Visualization

Visualizations were created to identify patterns and relationships.

Charts Used:
Customer Age Distribution
sns.histplot(df['Age'])
Annual Income Distribution
sns.histplot(df['Annual Income'])
Spending Score Distribution
sns.histplot(df['Spending Score'])
Correlation Heatmap
sns.heatmap(df.corr(), annot=True)
Insights:
Identified purchasing trends.
Understood customer demographics.
Detected feature relationships.
6️⃣ Feature Selection

Relevant features were selected for customer segmentation.

Selected Features:
Annual Income
Spending Score

These variables effectively represent purchasing power and buying behavior.

X = df[['Annual Income', 'Spending Score']]
7️⃣ Finding Optimal Number of Clusters

The Elbow Method was used to determine the best number of customer groups.

Process:
Applied K-Means for multiple cluster values.
Calculated Within Cluster Sum of Squares (WCSS).
Identified optimal cluster count.
Example Code
wcss = []

for i in range(1,11):
    kmeans = KMeans(n_clusters=i)
    kmeans.fit(X)
    wcss.append(kmeans.inertia_)
Elbow Curve

The elbow point indicates the ideal number of customer segments.

8️⃣ Customer Segmentation Using K-Means

K-Means clustering was applied to group customers with similar purchasing behaviors.

Model Training
kmeans = KMeans(n_clusters=5)
y_pred = kmeans.fit_predict(X)
Output

Customers were grouped into distinct clusters.

9️⃣ Cluster Visualization

Customer segments were visualized using scatter plots.

Example
plt.scatter(X[y_pred==0,0], X[y_pred==0,1])
plt.scatter(X[y_pred==1,0], X[y_pred==1,1])
plt.scatter(kmeans.cluster_centers_[:,0],
            kmeans.cluster_centers_[:,1],
            color='red')
Benefits
Easy interpretation of customer groups.
Visual understanding of customer behavior.
📊 Customer Segments Identified
Segment 1: High Income – High Spending

Characteristics:

Premium customers
Frequent buyers
High purchasing power

Recommendation:

VIP Membership Programs
Exclusive Offers
Loyalty Rewards
Segment 2: High Income – Low Spending

Characteristics:

Wealthy customers
Low engagement

Recommendation:

Personalized Promotions
Product Recommendations
Retargeting Campaigns
Segment 3: Low Income – High Spending

Characteristics:

Highly engaged customers
Budget-conscious buyers

Recommendation:

Discounts
Cashback Offers
Seasonal Promotions
Segment 4: Low Income – Low Spending

Characteristics:

Least active customers

Recommendation:

Awareness Campaigns
Entry-Level Products
Special Discounts
Segment 5: Moderate Income – Moderate Spending

Characteristics:

Average customers
Consistent purchasing behavior

Recommendation:

Regular Marketing Campaigns
Loyalty Programs
🔍 Key Insights
Insight 1

Customers with high spending scores generate a significant portion of revenue.

Insight 2

Not all high-income customers spend frequently.

Insight 3

Several moderate-income customers exhibit strong purchasing behavior.

Insight 4

Targeted marketing can significantly improve customer retention and sales.

💡 Business Recommendations
For Premium Customers
Provide VIP services.
Offer premium product bundles.
For Potential Customers
Use personalized email marketing.
Offer loyalty incentives.
For Low-Spending Customers
Introduce discounts and promotional campaigns.
For Customer Retention
Create customer loyalty programs.
Reward repeat purchases.
📈 Project Outcomes

This project successfully:

✔ Cleaned and prepared customer data

✔ Performed exploratory data analysis

✔ Applied K-Means clustering

✔ Identified meaningful customer segments

✔ Created insightful visualizations

✔ Generated business recommendations

✔ Improved understanding of customer behavior

🎓 Learning Objectives Achieved
Data Cleaning and Preprocessing
Exploratory Data Analysis (EDA)
Statistical Analysis
Feature Selection
K-Means Clustering
Elbow Method
Data Visualization
Business Insight Generation
Marketing Strategy Development
🚀 Future Improvements
Apply Hierarchical Clustering
Use DBSCAN for advanced segmentation
Build customer lifetime value prediction models
Develop interactive dashboards using Power BI or Tableau
Deploy the model as a web application
📌 Conclusion

Customer segmentation enables businesses to better understand their customers and make data-driven decisions. Using K-Means clustering, this project successfully identified distinct customer groups based on purchasing behavior and income levels. These insights can help organizations improve marketing effectiveness, customer engagement, and overall business performance.

⭐ If you found this project useful, don't forget to Star the repository and connect with me on LinkedIn!e
