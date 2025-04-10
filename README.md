📊 Provide Insights for Management in Consumer Goods Domain
This project is part of the Codebasics Monthly Resume Challenge #4, where I analyzed business data using SQL and present meaningful insights in a structured and engaging format.

📌 [Challenge Link] - (https://codebasics.io/challenge/codebasics-resume-project-challenge)

🔗 LinkedIn Post -

🏢 Company Overview: AtliQ Hardware
AtliQ Hardware (an imaginary company) is a leading manufacturer of computer hardware and accessories, operating across four major regions:

🌎 Global Presence:
  * North America (NA)
  * Latin America (LATAM)
  * Europe (EU)
  * Asia-Pacific (APAC)

🖥️ Core Business Divisions:
  * Networking & Storage (Routers, Switches, External Drives)
  * PCs (Laptops, Desktops, Workstations)
  * Peripherals & Accessories (Keyboards, Mice, Monitors, Headsets)


📝 Problem Statement

In this challenge, I stepped into the role of a junior data analyst for Atliq Hardware, a company facing challenges in data-driven decision-making due to a lack of actionable insights.

To overcome this, they are expanding their Data Analytics team and designed this challenge to evaluate candidates' SQL proficiency and business storytelling skills.


🎯 My Role in This Challenge:

  🔍 Analyze sales, pricing, and customer data.
  
  📊 Extract meaningful insights to support strategic decisions.
  
  🎥 Present findings in a compelling way for top-level management.
  

🎯 My Approach

Here's how I tackled this challenge step by step:

📄 Understanding Business Needs – I reviewed the 10 ad-hoc business requests that required insights.

🔍 Running SQL Queries – I used SQL to fetch relevant data from multiple tables.

📊 Creating a Management Dashboard – I transformed raw data into clear, actionable insights using PowerBI for executives.

🎥 Presenting Findings Creatively – I designed an engaging presentation, incorporating charts, visuals, and storytelling using Canva for impact.


📂 Dataset Details

Before diving into the analysis, it's essential to understand the structure of the data. Here's a breakdown:

🔹 Dimension Tables

Dimension tables contain descriptive/static data that help categorize and define the facts.


dim_date (NEW! 🗓️): I created this additional table to facilitate time-based analysis efficiently.

📅 date: Covers a range of fiscal years from 2020 to 2021.

📊 fiscal_year: Since the company's fiscal year starts in September, the data follows the fiscal years 2020 & 2021.

📆 quarter: Represents the quarter corresponding to the fiscal year.

🏛️ fy_month_num: Maps the fiscal month order (e.g., September = 1, October = 2, etc.).


dim_customer: Contains details about customers and their market presence.

🏬 customer: Name of the customer (e.g., Atliq Exclusive, Flipkart, Surface Stores).

🌍 platform: The channel used to sell products (E-Commerce or Brick & Mortar).

📦 channel: How the product reaches the end consumer (Retailers, Direct, Distributors).

🗺️ market: Country where the customer is located.

🌎 region: Broader classification (APAC, EU, NA, LATAM).

🏢 sub_zone: Sub-region within a market (India, Southeast Asia, Australia & New Zealand).


dim_product: Contains product-related information.

💻 product_code: Unique identifier for each product.

🏷️ category: Product classification (e.g., Peripherals, Accessories, Notebook, Storage, Networking).

🖥️ division: High-level classification (PC, Network & Storage, Peripherals & Accessories).

📦 variant: Differentiates product versions (Standard, Plus, Premium).


🔹 Fact Tables
Fact tables contain transactional and measurable data, such as sales, pricing, and costs.


fact_sales_monthly: Tracks monthly sales of each product.

📅 date: The month in which the sale occurred (fiscal years 2020 & 2021).
🛒 customer_code: Unique identifier for the customer who purchased the product.
📦 product_code: Unique identifier for the sold product.
📊 sold_quantity: Number of units sold.


fact_gross_price: Holds pricing data for each product.

📆 fiscal_year: The fiscal year for which the gross price is recorded.

💰 gross_price: The initial selling price of a product before any deductions.


fact_manufacturing_cost: Tracks production costs per product.

📆 cost_year: Fiscal year in which the product was manufactured.

🏭 manufacturing_cost: The total production cost incurred, including raw materials, labor, and overhead expenses.


fact_pre_invoice_deductions: Contains discounts applied before invoicing.

🛍️ customer_code: The customer receiving the discount.

📅 fiscal_year: The fiscal year for the discount.

🔻 pre_invoice_discount_pct: Percentage discount applied before invoice generation.


🔍 SQL Concepts Learned
* WHERE & ORDER BY – Used to filter records and sort data in ascending or descending order.
* DISTINCT – Applied to retrieve unique values, such as counting unique products.
* CTEs (WITH statements) – Used to modularize queries, improving readability and reusability.
* GROUP BY & Aggregations – Summarized data by categories using COUNT(), SUM(), AVG(), etc.
* JOINs (INNER, LEFT) – Merged tables to fetch relevant data across multiple datasets.
* DENSE_RANK() & PARTITION BY – Ranked products within each category while maintaining ties.
* CASE Statement – Applied conditional logic, such as formatting sales values dynamically.
* ROUND() & Formatting – Used to calculate and display percentages, sales in millions/billions.
* HAVING vs. WHERE – Applied HAVING for filtering grouped results after aggregation.
* Subqueries & Nested Queries – Used inline queries to calculate differences and trends.


🔑 Key Insights from Data Visualizations:

🌍 APAC Market Performance
* India, Bangladesh, Indonesia, and Australia are Atliq Exclusive's top APAC markets by gross sales.
* Japan and South Korea have relatively smaller contributions.


📊 Unique Product Growth (2021 vs. 2020)
* Unique products increased by 36.33%, from 245 in 2020 to 334 in 2021.
* Significant product diversification occurred, reflecting higher market demand.


🛒 Product Segments & Trends
* Notebooks and Accessories dominate in product count, followed by Peripherals.
* Networking products have the lowest count, indicating a potential gap in offerings.
* Accessories had the highest increase (34 new products), while Notebooks grew by 16 products.


💰 Manufacturing Costs: Highest & Lowest
* AQ HOME Allin1 Gen 2 (Personal Desktop) has the highest cost ($240.54).
* AQ Master Wired Mouse has the lowest cost ($0.89), showing a wide cost disparity in product categories.


🏷️ Top 5 Indian Customers by Avg. Discount (FY 2021)
* Flipkart received the highest average discount (30.83%), followed by Viveks and Ezone.
* Amazon received the lowest discount (29.33%), indicating varying pricing strategies across retailers.


📈 Monthly Gross Sales Trend (2020 vs. 2021)
* FY 2021 saw a massive growth in gross sales (224.42M vs. 79.50M in FY 2020).
* The highest sales occurred in October 2021 (32.2M).
* March 2020 had the lowest sales (767K), possibly due to the impact of COVID-19.


📦 Quarterly Sales Distribution (2020)
* Q1 had the highest total sales (33.72%), followed by Q2 (32.01%).
* Q3 had the lowest sales (9.99%), indicating a seasonal dip in demand.


📊 Total Sold Quantity Contribution
* December had the highest sold quantity (15.33%), followed by November (14.69%).
* March had the lowest sales (1.15%), which aligns with the gross sales trend.


🛍️ Gross Sales by Channel
* Retailers contributed the highest gross sales ($1219.1M), followed by Direct ($257.5M) and Distributors ($188.0M).
* Retail remains the strongest sales channel, showing the dominance of B2C sales.

🏆 Top 3 Best-Selling Products by Division (FY 2021)
* Networking & Storage (N & S): Pen Drives dominated sales, with the AQ Pen Drive 2 IN 1 leading at 701,373 units.
* Peripherals & Accessories (P & A): Gaming and Maxima Mouse were the top sellers.
* PC Division: AQ Digit and AQ Velocity had significantly lower sales than other divisions.
