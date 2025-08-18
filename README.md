# Sales Data Analysis - Power BI Dashboard

## 📌 Overview
This Power BI project provides an interactive analytics solution for sales data, offering insights into order patterns, customer behavior, and revenue performance across different territories and product categories.

## 📂 Dataset
The analysis uses `Sales.xlsx` containing:
- 1,500+ sales transactions
- 25+ columns of detailed order information
- Data spanning multiple months

Key data dimensions:
- Order metadata (dates, statuses)
- Customer and territory information
- Product hierarchy (category → subcategory → product)
- Financial metrics (pricing, taxes, freight)

## 🛠️ Features

### Interactive Dashboards
- **Sales Overview**: High-level KPIs and trends
- **Geographical Analysis**: Sales by territory
- **Product Performance**: Breakdown by categories
- **Temporal Analysis**: Monthly/quarterly trends

### Key Visualizations
- Dynamic filters for date ranges and categories
- Drill-down capabilities for detailed analysis
- Tooltips with contextual information
- Export functionality for reports
- Orders by OrderDate chart
- Orders by Status chart
- Orders by Category, SubCategory, Product chart
- Orders vs. TotalDue by Territory chart

## 🔧 Technical Implementation
- **Transformations**:
  - Date hierarchy creation
  - Calculated columns for profit margins
  - Data type standardization
- **DAX Measures**:
  ```dax
   # Orders = DISTINCTCOUNT(Sales[OrderID])
   # Order Details = COUNT(Sales[OrderDetailID])
   Total Amount = SUM(Sales[LineTotal])
   Total Tax  = SUM(Sales[TaxAmt])
   Total Freight = SUM(Sales[Freight])
   Total Due = SUM(Sales[TotalDue])
