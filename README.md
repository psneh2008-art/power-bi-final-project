https://app.powerbi.com/groups/me/reports/5329a51d-ca7b-43cd-89a4-361dff765e2e/0bbf51dedc676e7971c1?experience=power-bi    


# 📊 Power BI Final Project

## 📌 Project Overview
This Power BI project analyzes sales performance data and provides interactive dashboards 
to visualize key business insights such as Total Sales, Profit, Quantity, and Returns.

The project follows a Star Schema data model with fact and dimension tables.

---

## 🗂 Dataset Structure

### 🔹 Fact Tables
- **Sales_Fact**  
  Contains transactional sales data including:
  - SaleID
  - CustomerID
  - ProductID
  - DateID
  - UnitsSold
  - TotalAmount
  - Profit Category (Calculated Column)

- **Returns_Fact**  
  Contains return transaction data.

### 🔹 Dimension Tables
- **Customer_Dim** – Customer details  
- **Product_Dim** – Product information  
- **Date_Dim** – Date hierarchy  
- **Region_Dim** – Region and manager details  

---

## 🧮 Data Modeling
- Established relationships between fact and dimension tables.
- Implemented one-to-many relationships.
- Used proper primary and foreign keys.
- Followed Star Schema model for better performance.

---

## 📐 DAX Calculations

### 🔹 Calculated Column
```
Profit Category = 
SWITCH(
    TRUE(),
    Sales_Fact[TotalAmount] < 500, "Low",
    Sales_Fact[TotalAmount] < 1000, "Medium",
    "High"
)
```

### 🔹 Measures Created
- Total Sales
- Total Profit
- Total Quantity
- Total Returns
- Sales YTD
- Total Sales YoY%

---

## 📊 Dashboard Features

### 🔹 KPI Cards
- Total Sales
- Total Profit
- Total Quantity
- Total Returns

### 🔹 Visualizations
- Donut Chart (Sales by Category)
- Bar Chart (Sales by Region)
- Bar Chart (Quantity by Region)
- Line Chart (Sales by Month)
- Gauge Chart (Sales vs Target/YTD)
- Table (Year-wise and Product-wise summary)

### 🔹 Slicers
- Category
- Region
- Segment
- Year

---

## 📈 Key Insights
- South region generates highest sales.
- Technology and Furniture categories contribute major revenue share.
- Sales show strong growth in Q4 months.
- High-value transactions are categorized using Profit Category logic.

---

## 🛠 Tools Used
- Microsoft Power BI Desktop
- Power Query Editor
- DAX (Data Analysis Expressions)

---

## 🚀 How to Use
1. Open the `.pbix` file in Power BI Desktop.
2. Explore dashboard using slicers.
3. Interact with visuals to analyze trends.
4. Modify measures or visuals as needed.

---

## 👤 Author
Sneha Patel  
Power BI Final Project  
2026

---

⭐ This project demonstrates data cleaning, modeling, DAX calculations, and interactive dashboard development using Power BI.



