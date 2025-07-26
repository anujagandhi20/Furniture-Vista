# 📊 Furniture-Vista : US Furniture Sales Executive Dashboard

## 📝 Project Overview

This repository contains a Power BI executive dashboard designed to provide insightful analytics for the **US Furniture Sales Organization**. The objective of this project is to display key performance indicators (KPIs), profit metrics, regional and customer segment trends, and comparative performance against targets.

The dashboard has been designed for desktop viewing, ensuring accessibility for decision-makers on the go.

---

## 📁 Files Included

| File Name | Description |
|-----------|-------------|
| `US_Furniture_Sales.pbix` | Power BI report containing executive dashboard and detailed report |
| `data/US_Furniture_Sales.xlsx` | Source Excel data for dashboard creation |
| `data/Regional_Sales_Plan_vs_Actual_Achievement.xlsx` | Data used for plan vs. actual performance comparison chart |
| `images/` | Screenshots of the dashboard and report pages |

---

## 📌 Dashboard Features

### 📍 Page 1: `US Furniture Sales`

#### ✅ Visual Highlights:
- **Title Card**: “US Furniture Sales”
- **KPI Cards**:
  - Total Revenue Generated (💰)
  - Profit Earned
  - Total Discount Offered
  - Total Quantity Sold
  - Number of Products Sold (Custom Measure)
- **Visualizations**:
  - **Pie Chart**: Sales by Customer Segment
  - **Bar Chart**: Sales by Sub-Category
  - **Map**: Sales by State and Region
  - **Column Chart**: Sales by Month
  - **Year Filter Buttons**: 2018–2021 using slicer

#### 🛠️ Features Implemented:
- Custom DAX measure to calculate number of distinct products
- Page Navigation enabled for smooth user experience

---

### 📍 Page 2: `Detailed Sales Report`

#### ✅ Table Visual:
- Columns: Sub-Category | Profit | Quantity | Revenue
- Conditional Formatting:
  - **Data Bars**: on Quantity
  - **Font Colors & Icons**: on Profit (positive = green/up; negative = red/down)
  - **Background Colors**: on Revenue

#### 📊 Column Chart:
- **Sum of Actual vs Target by Region** (North, South, East, West)
- Conditional formatting based on a DAX measure:
  - Green bar = Target Achieved
  - Red bar = Target Not Achieved

---

## 🔧 DAX Measures Used

### ✅ Product Count
```DAX
Product Count = DISTINCTCOUNT('YourTableName'[Product Name])
