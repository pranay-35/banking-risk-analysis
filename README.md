# banking-risk-analysis
A project on banking customer risk analysis using EDA and Power BI.

# 💼 Banking Risk Analysis Project

## 🧠 Problem Statement

**Develop a basic understanding of risk analytics in banking and financial services and understand how data is used to minimise the risk of losing money while lending to customers.**

## ✅ Solution

With our dashboards, which are created using the **latest features of Power BI**, the company can make data-driven decisions. These dashboards provide valuable insights based on the applicant’s profile — for instance, whether the applicant is likely to repay the loan — and help determine if a loan should be approved or rejected. This reduces financial risk and enhances customer profiling accuracy.


## 📌 Project Overview

In the fast-evolving financial sector, it is vital for banking institutions to assess risk efficiently to reduce defaults and improve profitability. This project uses real-world banking customer data to segment income levels, evaluate financial behavior, and visually represent trends that matter.

The pipeline consists of the following stages:
1. Data preparation and cleaning using **Microsoft Excel**
2. Importing the cleaned data into a **MySQL/PostgreSQL database**
3. Querying the database using **Python in Jupyter/Google Colab**
4. Performing **exploratory data analysis (EDA)** using Python
5. Creating interactive dashboards using **Power BI**


## 🗃️ Dataset Description

The dataset used is titled `Banking.csv`, which contains anonymized information about banking customers including:
- Customer ID
- Estimated Income
- Credit Card usage
- Loan and deposit history
- Financial product adoption


## 🧹 Data Cleaning Using Excel

Before diving into the analysis, the dataset underwent a comprehensive cleaning process using **Microsoft Excel**. The key cleaning steps included:
- Removing duplicates
- Handling null values by imputation or removal
- Normalizing column names for better readability
- Converting numeric strings to proper number formats
- Validating income and loan values for outliers

This step ensured the dataset was analysis-ready and free from data integrity issues.


## 🛢️ Creating the Database and Table
Once the cleaned data was ready, a relational database named **`banking_case`** was created.
### Database: `banking_case`  
- A table named **`customer`** was created within this database to house the cleaned data.

### Table: `customer`

| Column Name        | Data Type   | Description                            |
|--------------------|-------------|----------------------------------------|
| customer_id        | INT         | Unique customer identifier             |
| estimated_income   | FLOAT       | Estimated annual income of the customer |
| has_loan           | BOOLEAN     | Indicates if customer has a loan       |
| has_deposit        | BOOLEAN     | Indicates if customer has a deposit    |
| credit_score       | INT         | Credit score of the customer           |

The dataset was then imported into this table using SQL commands or database tools like MySQL Workbench or pgAdmin.


## 🔌 Connecting to the Database via Python
The notebook was executed in **Google Colab**, allowing flexible and remote access to Python tools.
To connect the notebook to the database, the following libraries were used:

```python
import sqlalchemy
import pandas as pd


📊 Exploratory Data Analysis (EDA)
A detailed EDA was carried out using Python to uncover patterns, trends, and correlations in the data. The following types of analyses were conducted:

📌 Univariate Analysis
Distribution of income, credit scores, and loan status.
Histograms and count plots used to understand individual feature distributions.

🔗 Bivariate Analysis
Relationship between income and loan status.
Deposit trends segmented by income bands.
Credit score vs loan status visualizations.

📈 Multivariate Analysis
Heatmaps and pair plots to identify correlations.
Cluster analysis of high-income customers who also have deposits and loans.
These analyses revealed meaningful business insights, such as:
Customers with higher credit scores are more likely to be offered loans.
Mid and high-income bands exhibit greater loan uptake.
Deposit ownership positively correlates with income and creditworthiness.

📈 Interactive Dashboards in Power BI
The most visually engaging part of this project involved creating interconnected dashboards using Power BI.
The report contains five key pages, each serving a unique purpose:

1. 🏠 Home
An overview page summarizing customer counts, average income, and high-level indicators.
Contains slicers for segmenting data by income bands or loan status.

2. 🏦 Loan Analysis
Focuses on customer behavior around loans.
Visuals include:
Loan approval distribution by income band
Loan vs credit score heatmap
Pie chart showing percentage of customers with active loans

3. 💰 Deposit Analysis
Highlights patterns in deposits and savings.
Interactive visuals display:
Deposit ownership by income segment
Correlation between deposits and credit score
Deposit ratio by gender (if available in the dataset)

4. 📊 Summary
Provides an aggregated view combining loan and deposit metrics.
KPIs include:
Average loan amount
Deposit count by region
Income-to-loan ratio per segment

5. 🔍 Drill-through
Enables focused analysis on individual customer IDs or income groups.

Users can click on a data point in any report and "drill-through" for detailed insights.

🖼️ Dashboard Preview Images
Images of each dashboard page are included in the repository (/images folder) for quick reference.

🧰 Tools and Technologies
Tool	            Usage
Excel	            Data cleaning and preprocessing
MySQL       	    Database creation and data storage
Python            EDA and DB connection
Google Colab	    Notebook execution on the cloud
Power BI	        Dashboard and report generation

🧪 How to Run This Project
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/your-username/banking-risk-analysis.git
cd banking-risk-analysis

2. Launch the Jupyter Notebook (or use Colab)
Open the file notebooks/BankEDA.ipynb using:

Jupyter Notebook locally, or
Upload to Google Colab

3. Connect to Your SQL Database
Update your database connection credentials in the notebook:
python
Copy
Edit
engine = sqlalchemy.create_engine('mysql+pymysql://user:password@host/banking_case')

4. Explore the Dashboards
Open the Power BI file:
📂 dashboard/Banking Dashboard.pbix
Navigate through the different report tabs (Home, Loan Analysis, Deposit Analysis, etc.)


🚀 Future Enhancements
Incorporate a Machine Learning model to predict customer default risk
Add time-series data for trend-based predictions
Publish dashboard using Power BI Service for public sharing
Automate ETL workflow for regular updates

🙌 Acknowledgements
Thanks to open-source contributors and the creators of the tools that made this possible.
