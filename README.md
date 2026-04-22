# 📊 Blinkit Sales Performance Dashboard (Power BI)

## 🚀 Overview

This project presents an **interactive Power BI dashboard** built to analyze sales performance for Blinkit (India’s last-minute delivery app).
The dashboard provides insights into **revenue trends, category performance, delivery efficiency, and customer behavior**, enabling data-driven decision-making.

---

## 🎯 Objectives

* Analyze overall revenue performance and growth trends
* Track **Month-over-Month (MoM) growth** to evaluate business momentum
* Identify top-performing product categories and packaging types
* Monitor operational efficiency using delivery metrics
* Understand the split between organic and non-organic sales

---

## 📌 Key Features

* 📈 **Revenue Trend Analysis**
  Visualizes monthly revenue performance to identify peaks and dips

* 📊 **MoM Growth Indicator**
  Displays growth percentage with directional arrows (▲/▼) and conditional formatting

* 🏆 **Category-wise Revenue Breakdown**
  Highlights top contributing product categories

* 📦 **Packaging Type Contribution**
  Analyzes revenue distribution across packaging formats

* 🚚 **Delivery Performance Metrics**
  Tracks on-time vs delayed deliveries

* 🔍 **Interactive Filters**
  Allows filtering by:

  * City/Location
  * Category
  * Offer Type

* 💡 **Business Insight Layer**
  Includes contextual insights such as:

  > “Revenue peaked in Jul 2024 and declined in early 2025 before stabilizing.”

---

## 🛠️ Tools & Technologies

* **Power BI** – Data visualization & dashboard design
* **DAX (Data Analysis Expressions)** – Measures & calculations
* **Data Modeling** – Relationships and transformations

---

## 🧠 Key DAX Measures

### Revenue(Lakh)

```DAX
Revenue (Lakh) = 
FORMAT(
    DIVIDE(SUM('blinkit_dataset'[final_price]), 100000),
    "₹0.0"
) & "L"
```

### MoM Growth %

```DAX
MoM Growth % =
DIVIDE(
    [Revenue] - CALCULATE([Revenue], DATEADD('Date'[Date], -1, MONTH)),
    CALCULATE([Revenue], DATEADD('Date'[Date], -1, MONTH))
)
```

### MoM Display (Arrow Indicator)

```DAX
MoM Display =
IF([MoM Growth %] > 0, "▲ ", "▼ ") &
FORMAT([MoM Growth %], "0.00%")
```

---

## 📊 Dashboard Highlights

* Clean and consistent **monochrome (yellow) theme** inspired by Blinkit branding
* KPI cards for quick performance overview
* Interactive visuals for deeper analysis
* Conditional formatting for intuitive insights

---

## 📈 Insights Derived

* Revenue showed peak performance around **mid-2024**
* A noticeable decline occurred in early 2025, followed by stabilization
* **Household and Personal Care categories** contributed the highest revenue
* Majority of deliveries were completed **on-time (~80%)**
* Non-organic sales dominated the revenue share

---

## 🎯 Business Impact

This dashboard helps stakeholders:

* Monitor short-term growth trends
* Identify high-performing categories
* Improve delivery efficiency
* Optimize marketing strategies

---

## 📷 Dashboard Preview

*(Add your screenshot here)*

---

## 📌 Future Enhancements

* Add **Year-over-Year (YoY) comparison**
* Implement **drill-through analysis** for detailed insights
* Create **dynamic insight generation using DAX**
* Add **reset button and navigation bookmarks**

---

## 🙌 Conclusion

This project demonstrates strong capabilities in:

* Data visualization
* Business analysis
* DAX-based calculations
* Dashboard storytelling

It reflects practical skills required for a **Data Analyst role**.

---
