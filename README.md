
# Project Title: Bhoj-Dashboard

## Table of Contents
- [Introduction](#introduction)
- [Dashboard Link](#dashboard-link)
- [Problem Statement](#problem-statement)
- [Steps Followed](#steps-followed)
- [Results](#results)
- [Snapshot of Dashboard](#snapshot-of-dashboard)
- [Conclusion](#conclusion)

# Introduction
This document outlines the creation of a Power BI dashboard for Bhoj, an online food and grocery delivery app. The dashboard provides comprehensive insights into the app's performance, including customer satisfaction and sales data, helping stakeholders identify strengths and areas for improvement.

### Dashboard Link : https://app.powerbi.com/groups/me/reports/e3435ea1-9b2d-43e0-a467-1abc4063e06f/a66d58bec03cfc5f6949?experience=power-bi

## Problem Statement

**Objective:** To provide insights into the performance of the Bhoj App, an online food and grocery delivery platform, by analyzing customer ratings and service metrics.

**Details:** This dashboard showcases the app's ability to meet customer expectations through various ratings and performance indicators. It helps identify areas where the service excels and highlights opportunities for improvement.

**Insights:** With an average rating of nearly 4, the data indicates that the app is performing well overall, reflecting positive customer satisfaction.


## Steps Followed

**Load Data into Power BI Desktop:**
- Load your dataset (Excel/CSV/Database) into Power BI Desktop.
Go to Home > Get Data > Excel Workbook > Select your dataset file.

**Open Power Query Editor and Check Column Properties:**
- Open Power Query Editor:
Go to Home > Transform Data > Power Query Editor.
- Enable Column Properties:
View > Enable "Column Distribution," "Column Quality," and "Column Profile."

**Ensure No Column Errors or Empty Values:**
-Remove rows with null or blank values:
Go to Power Query Editor > Select the column > Use the "Remove Rows" or "Replace Values" feature to handle missing or erroneous data.

**Calculate Average Sales (Ignoring Null Values):**
- Create a calculated column in Power BI:
Average Sales = 
    AVERAGEX(
        FILTER(SalesTable, NOT(ISBLANK(SalesTable[SalesAmount]))), 
        SalesTable[SalesAmount]
    )
  **Add Visualizations for Ratings:**
- Add visuals:
Go to the "Report" view, and drag data fields into the canvas.
Use the "Visualizations" pane to add visuals like:
- Pie Chart (for distribution of ratings).
- Line Chart (for trends in ratings over time).

**Add Visual Filters:**
- Add filters:
Drag any data field into the "Filters" pane and apply conditions, such as:
Ratings > 0 (Exclude null or blank values).

-- Examples of visuals:
1. **Slicer**: Drag `Region` or `Category` to the canvas and set it as a slicer.
2. **Card**: Display `Total Sales` as a single number.
3. **Pie Chart**: Use `Ratings Distribution` for the chart.
4. **Donut Chart**: Use `Category-wise Sales` for analysis.
5. **Matrix Table**: Use columns like `Region`, `Item`, and `SalesAmount` for tabular insights.



**Note:** By default, blank values were ignored while calculating averages.

## Results

Key insights derived from the data analysis include:

- **Total Sales:** 1.20M
- **Average Sales per Item:** $141
- **Number of Items Sold:** 8523
- **Average Rating:** 4
 
# Snapshot of Dashboard (Power BI Service)




![DashBoard]
![Bhoj](https://github.com/user-attachments/assets/23669df4-3965-4dfa-810c-5b8fff1735b6)

 
 
## Conclusion

The Bhoj Dashboard demonstrates the app's performance metrics effectively, helping stakeholders analyze customer satisfaction and areas for improvement. This visual representation provides actionable insights that can drive further growth and optimization of services.

