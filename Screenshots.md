# 🌍 Nairobi Cost of Living Dashboard (2019–2024): Area Level Expense Trends and Budget Insights
# Data Cleaning and DAX Measures Documentation

![Power BI](https://img.shields.io/badge/PowerBI-DAX-yellow?logo=powerbi)
![Data Analytics](https://img.shields.io/badge/Data-Analytics-blue)
![Status](https://img.shields.io/badge/Project-Active-success)
![License](https://img.shields.io/badge/License-MIT-green)

> By:
> Kyeremateng Martin
> 
## Overview

This document provides comprehensive documentation for all cleaning and DAX measures developed in the **Advanced PowerBI for Nairobi Living Expenses** project. Measures are designed to answer key business questions, support the executive dashboard, and ensure robust time intelligence. All measures follow a consistent naming convention for clarity and maintainability.


# Data Cleaning and Manipulation

## Data source: [Google](https://www.kaggle.com/datasets/yacooti/cost-of-living-in-nairobi)
<img width="975" height="428" alt="image" src="https://github.com/user-attachments/assets/3975a003-4f6d-44b1-98b1-934caa1fd15e" />

## Raw data:
<img width="1061" height="578" alt="image" src="https://github.com/user-attachments/assets/a396853f-6db8-4248-ad00-0475dea441d8" />

## BI view before cleaning:
<img width="975" height="509" alt="image" src="https://github.com/user-attachments/assets/712fb3ab-940f-453d-af0b-627b4df2924e" />

## After Cleaning:
<img width="941" height="675" alt="image" src="https://github.com/user-attachments/assets/50dc98e1-c38b-410b-bf41-7aae4a8b6590" />

## Applied steps in cleaning and transformation
<img width="533" height="612" alt="image" src="https://github.com/user-attachments/assets/1f5ca453-5dd1-4c3c-a6ec-5bb3fd1eafe3" />

## Model View:
<img width="975" height="811" alt="image" src="https://github.com/user-attachments/assets/547c2a67-ca58-48ae-aae2-4fb0fc1a49f3" />

## Relationships:
<img width="688" height="507" alt="image" src="https://github.com/user-attachments/assets/dbee2568-c8da-4a6c-b07d-9a711db1489c" />

# DAX Development Documentation (Measures and Calculated Columns)
  ## Total Spend
<img width="738" height="61" alt="image" src="https://github.com/user-attachments/assets/d6e2f010-0603-4a09-906d-729c13853dd1" />
 Similar to Total_Expenses, this measure sums the total spending but is likely filtered to a specific context (e.g., per area or per month). I created it as a base SUM measure for high level reporting\
 
## YTD Expenses
<img width="722" height="167" alt="image" src="https://github.com/user-attachments/assets/f8a307ef-e215-429d-b345-fbdcc7e39b7f" />
  This calculates the cumulative total of expenses from the start of the year up to the selected date. I achieved it using a standard year to date time intelligence function, referencing my dimDate table.
 
## Daily Avg
<img width="878" height="72" alt="image" src="https://github.com/user-attachments/assets/a5cce8b1-d98c-428f-a8f1-bfd8dfc5ec20" />
 This measure gives the average daily expense within a selected month or period. I computed it by dividing the total expense for the period by the number of days in that period, using the date table to get the day count.
 
## Monthly Avg
<img width="667" height="98" alt="image" src="https://github.com/user-attachments/assets/8b9d0ef3-d5a1-4c44-b10a-5660fcccd695" />
 This shows the average monthly expense across the filtered time range. I created it by summing total expenses and dividing by the number of distinct months in the current filter context.
 
## MoM Change
<img width="975" height="319" alt="image" src="https://github.com/user-attachments/assets/ebb50bdd-bc48-48d0-a866-9e1c4b97a52c" />
 This measures the percentage change in total expense from the previous month to the current month. I achieved it by calculating the current month’s total, retrieving the previous month’s total using a time shift function, and then computing the difference divided by the previous month.
 
## Budget Variance
<img width="966" height="64" alt="image" src="https://github.com/user-attachments/assets/15f7c41c-3bc1-4b67-9907-7cbaff9169ea" />
 This shows the difference between actual total expense and the budgeted target. I created it by joining the fact table to my dimBudget table on ExpenseType, then subtracting the sum of MonthlyBudget from the actual expense.
 
## Category Contribution %
<img width="881" height="197" alt="image" src="https://github.com/user-attachments/assets/72d3eac0-9fde-477d-9a68-b4c1ef747672" />
 This measure calculates how much each expense category (Rent, Food, etc.) contributes as a percentage of total spending. I achieved it by dividing the category total by the overall total while removing the category filter for the denominator.
 
## Food Ratio %
<img width="975" height="49" alt="image" src="https://github.com/user-attachments/assets/62538359-9e32-4874-9108-6de77650fe89" />
 This is a specific percentage showing Food cost as a proportion of total expense for a given area or month. I created it by summing Food expenses only and dividing by total expenses, then formatting as a percentage.
 
## Expense Count
<img width="630" height="77" alt="image" src="https://github.com/user-attachments/assets/d498d931-7264-485b-8e80-5907040bb6b7" />
 This counts the number of individual expense records (rows) in the fact table. I achieved it using a simple count or distinct count function on a key column.
 
## Area Rank
<img width="580" height="163" alt="image" src="https://github.com/user-attachments/assets/9743e991-e488-4a4d-952c-9be2a74c1f31" />
 This measure ranks each residential area based on total expense, from highest to lowest. I used a ranking function that iterates over all areas and assigns a dense rank.

## Inflation Rate
<img width="975" height="48" alt="image" src="https://github.com/user-attachments/assets/2eb9a16f-46c0-45e1-980e-01eb23486212" />
 This calculates the year over year percentage increase in total expense. I achieved it by comparing total expense for the selected period to the same period in the previous year, using time intelligence to shift the date context.
 
Projected Spend
This is a forward looking estimate of future expenses. I created it using a forecasting or linear regression calculation, based on historical monthly averages.
  
