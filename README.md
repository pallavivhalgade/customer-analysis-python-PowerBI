# 👨🏻‍💻 Customer Behavior Data Analysis

*Analyze customer spending patterns, identify trends, and generate actionable insights using Python, SQL, and Power BI.*

---


<a id="system-architecture"></a>
## 🏗️ System Architecture

This is a reproducible analytics pipeline, not a web application. The notebook cleans review ratings, standardizes column names, and creates derived fields before loading a customer table. SQL queries and the Power BI artifact explain the business questions and findings.

```mermaid
flowchart LR
    A["Customer shopping CSV"] --> B["Pandas cleaning and feature engineering"]
    B --> C["Customer table in SQL database"]
    C --> D["Customer behavior SQL queries"]
    D --> E["Power BI dashboard"]
    E --> F["Business findings and reports"]
    class A entry
    class B,D process
    class C system
    class E,F output
    classDef entry fill:#EAF2FF,stroke:#5275AD,color:#1E3556
    classDef process fill:#F0EBFA,stroke:#8870B2,color:#3B2856
    classDef system fill:#FFF2DA,stroke:#AA8440,color:#51401E
    classDef output fill:#E3F4EC,stroke:#4C8A72,color:#234C3B
    classDef pending fill:#F8E9E7,stroke:#AD706A,color:#653C37,stroke-dasharray:5 5
```

<details>
<summary><strong>Follow the implementation</strong></summary>

| Stage | Source |
| --- | --- |
| Cleaning notebook | [analysis/Customer_Shopping_Behavior_Analysis.ipynb](analysis/Customer_Shopping_Behavior_Analysis.ipynb) |
| Business queries | [analysis/customer_behavior_sql_queries.sql](analysis/customer_behavior_sql_queries.sql) |
| Dashboard artifact | [dashboard/customer_behavior_dashboard.pbix](dashboard/customer_behavior_dashboard.pbix) |
| Input dataset | [data/customer_shopping_behavior.csv](data/customer_shopping_behavior.csv) |

</details>

## Overview
Designed and executed a complete end-to-end data analytics workflow simulating a professional business environment. Leveraged transactional data from **3,900 purchases** across multiple product categories to **analyze customer behavior, identify trends, and generate strategic business insights**. Performed data cleaning in Python, structured analysis in SQL, and visualized key metrics in Power BI.

---

## Business Problem
Addressed challenges faced by organizations in improving sales, loyalty, and customer retention by:  
- **Analyzing** purchasing trends and identifying high-value customer segments  
- **Detecting** loyal customers and repeat buyers  
- **Generating** actionable insights for targeted marketing and business strategy  
- **Evaluating** product performance and discount effectiveness  

---

## Dataset Summary
- **Rows/Purchases:** 3,900  
- **Columns:** 18  
- **Key Features:** Customer demographics, purchase details (Item, Category, Amount), and shopping behavior (Discount Applied, Previous Purchases, Review Rating, Subscription Status)  
- **Missing Data:** Imputed 37 missing values in `Review Rating`  

---

## Tools & Technologies
- **Python (Pandas):** Cleaned, transformed, and engineered features  
- **SQL (PostgreSQL):** Queried structured data and extracted business insights  
- **Power BI:** Built interactive dashboards and KPIs  
- **Jupyter Notebook:** Documented EDA workflow  

---

## 🗂️ Project Structure

![Project Structure](images/structure.png)


---

## Data Cleaning & Preparation
- **Handled missing data:** Imputed `Review Rating` using median per product category  
- **Standardized columns:** Renamed columns to snake_case  
- **Engineered features:** Created `age_group` column for segmentation  
- **Validated data:** Removed redundant columns like `promo_code_used`  
- **Integrated database:** Loaded cleaned data into PostgreSQL for analysis  

---

## Exploratory Data Analysis (EDA)
- **Examined** purchase amount distribution: mean $59.76  
- **Analyzed** gender distribution: majority male customers  
- **Evaluated** review ratings: average rating 3.75  
- **Visualized** purchase patterns and customer segmentation  

---

## Research Questions & Key Findings
- **Revenue by Gender:** Male customers generated $157,890 vs. female $75,191  
- **Subscribers vs. Non-Subscribers:** Non-subscribers generated $170,436 due to volume  
- **Repeat Buyers Conversion:** Identified 2,518 loyal customers not subscribed, highlighting conversion opportunities  
- **High-Value Discount Users:** 839 customers used discounts while spending at/above average amount  
- **Top Products for Marketing:** Gloves, Sandals, Boots received highest ratings; Hats had highest discount usage  
- **Revenue by Age Group:** Young Adults contributed $62,143  

### Business Recommendations
- **Promote subscriptions:** Encourage non-subscribers to convert loyal buyers  
- **Target marketing campaigns:** Focus on Young Adult segment and premium Express Shipping users  
- **Optimize discount policies:** Review high-discount products like Hats for margin control  

---

## Dashboard
- **Developed** interactive Power BI dashboard summarizing key metrics  
- **Visualized** revenue by category, sales by age group, subscription status, and average purchase amount  
- **Tracked KPIs:** 3.9K customers, average review rating 3.75  

![Customer Behavior Dashboard](images/Screenshot%202025-11-26%20193914.png)

---

## Project Links
- 🔗 **GitHub Repository:** [https://github.com/pallavivhalgade/customer-analysis-python-PowerBI.git](https://github.com/pallavivhalgade/customer-analysis-python-PowerBI.git)  
- 📄 **Project Report PDF:** [https://drive.google.com/file/d/1TkWuLTKY4H324EpAdgpdPrcp6e-tUlvu/view?usp=sharing]  
- 💡 **Presentation Deck:** [https://drive.google.com/file/d/1GEbTJxG_ulYjsVqHtPjDNHzEgRI3DdXk/view?usp=sharing]
---

## How to Run This Project
1. **Clone the repository:**
```bash
git clone https://github.com/pallavivhalgade/customer-analysis-python-PowerBI.git
cd customer-analysis-python-PowerBI


2.Open Jupyter Notebook:
Open Customer_Shopping_Behavior_Analysis.ipynb and execute all cells to clean data and load into SQL.

3.Run SQL Queries:
Execute customer_behavior_sql_queries.sql to extract business insights.

4.Explore Dashboard:
Open customer_behavior_dashboard.pbix and connect to SQL database for interactive visualizations.

##Author & Contact


Pallavi Vholgade
Final Year AIML Student | Aspiring Data Analyst
📧 Email: pallavivhalgade@gmail.com

🔗 GitHub

---

## About the developer

Built by **Pallavi Vholgade**. Explore my AI / ML projects, experience, and skills in my [portfolio](https://pallavi-portfolio-preview.vercel.app).

[LinkedIn](https://www.linkedin.com/in/pallavi-vholgade-05565b24b) · [Email](mailto:pallavivhalgade@gmail.com)
