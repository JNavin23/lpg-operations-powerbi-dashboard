# LPG Operations Dashboard — Power BI

## Overview
End-to-end Power BI project analyzing Pan-India LPG 
distribution operations across 22 states, 15 distributors, 
and 3 oil companies — IndanGas, HP Gas, and Bharat Gas — 
covering the period 2022 to 2024.

The project covers the complete analyst workflow from raw 
messy data to a professional interactive dashboard.

---

## Dataset
- 5,000 rows and 25 columns
- Moderately messy with real-world data quality issues
- Mixed date formats, nulls, duplicates, outliers and typos
- Covers bookings, deliveries, pricing, subsidies and schemes

---

## Tools and Technologies
- Power BI Desktop
- Power Query — M Language
- DAX — Data Analysis Expressions
- Microsoft Excel — CSV source data

---

## Data Cleaning (Power Query)
- Removed 165 duplicate Booking IDs
- Fixed 4 mixed date formats using Change Type with Locale
- Standardized 7 messy text category columns
- Replaced nulls across all columns with appropriate values
- Removed outlier prices — negatives, zeros and values above 3000
- Fixed negative Delivery TAT values
- Applied TRIM, PROPER and UPPER formatting on text columns

---

## Data Modelling
- Created a separate Date Table using DAX CALENDAR function
- Marked Date Table as official date table in Power BI
- Built One to Many relationship between Date Table and fact table
- Sorted Month Name by Month Number for correct visual ordering

---

## Feature Engineering
- TAT Flag — Same Day, On Time, Delayed, Very Delayed
- Price Band — Low, Medium, High, Premium
- Revenue Category — Low Value, Mid Value, High Value
- Cylinders Flag — Single, Double, Bulk
- Booking Year and Quarter columns

---

## DAX Measures 

**Basic Measures**
- Total Bookings, Total Revenue, Total Subsidy
- Total Net Payable, Avg Unit Price

**CALCULATE and FILTER**
- Delivery Success Rate %, Cancellation Rate %
- Subsidy Utilization Rate %, Avg TAT Days
- Ujjwala Scheme Revenue

**Time Intelligence**
- Revenue MTD, Revenue YTD, Revenue FYTD
- Revenue SPLY, YoY Growth %, MoM Growth %

**Ranking and Filtering**
- Distributor Revenue Rank, Region Revenue Rank
- Revenue Contribution %, Dynamic Top N Revenue
- Is Top 5 Distributor

---

## Dashboard Pages

**Page 1 — Executive Summary**
- 5 KPI Cards — Total Bookings, Total Revenue, 
  Avg Unit Price, YoY Growth %, Delivery Success Rate %
- Monthly Revenue Trend — Current vs Same Period Last Year
- Revenue by Oil Company — Donut Chart
- Slicers — Year, Region, Oil Company

**Page 2 — Operations Analysis**
- Bookings by Delivery Status — Color coded bar chart
- Top 5 Distributor Performance — Table with data bars
- Avg Delivery TAT by Cylinder Type — Column chart
- Slicers — Year, Delivery Status, Cylinder Type

---

## Files in this Repository
- LPG_Operations.csv — Raw messy source dataset
- LPG_Operations_Dashboard.pbix — Power BI project file
- LPG_Operations_Dashboard_PDF.pdf — Exported dashboard
- LPG_Dashboard_Page1_Executive_Summary.png — Screenshot
- LPG_Dashboard_Page2_Operations_Analysis.png — Screenshot

---

## Author
**Navin **

GitHub: github.com/JNavin23
