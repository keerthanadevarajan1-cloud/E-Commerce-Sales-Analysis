# E-Commerce-Sales-Analysis
Developed an interactive Power BI dashboard integrating DAX calculations, KPIs, and multiple visualizations to provide comprehensive business insights into sales performance, profitability, targets, and regional analysis.

## 📌 Project Overview

This project demonstrates the use of **DAX calculations** and **interactive data visualizations** in Microsoft Power BI to analyze sales performance, profitability, targets, and regional trends.
The dashboard provides meaningful business insights through calculated columns, measures, and visual reports.

---

# 📂 Project Objectives

* Perform business analysis using DAX functions
* Create calculated columns and measures
* Build interactive dashboards and visualizations
* Analyze sales, profit, quantity, and targets
* Understand geographic and category-wise performance

---

# 🛠️ Tools & Technologies Used

* Microsoft Power BI
* DAX (Data Analysis Expressions)
* Data Visualization Techniques
* Business Intelligence Concepts

---

# 📊 Calculated Columns

## 1️⃣ Category Type

Combined the **Category** and **Sub-Category** columns into a single column for improved product classification and analysis.

### Example

```DAX
Category Type = Orders[Category] & " - " & Orders[Sub-Category]
```

---

## 2️⃣ Revenue per Order

Calculated total revenue generated for each order.

### Formula

```DAX
Revenue = Orders[Amount] * Orders[Quantity]
```

---

## 3️⃣ Sales Category

Categorized sales records as **Above Average** or **Below Average** based on sales amount.

### Formula

```DAX
Sales Category =
IF(
    Orders[Amount] > AVERAGE(Orders[Amount]),
    "Above Average",
    "Below Average"
)
```

---

# 📈 Calculated Measures

## 1️⃣ Total Order Count

Calculated the total number of orders placed.

```DAX
Order Count = COUNT(Orders[Order ID])
```

---

## 2️⃣ Average Profit in Delhi

Calculated the average profit for orders placed in Delhi.

```DAX
Avg Profit Delhi =
CALCULATE(
    AVERAGE(Orders[Profit]),
    Orders[City] = "Delhi"
)
```

---

## 3️⃣ Year-To-Date (YTD) Sales

Calculated cumulative sales over time.

```DAX
YTD Sales =
TOTALYTD(
    SUM(Orders[Amount]),
    Orders[Order Date]
)
```
---

### Insights

* Compared order volume across states
* Identified top-performing states

---

The final dashboard integrates:

* DAX calculations
* KPI cards
* Interactive charts
* Geographic analysis
* Sales target tracking
* Business performance insights

---

# 📖 Key Learnings

* Understanding DAX formulas and calculations
* Building interactive business dashboards
* Data storytelling through visualization
* KPI and sales performance analysis
* Business intelligence reporting

---

# 📌 Conclusion

This project successfully demonstrates the application of **DAX calculations** and **Power BI visualizations** to analyze sales performance, targets, profitability, and regional trends.
The dashboard provides meaningful business insights that support data-driven decision-making.
