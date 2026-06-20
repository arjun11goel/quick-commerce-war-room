# Quick Commerce War Room: Operations & Customer Intelligence

## Executive Snapshot (3-Minute Read)

This project simulates an executive business intelligence environment for a large-scale quick commerce company. Using transaction, product, customer, and delivery data, the objective was to transform raw operational records into actionable business insights that support strategic decision-making.

The project combines Python-based data preparation with Power BI dashboarding to analyze revenue performance, customer value, product demand, reorder behavior, and operational efficiency.

## Interactive Dashboard Demo

<img width="852" height="480" alt="dashboard_demo" src="https://github.com/user-attachments/assets/390e2310-f7c5-4753-98b8-dbb3cce31823" />


The dashboard consists of four business intelligence pages:
- Executive War Room
- Customer Intelligence
- Revenue & Product Intelligence
- Operations Intelligence

### Key KPIs

| KPI                   | Value        |
| --------------------- | ------------ |
| Total Revenue         | ₹1.1 Billion |
| Total Orders          | 500K         |
| Total Customers       | 160K         |
| Average Order Value   | ₹2.19K       |
| Average Delivery Time | 20.5 Minutes |
| Repeat Customer Rate  | 66%          |

### Executive Highlights

* VIP customers represent only 14% of customers but generate 44% of total revenue.
* Peak demand occurs between 10 AM and 4 PM, creating significant operational pressure.
* Approximately 75% of deliveries are completed successfully, while 25% experience delays.
* Revenue concentration is driven by a relatively small set of departments and products.
* Several products simultaneously lead both revenue generation and reorder behavior, indicating strong customer loyalty.

---

## Dashboard Walkthrough

### Executive War Room

Focuses on top-level business performance metrics including revenue, customer growth, delivery performance, customer segmentation, and hourly demand trends.

<img width="1400" height="782" alt="Executive War Room" src="https://github.com/user-attachments/assets/a23d2f04-2259-49f9-bc1a-e6c1fadb5565" />


---

### Customer Intelligence

Analyzes customer segments, revenue contribution, customer share, repeat purchasing behavior, and customer value concentration.

<img width="1401" height="786" alt="Customer Intelligence" src="https://github.com/user-attachments/assets/71db491a-c5a6-43aa-bfc6-ddd95b5cffff" />


---

### Revenue & Product Intelligence

Evaluates department-level revenue performance, reorder patterns, product contribution, and category performance.

<img width="1402" height="787" alt="Revenue   Product Intelligence" src="https://github.com/user-attachments/assets/be56679e-a460-41e9-8be9-b2745e860750" />


---

### Operations Intelligence

Monitors delivery performance, operational bottlenecks, peak-hour pressure, delay patterns, and service-level efficiency.

<img width="1397" height="790" alt="Operations Intelligence" src="https://github.com/user-attachments/assets/dbaf1fff-25da-4b54-ad62-5b159cc5cb43" />


---

## Key Findings

### Finding 1: Revenue Is Highly Concentrated Among VIP Customers

VIP customers account for only 14% of the customer base but contribute approximately 44% of total revenue.

This indicates a highly profitable customer segment whose retention directly influences overall business performance.

---

### Finding 2: Demand Peaks During Midday Hours

Order volume and revenue both peak between 10 AM and 4 PM.

This pattern suggests that staffing, inventory allocation, and delivery capacity should be optimized around these hours to prevent service degradation.

---

### Finding 3: Customer Size Does Not Equal Customer Value

Occasional customers represent more than half of the customer population but contribute significantly less revenue compared to VIP customers.

This reveals a substantial opportunity for customer conversion and loyalty-building programs.

---

### Finding 4: Product Demand Is Unevenly Distributed

A limited number of products and departments contribute a disproportionate share of total revenue and reorder activity.

This suggests inventory prioritization opportunities and category-level optimization potential.

---

### Finding 5: Operational Delays Affect One Out of Every Four Orders

Approximately 25% of orders experience delivery delays.

Although the majority of orders are delivered successfully, improving delivery efficiency remains a major opportunity for operational improvement.

---

## Actionable Recommendations

### Short-Term (0–3 Months)

* Prioritize inventory availability for top revenue-generating products.
* Increase staffing during identified peak demand hours.
* Monitor delayed-order hotspots more aggressively.
* Launch retention campaigns targeting high-value customers.

### Medium-Term (3–12 Months)

* Develop a loyalty program designed to convert Regular customers into VIP customers.
* Introduce operational monitoring alerts for delivery bottlenecks.
* Implement demand forecasting for high-volume product categories.

### Long-Term (1–3 Years)

* Build predictive customer lifetime value models.
* Develop delivery optimization and route intelligence systems.
* Implement personalized recommendation engines for increasing reorder rates.
* Create automated executive monitoring systems for real-time decision support.

---

## Project Overview

### Business Problem

Quick commerce businesses operate in highly competitive environments where profitability depends on customer retention, operational efficiency, inventory management, and delivery performance.

Decision-makers require visibility into both strategic and operational metrics to identify growth opportunities and operational risks.

The objective of this project is to build a centralized executive intelligence platform capable of transforming raw transaction data into actionable insights.

---

## Executive Summary

### Page 1: Executive War Room

Provides a high-level overview of business performance through revenue, orders, customers, delivery performance, and demand trends.

Primary business question:

"How is the business performing overall?"

---

### Page 2: Customer Intelligence

Focuses on customer segmentation and customer value concentration.

Primary business question:

"Which customers create the most value?"

---

### Page 3: Revenue & Product Intelligence

Evaluates department and product performance.

Primary business question:

"What products and categories drive growth?"

---

### Page 4: Operations Intelligence

Focuses on delivery performance and operational efficiency.

Primary business question:

"Where are operational bottlenecks occurring?"

---

## Insights Deep Dive

### Customer Value Index Analysis

The analysis revealed that VIP customers generate revenue at a rate significantly higher than their population share.

This indicates that business growth is highly dependent on retaining and expanding this segment.



### Revenue vs Order Volume Analysis

Several departments generate disproportionately high revenue relative to order volume.

This demonstrates that volume alone should not be used to evaluate business performance.

Revenue efficiency is equally important.



### Reorder Behavior Analysis

Products with consistently high reorder counts indicate customer trust and recurring demand.

These products should receive inventory priority and forecasting attention.



### Delivery Operations Analysis

Peak-hour demand creates the largest operational burden on the delivery network.

Resource allocation should be concentrated during these periods.

---

## Key Analytical Decisions

### Star Schema Design

Data was transformed into a dimensional model using:

* Fact Orders
* Fact Delivery
* Fact Order Product

Supported by:

* Dim Customer
* Dim Product
* Dim Hub

This design improves scalability and analytical performance.

```text
quick-commerce-war-room/
│
├── data/
│   └── processed/
│       ├── dim_customer.csv
│       ├── dim_product.csv
│       ├── dim_hub.csv
│       ├── fact_orders.csv
│       ├── fact_delivery.csv
│       └── fact_order_product.csv
│
├── notebooks/
│   ├── 01_Data_Loading.ipynb
│   ├── 02_Data_Cleaning.ipynb
│   ├── 03_KPI_Analysis.ipynb
│   └── 04_Advanced_Business_Questions.ipynb
│
├── dashboard/
│   ├── Quick_Commerce_War_Room.pbix (Not Uploaded due to github file size limit)
│   └── Quick_Commerce_War_Room.pdf
│
├── screenshots/
│   ├── executive_war_room.png
│   ├── customer_intelligence.png
│   ├── revenue_product_intelligence.png
│   └── operations_intelligence.png
|   └── dashboard_demo.gif
│
│
└── README.md
```

---

### Customer Segmentation

Customers were classified into:

* VIP
* Regular
* Occasional

based on purchasing behavior and revenue contribution.

This segmentation enables targeted business analysis.

---

### Feature Engineering

Additional analytical fields were created including:

* Order Revenue
* Delivery Status
* Customer Segment
* Reorder Metrics
* Delivery Performance Indicators

---

## Data Quality Audit Summary

The raw data underwent cleaning and validation procedures before dashboard development.

### Validation Activities

* Missing value handling
* Duplicate detection
* Data type correction
* Relationship validation
* Revenue consistency checks
* Delivery metric verification

### Result

The final analytical model contained approximately 500,000 transaction records prepared for reporting and dashboarding.

---

## Tools Used

| Tool             | Purpose                             |
| ---------------- | ----------------------------------- |
| Python           | Data Processing                     |
| Pandas           | Data Cleaning & Analysis            |
| NumPy            | Numerical Operations                |
| Jupyter Notebook | Exploratory Analysis                |
| Power BI         | Dashboard Development               |
| DAX              | KPI & Measure Creation              |

---

## Assumptions and Caveats

* Customer segments were engineered for analytical purposes.
* Delivery performance indicators are based on available delivery metrics.
* Certain location attributes were synthetically distributed to support geographic analysis demonstrations.
* The project focuses on business intelligence workflows rather than production deployment.

---

## Data Source

Dataset used for educational and portfolio purposes.

Original source: https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis
Instacart Online Grocery Shopping Dataset.

The dataset was transformed and extended to simulate a quick-commerce operational environment.

---

The original project was developed using the complete analytical dataset containing 500,000+ orders and delivery records. Large fact tables and the Power BI (.pbix) file have been excluded from the repository because they exceed GitHub's recommended file size limits.

---

## Contact and Feedback

I welcome feedback, suggestions, and discussions regarding data analytics, business intelligence, Power BI, and data-driven decision-making.

### Author

Arjun Goel

MCA, VIT Vellore

LinkedIn: https://www.linkedin.com/in/arjun11goel
