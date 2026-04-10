📱 Mobile Sales Analytics Dashboard

📌 Description

This project presents an interactive Mobile Sales Analytics Dashboard built using Power BI and DAX to analyze sales performance, customer behavior, and product trends.

The dashboard transforms raw transactional data into actionable insights, enabling businesses to optimize sales strategies, improve customer targeting, and make data-driven decisions.

🚨 Business Problem

Retail businesses often face challenges in:

   * Identifying top-performing and underperforming mobile models
   * Understanding customer purchasing behavior
   * Tracking sales trends across time and regions
   * Analyzing payment preferences and customer satisfaction

This leads to inefficient planning, missed opportunities, and suboptimal decision-making.

🎯 Project Objectives
   * Analyze overall sales performance using key KPIs
   * Identify best-selling brands and mobile models
   * Understand monthly and yearly sales trends
   * Evaluate performance across cities and payment methods
   * Provide actionable insights for business growth

🛠️ Tech Stack
   * Power BI Desktop – Dashboard development & visualization
   * Power Query – Data cleaning & transformation
   * DAX – KPI calculations & time intelligence
   * Data Modeling – Relationship building (Star Schema)

📂 Dataset Information
   * Dataset: Mobile Sales Data
   * Type: Transaction-level data
     
🔑 Key Fields
   * Transaction ID
   * Date
   * Mobile Model
   * Brand
   * Units Sold
   * Price Per Unit
   * Total Sales
   * Customer Name & Age
   * City
   * Payment Method
   * Customer Rating

📊 Key KPIs
   * 💰 Total Revenue: 769M+
   * 📦 Total Quantity Sold: 19K+
   * 🧾 Total Transactions: 4K+
   * 📈 Average Price: 40K+

🧮 Key DAX Measures

🔹 Total Revenue

Total Revenue = SUM('Mobile sales Data'[Total Sales])

🔹 Total Quantity

Total Quantity = SUM('Mobile sales Data'[Units Sold])

🔹 Total Transactions

Total Transactions = COUNT('Mobile sales Data'[Transaction ID])

🔹 Average Price

Avg Price = AVERAGE('Mobile sales Data'[Price Per Unit])

🔹 MTD Sales

MTD Sales = 
TOTALMTD(
    [Total Revenue],
    'Custom Calendar'[Date]
)

🔹 Same Period Last Year

Sales LY =
CALCULATE(
    [Total Revenue],
    SAMEPERIODLASTYEAR('Custom Calendar'[Date])
)

🔹 YoY Growth %

YoY Growth % =
DIVIDE(
    [Total Revenue] - [Sales LY],
    [Sales LY],
    0
)

📈 Dashboard Insights

🔹 Sales Performance

   * Strong overall revenue with consistent transaction volume
   * High-value purchases reflected in average price trends
     
🔹 Product Insights

   * Identified top-performing mobile models driving maximum revenue
   * Brand-wise comparison highlights leading market players
     
🔹 Time-Based Trends

   * Monthly and quarterly trends show fluctuations in sales
   * MTD and YoY analysis reveal growth patterns
     
🔹 Geographic Insights

   * Certain cities contribute significantly higher revenue
   * Regional demand variations observed
     
🔹 Payment Behavior

   * Digital payments (UPI, Cards) dominate transactions
   * Cash usage is comparatively lower
     
🔹 Customer Insights

   * Majority of ratings fall under "Good" category
   * Indicates overall positive customer satisfaction

