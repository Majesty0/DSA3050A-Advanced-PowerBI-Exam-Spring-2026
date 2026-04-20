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
> <img width="1353" height="788" alt="Screenshot 2026-04-20 044716" src="https://github.com/user-attachments/assets/5bcac4f9-e7a7-4123-936f-7c493bec14fa" />

## Recommendations for Customers (Relocating Individuals/Employees)
> If an employee or family spends above 55,000 KES monthly, we advise relocating from Karen or Kileleshwa to Kasarani, Kitengela, or Mlolongo. Potential monthly savings of 10,000‑15,000 KES are achievable. Use the year and quarter filters to identify seasonal spending peaks; plan major expenditures outside high‑cost quarters. Rent reduction should be the first priority – it is the largest single cost.

## Strategic Implications for Real Estate Developers
> The typical tenant in these areas spends approximately 50,000 KES monthly, with rent as the largest component. Therefore, affordable rent should not exceed 25,000‑30,000 KES to leave adequate room for food, transport, and utilities. The narrow spread between minimum and maximum expenses suggests that even premium subcounties are not dramatically more expensive in this filtered view. We recommend verifying whether the data excludes large family homes or high‑end luxury units.

## Board Recommendations for Developers
> In Kasarani, Kitengela, and Mlolongo: Build 1‑2 bedroom units with rent between 15,000‑22,000 KES. Keep total tenant expense under 50,000 KES.
> In Karen and Kileleshwa: Avoid ultra‑high‑end units (rent >50,000 KES). Instead, develop smaller affordable units (25,000‑30,000 KES rent) targeting young professionals who desire a premium location without premium pricing.

## PART 2: Detailed Summary
> <img width="1423" height="795" alt="image" src="https://github.com/user-attachments/assets/f9e0b6ad-b946-455d-9a2c-534918f8022e" />



## Strategic Insights – Board Level

> Rent variation is extreme: Westlands (97.8K) is **4.6 times higher** than Ruiru (21.3K). Food costs differ only 2.2 times, and miscellaneous expenses differ about 2.8 times. This confirms that rent is the primary lever for cost reduction. South B presents a balanced middle tier (rent 43.2K, food 17.0K). Githurai, though not fully displayed, shows very low figures (as low as 9.7K for some categories), reinforcing its position as a budget‑friendly option.

> The area tier visual (Affordable, Middle, Premium) and the bar chart (Area Expenses Y‑M) clearly rank areas: Karen, Kileleshwa, Langata, Westlands at the high end; Ruiru, Githurai, Donholm, Rongai at the low end. This ladder provides a clear market segmentation.

## Recommendations for Customers (Employees/Families)

> **Budget under 50,000 KES:** Choose Ruiru, Thika, or Umoja (rent 21‑28K, food 11‑14K) – sufficient room for transport and utilities.
> **Mid‑level salary (60‑80K):** South B or Donholm are optimal; total expense around 60K, closer to city centre.
> **Income above 150K:** Westlands or Karen are viable, but note that rent alone (97.8K) consumes most of a typical salary. Consider smaller units in these premium areas.

## Implications for Real Estate Developers

> The extreme rent sensitivity (4.6× gap) tells us that tenants will not tolerate high markups on non‑housing expenses – food and misc costs are relatively inelastic. The middle tier (South B, Donholm) shows healthy demand with rent around 43K – we believe this segment is under‑supplied. Premium areas (Westlands, Karen) offer high margins but a smaller tenant pool; targeting the right buyer is essential.

## Board Recommendations for Developers

> **Affordable areas (Ruiru, Thika, Umoja):** Develop 1‑2 bedroom units renting at 18,000‑25,000 KES. Prioritise reliable water and electricity – tenants in these areas value utility stability.
> **Mid‑tier areas (South B, Donholm):** Build 2‑3 bedroom units at 35,000‑45,000 KES with secure parking and fibre internet. This segment has strong, underserved demand.
> **Premium areas (Westlands, Karen):** Introduce a limited number of smaller units (1 bedroom) at 50,000‑60,000 KES rent to capture young professionals priced out of the luxury market.
> **Mixed‑use potential:** In South B and Donholm, consider ground‑floor retail (groceries, cafes) paired with residential above – this can increase revenue per square metre.

---

## PART 3: Insights & Monitoring
> Image 1: General Analysis
> <img width="1353" height="781" alt="image" src="https://github.com/user-attachments/assets/4543fcd3-af75-435e-bfdf-1a7dee8e13db" />
> Image 2: Specific analysis
> <img width="1426" height="789" alt="image" src="https://github.com/user-attachments/assets/d0d75880-a916-47d5-b97b-f77d046cd416" />

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

## Dashboard Video Demo
> https://github.com/user-attachments/assets/1507e913-75f7-445c-90ae-d3976d5da026


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

