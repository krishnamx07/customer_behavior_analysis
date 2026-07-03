# Customer Shopping Behavior Analysis

> An end-to-end Data Analytics project demonstrating a real-world analytics workflow using Python, SQL, and Power BI.

![Project Workflow](customer-analysis-workflow.png)

---

# Project Overview

This project analyzes customer shopping behavior using transactional retail data to uncover customer trends, purchasing patterns, and business insights.

Unlike many portfolio projects that directly connect a CSV file to Power BI, this project follows a workflow similar to what data analysts use in real organizations.

The pipeline starts with raw CSV data, performs data cleaning and exploratory analysis in Python, stores the cleaned dataset inside a SQL database, performs business analysis using SQL queries, and finally connects Power BI directly to the database for interactive reporting.

The project also includes a business report and presentation summarizing the findings.

---

# Why This Project?

Most beginner projects follow:

CSV → Power BI

Real companies usually follow something closer to:

CSV/Data Source
↓
Python (Cleaning & Validation)
↓
SQL Database
↓
Business SQL Queries
↓
Power BI Dashboard
↓
Reports & Business Presentation

This project follows that complete analytics pipeline.

---

# Real-World Analytics Workflow

The project was completed using the same sequence commonly followed by Data Analysts in organizations.

1. Raw customer dataset received as a CSV file.
2. Import the dataset into Python.
3. Perform Exploratory Data Analysis (EDA).
4. Clean missing values and inconsistent data.
5. Create new features where required.
6. Export the cleaned dataset into a SQL database.
7. Perform business analysis using SQL queries.
8. Connect Power BI directly to the SQL database.
9. Build an interactive dashboard.
10. Generate a business report.
11. Create a presentation summarizing insights.
12. Upload the complete project to GitHub.

---

# Project Architecture

```text
CSV Dataset
      │
      ▼
Python
(Data Cleaning + EDA)
      │
      ▼
SQL Database
(PostgreSQL / MySQL / SQL Server)
      │
      ▼
Business Analysis using SQL
      │
      ▼
Power BI Dashboard
      │
      ▼
Business Report
      │
      ▼
Presentation (Gamma)
      │
      ▼
GitHub Repository
```

---

# Dataset

The dataset contains customer shopping transactions including:

- Customer Information
- Product Category
- Purchase Amount
- Subscription Status
- Shipping Type
- Discounts
- Ratings
- Purchase Frequency
- Demographical Information

---

# Technologies Used

| Tool | Purpose |
|------|----------|
| Python | Data Cleaning & EDA |
| Pandas | Data Manipulation |
| Matplotlib | Visualization |
| Seaborn | Visualization |
| SQL | Business Analysis |
| PostgreSQL / MySQL / SQL Server | Data Storage |
| Power BI | Dashboard |
| Gamma | Presentation |
| GitHub | Version Control |

---

# Project Steps

## 1. Data Collection

- Import CSV dataset
- Inspect data
- Understand columns

---

## 2. Data Cleaning

- Handle missing values
- Remove duplicates
- Standardize column names
- Correct data types
- Create additional features

---

## 3. Exploratory Data Analysis

Examples:

- Customer Distribution
- Revenue Analysis
- Product Categories
- Gender Analysis
- Subscription Analysis
- Purchase Behaviour
- Correlation Analysis

---

## 4. SQL Analysis

Load the cleaned dataset into SQL.

Perform business queries such as:

- Revenue by Category
- Customer Segmentation
- Top Products
- Repeat Customers
- Subscription Analysis
- Shipping Analysis
- Revenue by Age Group
- Product Performance

---

## 5. Power BI Dashboard

Power BI connects directly to the SQL database instead of the CSV file.

Dashboard contains:

- KPI Cards
- Revenue Analysis
- Customer Analysis
- Product Performance
- Age Group Analysis
- Subscription Analysis
- Interactive Filters

---

# Business Insights

The analysis provides insights into:

- Customer purchasing patterns
- High-value customers
- Best-selling products
- Revenue contribution
- Subscription behaviour
- Customer demographics
- Product performance

---

# Project Deliverables

- Python Notebook
- SQL Scripts
- Cleaned Dataset
- Power BI Dashboard
- Business Report
- Presentation
- GitHub Repository

---

# Repository Structure

```
Customer-Shopping-Behavior-Analysis/
│
├── Dataset/
│
├── Python/
│   └── Customer_Shopping_Behavior_Analysis.ipynb
│
├── SQL/
│   └── customer_shopping_behavior.sql
│
├── PowerBI/
│   └── Dashboard.pbix
│
├── Report/
│   └── Customer Shopping Behavior Analysis.pdf
│
├── Presentation/
│
├── Images/
│   └── customer-analysis-workflow.png
│
└── README.md
```

---

# How to Run

### Step 1

Clone the repository.

```bash
git clone <repository-url>
```

### Step 2

Open the Jupyter Notebook.

Run all cells to clean and analyze the dataset.

### Step 3

Execute the SQL script to create and populate the database.

### Step 4

Open the Power BI dashboard.

Refresh the connection to retrieve data directly from the SQL database.

### Step 5

Review the business report and presentation.

---

# Key Learning Outcomes

- Data Cleaning
- Exploratory Data Analysis
- SQL Query Writing
- Database Integration
- Power BI Development
- Business Reporting
- End-to-End Analytics Workflow
- GitHub Project Documentation

---

# Future Improvements

- Automated ETL Pipeline
- Scheduled Database Refresh
- Real-Time Data Integration
- Cloud Database Deployment
- Power BI Service Deployment
- Data Validation Pipeline

---


