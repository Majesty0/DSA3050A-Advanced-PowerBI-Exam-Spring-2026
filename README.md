# 🏠 Nairobi Cost of Living Dashboard

[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?logo=kaggle&logoColor=fff)](#)
![Power BI](https://img.shields.io/badge/PowerBI-DAX-yellow?logo=powerbi)
![Data Analytics](https://img.shields.io/badge/Data-Analytics-blue)
![Status](https://img.shields.io/badge/Project-Active-success)
![License](https://img.shields.io/badge/License-MIT-green)
[![Google Chrome](https://img.shields.io/badge/Google%20Chrome-4285F4?logo=GoogleChrome&logoColor=white)](#)
![Nairobi](https://img.shields.io/badge/Region-Nairobi-red)

# Advanced-Power-BI-Cost-of-Living-Analysis
## Nairobi Residential Expense Intelligence | 2019–2024
> by: Kyeremateng Martin - *669217*

> [!Note]
> Power BI Dashboard Link: *To be updated when license is renewed*

## Project Overview

This project investigates the monthly cost of living across **20+ residential areas** in Nairobi, Kenya, from **2019 to 2024**. By analysing five expense categories (Rent, Food, Transport, Utilities, Misc), the dashboard reveals how area selection, time of year, and expense type drive total living costs. The primary objective is to build an end‑to‑end BI solution that supports **relocation planning**, **salary benchmarking**, and **inflation tracking**.

---

## Problem Statement

Individuals relocating to Nairobi, HR departments setting location‑based salaries, and policymakers lack a consolidated, time‑intelligent view of living expenses per area. Without this, moving from Githurai to Karen is a financial guessing game, salary offers may be unfair, and inflation trends remain invisible. The dashboard solves this by providing **interactive area‑by‑area comparisons**, **budget variance analysis**, and **what‑if relocation simulations**.

> [!Caution]
> The data reflects monthly estimates, not daily fluctuations. Seasonal spikes (e.g., December holidays) are captured, but one‑off emergency expenses may be under‑represented.

---

## Used Column Description

| **Property**          | **Value**                                            |
|-----------------------|------------------------------------------------------|
| **Name**              | Nairobi Cost of Living Time Series                   |
| **Format**            | CSV                                                  |
| **Rows**              | 60,000                                               |
| **Time span**         | January 2019 – December 2024 (6 years)               |
| **Areas covered**     | 20+ residential areas (Karen, Westlands, Githurai, Juja, Embakasi, etc.) |
| **Expense categories**| Rent, Food, Transport, Utilities, Misc (all in KES)  |
| **Source**            | Kaggle   |

**A sample of the raw data (10 columns):**

| Date       | Neighborhood                 | Price (KES) | Rent (KES) | Area       | Food (KES) | Transport (KES) | Utilities (KES) | Bedrooms | Bathrooms |
|------------|------------------------------|-------------|------------|------------|------------|-----------------|-----------------|----------|-----------|
| 1/31/2019  | General Mathenge, Westlands  | 155,000     | 90,341     | Westlands  | 25,454     | 15,634          | 6,142           | 4        | 4         |
| 1/31/2019  | Waiyaki Way, Westlands       | 150,000     | 93,902     | Westlands  | 24,808     | 17,194          | 6,803           | 2        | 2         |
| 1/31/2019  | Kilimani, Dagoretti North    | 100,000     | 78,160     | Kileleshwa | 23,302     | 13,104          | 6,454           | 3        | 4         |

---

## Tools Used

| **Tool**              | **Purpose**                                            |
|-----------------------|--------------------------------------------------------|
| Power BI Desktop      | Data transformation (Power Query), modeling, DAX, visuals |
| Microsoft Excel       | Initial data inspection                                |
| GitHub                | Version control and project documentation              |
| Markdown              | README and report formatting                           |

---

## Steps Followed (Methodology)

1. **Data Acquisition** – Loaded the CSV file into Power BI.
2. **Data Cleaning (Power Query)** – Removed unnecessary `Total` column, handled missing values (none found), standardised area names, extracted date parts (Year, Quarter, Month Name).
3. **Data Transformation** – Created conditional column `Area Tier` (Premium, Middle, Affordable, Satellite). Unpivoted expense columns to row‑level granularity.
4. **Data Modeling** – Built a star schema with one fact table (`fact_expenses`) and five dimension tables (`dimDate`, `dimArea`, `dimExpenseType`, `dimBudget`, `DimBudgetLevel`).
5. **DAX Measures** – Created 8+ measures (Total Expense, YTD, MoM Growth, Rank, Budget Variance, Inflation Rate, etc.).
6. **Dashboard Design** – Designed four interactive report pages with slicers, bookmarks, and what‑if parameters.
7. **Testing & Validation** – Verified relationships, cross‑filtering, and measure calculations against raw data.
8. **Deployment** – Published to Power BI Service and documented in this README.

---


## Dashboard Features

| **Page**                | **Features**                                                                                   |
|-------------------------|------------------------------------------------------------------------------------------------|
| **Executive Overview**  | KPI cards (Total Expense, Avg Monthly Cost, Budget Variance), monthly trend line, area tier slicer |
| **Area Deep Dive**      | Bar chart ranking areas by expense, decomposition tree (Tier → Area → Category), drill‑through to monthly history |
| **Category Analysis**   | 100% stacked column chart (category % over time), inflation line chart by category             |
| **Relocation Simulator**| Two drop‑down slicers (From Area, To Area), dynamic cards showing difference, % change, category‑by‑category comparison |
| **What‑If Parameter**    | Simulate changes in monthly budget or move between areas                                      |

> [!Tip]
> Use the **Drill‑through** on the Area Deep Dive page: right‑click any area bar to see its full monthly history.

## Page 1: Executive Summary
<img width="1346" height="795" alt="image" src="https://github.com/user-attachments/assets/59f2e1c3-c19a-4e3b-892f-41c2e3e125d1" />

## Insights for customers:
> Average monthly cost per person is 81.6K KES, well below the 150K KES goal. This suggests most Nairobi residents spend less than expected.
> The highest expense category is Rent, followed by Food and Transport. Rent dominates the total 4.91 billion KES living expense.
> Monthly total spend varies, between 37K and 250K KES – which realistic for a single person and msot likely a family or premium budget.

## Recommendation for customers:
> If you spend above 81,670 KES monthly, focus on reducing rent first. Consider moving to a lower‑tier area or downsizing.
> Use the monthly trend to plan for high‑spending months (e.g., December). Set aside savings in lower months.

## Insights for real estate developers:
> Rent is the largest component of total living expense. Tenants are highly sensitive to rent increases.
> The gap between current average (81.67K) and goal (150K) indicates an opportunity to offer mid‑range housing (e.g., 100‑120K per month) to capture upgraders.

## Recommendation for developers:
> Develop affordable‑premium units in areas like Langata or Ruaka, priced around 100‑120K KES per month. Market them as “half the cost of Karen but double the space of Githurai.”

## PART 2: Detailed Summary
<img width="1362" height="786" alt="image" src="https://github.com/user-attachments/assets/89f27e7e-615a-4e41-91ed-cf99697b6d14" />

## Insights for customers:
> Moving to Kasarani costs approximately 48,941 KES per month – significantly lower than the Nairobi average (81,670 KES).
> The key influencer for low expense level is Quarter 1‑3 (1.64x higher likelihood). This means expenses are lower in the first three quarters of the year, possibly due to reduced holiday spending.
> Daily average expenses per area range from 12.0M to 13.8M (aggregate, not per person). Kasarani’s per‑person cost is among the lowest.

## Recommendation for customers:
> If you work in or near Kasarani, relocate there immediately. Your monthly living cost will be 40% below Nairobi’s average.
> Plan major purchases or rental renewals in Q1‑Q3 when your expense level is naturally lower.

## Insights for real estate developers:
> Kasarani is a high‑demand affordable area. Tenants are price‑sensitive but will pay for reliable utilities and security.
> Daily aggregate expenses (13M+) show strong economic activity – not just residential but also commercial potential.

## Recommendation for developers:
> Invest in mixed‑use developments in Kasarani (ground floor retail, upper floors residential). The daily foot traffic and expense volume support small businesses.
> Offer 1‑2 bedroom units between 45,000‑55,000 KES to match the average monthly cost.


## PART 3: Insights & Monitoring
<img width="1353" height="781" alt="image" src="https://github.com/user-attachments/assets/4543fcd3-af75-435e-bfdf-1a7dee8e13db" />

## Insights for customers:
> Premium areas (Karen, Westlands) have total spend above 0.6bn KES, while Affordable areas (e.g., Thika, Ruiru, Ruaka) spend below 0.4bn KES.
> Within affordable tier, Thika and Ruiru show lower expense per area – excellent for budget living.
> Average monthly expense distribution shows Karen at 229,480 KES, Westlands at 155,100 KES, and Githurai/Juja much lower (not shown but inferred).

## Recommendation for customers:
> For the lowest cost, choose Thika or Ruiru (satellite towns). For a balance of affordability and proximity, choose Ruaka or South B.
> Avoid premium areas unless your salary is 3x the affordable area rate.

## Insights for real estate developers:
> The Middle tier (e.g., South B, Ruaka) has total spend between 0.4‑0.6bn – a growing segment of young professionals.
> Premium areas have saturated high‑end demand; affordable areas have volume but low margins.

## Recommendation for developers:
> Focus new projects on middle tier areas (Ruaka, South B). Price units at 70‑90K KES per month. Include co‑working spaces and gyms – amenities that attract remote workers.
> In affordable areas (Thika, Ruiru), build smaller units (studio/1BR) to keep rent under 50K KES and maximise occupancy.
---

## Key DAX Measures (8+)

| **Measure**               | **Formula / Logic**                                                                 | **Purpose**                                      |
|---------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------|
| Total Expense             |  `SUM(fact_expenses[ExpenseAmount])`                                               | Base metric for all calculations                |
| Avg Monthly Expense       | `AVERAGEX(VALUES(dimDate[Month Name]), [Total Expense])`                           | Typical monthly cost per area                    |
| Distinct Areas            | `DISTINCTCOUNT(fact_expenses[Area])`                                               | Counts areas in current filter context           |
| Category Contribution %   | `DIVIDE([Total Expense], CALCULATE([Total Expense], ALL(dimExpenseType)))`         | % of total by Rent, Food, etc.                   |
| YTD Expense               | `TOTALYTD([Total Expense], dimDate[Date])`                                         | Year‑to‑date cumulative total                    |
| MoM Growth %              | `DIVIDE([Total Expense] - CALCULATE([Total Expense], PREVIOUSMONTH(dimDate[Date])), CALCULATE([Total Expense], PREVIOUSMONTH(dimDate[Date])))` | Month‑over‑month change |
| Expense Rank by Area      | `RANKX(ALL(dimArea[Area]), [Total Expense], , DESC, Dense)`                        | Ranks areas from highest to lowest cost          |
| Budget Variance           | `[Total Expense] - SUM(dimBudget[MonthlyBudget])`                                  | Actual vs. target (positive = overspend)         |
| Inflation Rate (YoY)      | `DIVIDE([Total Expense] - CALCULATE([Total Expense], SAMEPERIODLASTYEAR(dimDate[Date])), CALCULATE([Total Expense], SAMEPERIODLASTYEAR(dimDate[Date])))` | Year‑over‑year inflation |
| Projected Spend           | Rolling average or linear regression (implementation varies)                       | Forecast for next month                          |

> [!Caution]
> `SAMEPERIODLASTYEAR` requires `dimDate` to be marked as a date table.

---

## Key Insights (5)

1. **Rent is the dominant cost driver** – Rent accounts for 60–70% of total expenses in premium areas but only 35–40% in affordable areas.
2. **Two‑tier affordability gap** – Moving from Githurai (lowest) to Karen (highest) multiplies total monthly expenses by **3.8x**.
3. **Food costs are stable across areas** – Food ranges only from 4,500 KES (Githurai) to 15,000 KES (Karen), a 3x difference vs. rent’s 7x difference.
4. **Seasonal spikes in Nov–Dec** – Daily average expenses increase by 5–7% in November and December (holiday spending).
5. **Githurai is 26x more likely to have low expenses** – Key influencers analysis shows living in Githurai increases the probability of low expense level by 26.39x; Juja by 8.05x.

---

## Challenges Encountered

| **Challenge**                                      | **Solution**                                                                                  |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------|
| **Inconsistent area tier classification**          | Created a conditional column in Power Query using a `SWITCH` statement based on area name.    |
| **Unpivoting expense columns caused row explosion**| Handled by filtering out unnecessary rows and ensuring the fact table size remained manageable (<100k rows). |
| **Time intelligence measures returning blanks**    | Marked `dimDate` as a date table and ensured continuous date range (no gaps).                 |
| **What‑If parameter for relocation required dynamic switching of area filters** | Used `SELECTEDVALUE` and `SWITCH` inside a measure to recalculate totals based on the two selected areas. |
| **Budget variance needed a separate dimension table** | Created `dimBudget` manually in Power Query with ExpenseType and MonthlyBudget columns, then related to fact table. |
| **Key influencers visual required a binary target column** | Added a calculated column `Expense_Level = IF(ExpenseAmount < 50000, "Low", "High")` to enable the visual. |

---

## Conclusion

This Power BI dashboard successfully transforms raw cost‑of‑living data into an interactive decision‑support tool for Nairobi residents, employers, and policymakers. The star schema design ensures efficient reporting, while DAX measures enable time intelligence, ranking, variance analysis, and what‑if relocation simulations.

Key findings confirm a two‑tier affordability gap driven primarily by rent, with Githurai being the most affordable area (26x higher likelihood of low expenses). Seasonal spikes in November–December and faster inflation in utilities and transport provide actionable insights for budget planning.

The dashboard meets all assignment requirements: 60,000+ rows, 3+ related tables, categorical + numerical variables, date field, 8+ DAX measures, 2 calculated columns, and a fully interactive design. Future improvements could include live inflation data integration, mobile‑optimised layouts, and predictive forecasting using machine learning.

---

## Repository Structure

Nairobi-Cost-of-Living-Dashboard/

    ├── 📄End of Semester
    ├── 📄README.md          # This file
    ├── 📄Report
    ├── 📄screenshots/
    │   └── Data Cleaning
    │   └── model_view.png
    │   └── DAX_Formula_Reference
    ├── 📄Nairobi_Cost_of_Living.pbix           # Main Power BI file
    ├── 📄nairobi_cost_of_livingcsv                   
    └──📄rent_apts.csv
     
 


---

## License & Acknowledgements

This project is licensed under the **MIT License** – see the `LICENSE` file for details.

**Acknowledgements**  
- Dataset inspired by Kenya National Bureau of Statistics (KNBS) and Numbeo Nairobi cost estimates.  
- Power BI visuals and icons from Microsoft Fabric.  
- README template adapted from open‑source BI projects.

---

**Made with ❤️ by Majesty**  
*Last updated: April 2026*

---

> [!Tip]
> To run the dashboard locally:  
> 1. Download the `.pbix` file from the `/powerbi` folder.  
> 2. Open with Power BI Desktop (October 2023 or later).  
> 3. If prompted, edit data source settings to point to your local copy of the CSV (see `/data/instructions_download.txt`).

