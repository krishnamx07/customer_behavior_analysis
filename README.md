# Customer Shopping Behavior Analysis

> An end-to-end Data Analytics project demonstrating a real-world analytics workflow using Python, SQL, and Power BI.

![Project Workflow](customer-analysis-workflow.png)

---

## Project Overview

This project analyzes customer shopping behavior using a public retail transactions dataset (3,900 rows) to uncover customer trends, purchasing patterns, and business insights.

Rather than connecting a CSV directly to Power BI, this project follows a workflow closer to what data analysts use in real organizations: raw CSV → Python cleaning/EDA → SQL database → business analysis via SQL → Power BI connected directly to the database for interactive reporting, with a supporting business report.

**Note on the dataset:** this is a well-known public Kaggle retail dataset, used here to practice and demonstrate the full analytics pipeline end-to-end — not a proprietary or client dataset.

---

## Why This Project?

Most beginner projects follow:

CSV → Power BI

Real companies usually follow something closer to:

```
CSV/Data Source
      │
      ▼
Python (Cleaning & Validation)
      │
      ▼
SQL Database
      │
      ▼
Business SQL Queries
      │
      ▼
Power BI Dashboard
      │
      ▼
Report & Presentation
```

This project follows that complete pipeline instead of the shortcut version.

---

## Real-World Analytics Workflow

1. Raw customer dataset received as a CSV file.
2. Import the dataset into Python.
3. Perform Exploratory Data Analysis (EDA).
4. Clean missing values and inconsistent data.
5. Create new features (age_group, purchase_frequency_days).
6. Export the cleaned dataset into a SQL database.
7. Perform business analysis using SQL queries.
8. Connect Power BI directly to the SQL database.
9. Build an interactive dashboard.
10. Generate a business report.
11. Upload the complete project to GitHub.

---

## Dataset

The dataset contains customer shopping transactions including:

- Customer demographics (Age, Gender, Location, Subscription Status)
- Purchase details (Item Purchased, Category, Purchase Amount, Season, Size, Color)
- Shopping behavior (Discount Applied, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type)

37 missing values in Review Rating were imputed using the median rating per product category.

---

## Technologies Used

| Tool                            | Purpose             |
| -------------------------------- | -------------------- |
| Python (pandas)                  | Data Cleaning & EDA  |
| Matplotlib / Seaborn             | Visualization        |
| SQL (PostgreSQL)                 | Business Analysis    |
| Power BI                         | Dashboard            |
| GitHub                           | Version Control      |

---

## Key Business Insights

These are the findings that actually came out of the SQL analysis — not generic BI-tool boilerplate:

1. **Male customers generate ~2.1x the revenue of female customers** ($157,890 vs $75,191) — driven by transaction volume in this dataset, not higher average order value. Worth segmenting further before acting on it.

2. **Subscribers do not spend more than non-subscribers.** Average spend is nearly identical ($59.49 subscribers vs $59.87 non-subscribers), and non-subscribers generate ~2.7x more total revenue simply because there are more of them (2,847 vs 1,053). The common assumption that "subscribers are higher-value customers" is **not supported** by this data — subscription status tracks engagement, not spend.

3. **83% of the customer base falls into the "Loyal" segment** (3,116 of 3,900, defined as >10 previous purchases), with only 83 customers classified as "New." This is a mature, repeat-purchase-heavy customer base rather than one driven by new acquisition — retention economics matter more here than acquisition funnels.

4. **Discount usage is uneven across products**, ranging from ~50% of purchases (Hat) down to ~47% (Pants) for the top 5 most discount-dependent items — worth checking whether these categories have structurally thinner margins or whether discounting has just become the default sales lever for them.

5. **Repeat buyers (>5 previous purchases) skew heavily toward non-subscribers** (2,518 vs 958), reinforcing insight #2 — the subscription program isn't currently capturing the company's most loyal customers.

---

## Business Recommendations

- **Re-evaluate the subscription program's value proposition** — it isn't currently correlating with higher spend or capturing the most loyal customers, so the perk structure likely needs to change before further promotion makes sense.
- **Investigate the gender revenue gap** — determine whether it's driven by category mix, transaction volume, or marketing reach before assuming it reflects purchasing power.
- **Build a retention strategy for the Loyal segment**, since it's already 83% of the base — small improvements in this group's spend or frequency have outsized revenue impact compared to acquisition efforts.
- **Audit discount dependency** on the top 5 highest-discount-rate products to check margin impact.
- **Highlight top-rated products** (Gloves, Sandals, Boots, Hat, Skirt) in marketing, since review rating didn't strongly track with revenue in this dataset — an opportunity to cross-sell quality against volume.

---

## Repository Structure

```
customer_behavior_analysis/
│
├── customer_shopping_behavior.csv
├── Customer_Shopping_Behavior_Analysis.ipynb
├── customer_shopping_behavior.sql
├── customer_shopping_behavior.pbit
├── Customer Shopping Behavior Analysis.pdf
├── Problem Statement.pdf
├── customer-analysis-workflow.png
└── README.md
```

---

## How to Run

1. Clone the repository.
2. Open and run `Customer_Shopping_Behavior_Analysis.ipynb` to clean and explore the dataset.
3. Execute `customer_shopping_behavior.sql` against a PostgreSQL database populated with the cleaned data.
4. Open `customer_shopping_behavior.pbit` in Power BI and refresh the connection.
5. Review the business report (`Customer Shopping Behavior Analysis.pdf`).

---

## Key Learning Outcomes

- Data Cleaning & Feature Engineering
- Exploratory Data Analysis
- SQL Query Writing (CTEs, window functions, conditional aggregation)
- Database Integration (Python → PostgreSQL)
- Power BI Development
- Translating query output into business-relevant, non-contradictory recommendations

---

## Future Improvements

- Automated ETL pipeline
- Scheduled database refresh
- Cloud database deployment
- Power BI Service deployment
- Deeper segmentation (RFM analysis) instead of single-threshold customer tiers

---

## License

MIT
