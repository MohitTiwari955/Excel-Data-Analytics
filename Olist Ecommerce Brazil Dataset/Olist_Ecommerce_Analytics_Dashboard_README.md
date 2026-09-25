# Brazilian Olist E-Commerce Analytics Dashboard

An end-to-end **Excel data analytics and business intelligence project** built using the Brazilian Olist E-Commerce dataset.

This project was created after completing **Luke Barousse's Data Analysis with Excel course** and was used to apply the concepts independently to a larger, real-world-style dataset.

## Project Overview

The goal was to turn raw e-commerce data into an interactive analytical workbook that answers three business questions:

1. **Which sellers create the most delivery and value risk?**
2. **How are sales value and net value performing over time and across product categories?**
3. **What does customer review behaviour look like across ratings, product categories, and states?**

The final workbook contains **three interactive dashboards** connected through Excel's data model.

---

## Dataset

**Dataset:** Brazilian E-Commerce Public Dataset by Olist  
**Platform:** Kaggle  
**Domain:** E-commerce / Sales Analytics

The dataset contains information covering areas such as:

- Orders
- Order items
- Sellers
- Customers
- Products
- Product categories
- Reviews
- Delivery dates
- Estimated delivery dates
- Customer locations

The workbook focuses primarily on **delivered orders** for the sales, seller-risk, and customer-review analysis.

---

## Tools & Skills Used

### Excel

- Advanced Excel formulas and functions
- PivotTables
- PivotCharts
- Slicers
- Timeline
- Conditional formatting / dashboard formatting
- Data validation
- Dashboard design

### Power Query

Used Power Query to:

- Create referenced queries
- Clean and transform raw data
- Filter delivered orders
- Group and aggregate records
- Merge related datasets
- Create calculated columns
- Prepare fact-style analytical tables
- Build cleaner dimension tables

### Power Pivot & Data Model

Used Power Pivot to:

- Build relationships between tables
- Create a reusable data model
- Separate fact and dimension-style data
- Enable PivotTables/PivotCharts to work from the model

### DAX

Created measures for metrics such as:

- GMV
- Total Orders
- Net Value After Freight
- Net Margin %
- Average Review Score
- % 5-Star Orders
- % 1-Star Orders
- Seller delivery-risk metrics

---

# Dashboard 1 — Seller Delivery Risk Monitor

### Business Question

**Which sellers are contributing the most delivery-related risk to customers and sales value?**

### Main Analysis

The dashboard identifies sellers based on:

- **GMV at Risk**
- **% GMV at Risk**
- **Average Delivery Delay**

A seller eligibility threshold was also applied so that extremely low-volume sellers did not dominate the analysis.

### Visuals

- Top 10 Sellers by GMV at Risk
- Top 10 Sellers by % GMV at Risk
- Top 10 Sellers by Average Delivery Delay
- KPI cards
- Key findings
- Suggested operational actions

### Analytical Focus

The dashboard combines **delivery performance + financial exposure**, rather than looking at delivery delay alone.

---

# Dashboard 2 — Sales & Profit Performance

### Business Question

**How is the delivered-order business performing in terms of sales value, net value and category performance?**

### KPIs

- Total Orders
- GMV / Total Sales Value
- Net Value After Freight
- Net Margin %

### Visuals

- Top 10 Product Categories by Net Value
- Monthly GMV vs Net Value After Freight
- Product Category slicer
- Customer State slicer
- Order Purchase Timeline

### Calculation Note

The workbook uses:

**Net Value After Freight = Price − Freight**

This is treated as a **net-value / profit-proxy measure**, rather than full accounting profit, because the dataset does not contain every business cost.

---

# Dashboard 3 — Customer & Review Performance

### Business Question

**How are customers rating their purchases, and how does review behaviour vary across categories and locations?**

### KPIs

- Average Review Score: **4.16**
- % 5-Star Orders: **58.84%**
- % 1-Star Orders: **9.69%**

### Visuals

- Review Score Distribution
- Top 10 Product Categories by 5-Star %
- Review Distribution by Customer State
- State-level review breakdown using a PivotTable

The review analysis uses **distinct Order ID logic** where appropriate so that repeated product/category rows do not incorrectly inflate order-level review metrics.

---

# Data Model & Analytical Approach

The project evolved from simple worksheet analysis into a more structured **fact/dimension-style model**.

Examples include:

- Fact-style sales data for delivered orders
- Fact-style review data
- Seller eligibility logic
- A separate product-category dimension used for cleaner filtering
- Relationships between fact and dimension tables
- DAX measures for reusable calculations

One important part of the project was handling the difference between **order-level analysis** and **item/category-level data**. Because an order can contain multiple products or categories, measures such as review percentages and average review scores were designed around distinct orders where required.

---

# Key Metrics

Some of the final workbook metrics include:

| Metric | Value |
|---|---:|
| Total Orders | 96,478 |
| GMV | R$ 13,221,498 |
| Net Value After Freight | R$ 11,023,222 |
| Net Margin % | 83.37% |
| Total GMV at Risk | R$ 1,073,760 |
| Overall Value Risk % | 10.37% |
| Average Review Score | 4.16 |
| 5-Star Orders | 58.84% |
| 1-Star Orders | 9.69% |

---

# What I Learned

This project helped me move from **following individual Excel lessons to building an end-to-end analytics workflow**:

**Raw Data → Power Query → Data Model → DAX → PivotTables/PivotCharts → Interactive Dashboard → Business Insights**

The biggest learning points were:

- Thinking about the correct **grain of the data**
- Using relationships instead of relying only on worksheet formulas
- Creating reusable DAX measures
- Separating fact-style data from dimensions
- Handling duplicate rows and distinct-order calculations
- Designing dashboards around business questions rather than just displaying charts
- Debugging Power Query, PivotTable and Data Model issues during development

---

# Learning Foundation

This project was built after completing **Luke Barousse's Data Analysis with Excel course**.

I used the course as the learning foundation, then applied the concepts independently to a different dataset and expanded the work into a multi-dashboard project.

**Credit:** [Luke Barousse](https://www.youtube.com/@LukeBarousse)

---

# Project Structure

The workbook contains the analytical/dashboard layers along with supporting tables and transformation outputs.

Main dashboard sheets:

- `Seller Delivery Gmv`
- `Ecommerce`
- `Review Analysis`

Supporting/model sheets include:

- `Original`
- `Dimension&Fact_sales`
- `Background for pivot`
- `Sheet5`
- Other supporting analysis/model areas

---

# Outcome

The final workbook demonstrates practical use of **Excel + Power Query + Power Pivot + DAX + Data Modeling** to build an end-to-end e-commerce analytics solution.

This is my first substantial project applying the concepts from the Luke Barousse Excel course to a larger independent dataset, and it forms part of my growing **Data Analytics / BI portfolio**.

