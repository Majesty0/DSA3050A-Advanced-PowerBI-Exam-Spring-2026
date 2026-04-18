
Total Spend
Similar to Total_Expenses, this measure sums the total spending but is likely filtered to a specific context (e.g., per area or per month). I created it as a base SUM measure for high level reporting
 
YTD Expenses
This calculates the cumulative total of expenses from the start of the year up to the selected date. I achieved it using a standard year to date time intelligence function, referencing my dimDate table.
 
Daily Avg
This measure gives the average daily expense within a selected month or period. I computed it by dividing the total expense for the period by the number of days in that period, using the date table to get the day count.
 
Monthly Avg
This shows the average monthly expense across the filtered time range. I created it by summing total expenses and dividing by the number of distinct months in the current filter context.
 
MoM Change
This measures the percentage change in total expense from the previous month to the current month. I achieved it by calculating the current month’s total, retrieving the previous month’s total using a time shift function, and then computing the difference divided by the previous month.
 
Budget Variance
This shows the difference between actual total expense and the budgeted target. I created it by joining the fact table to my dimBudget table on ExpenseType, then subtracting the sum of MonthlyBudget from the actual expense.
 
Category Contribution %
This measure calculates how much each expense category (Rent, Food, etc.) contributes as a percentage of total spending. I achieved it by dividing the category total by the overall total while removing the category filter for the denominator.
 
Food Ratio %
This is a specific percentage showing Food cost as a proportion of total expense for a given area or month. I created it by summing Food expenses only and dividing by total expenses, then formatting as a percentage.
 
Expense Count
This counts the number of individual expense records (rows) in the fact table. I achieved it using a simple count or distinct count function on a key column.
 
Area Rank
This measure ranks each residential area based on total expense, from highest to lowest. I used a ranking function that iterates over all areas and assigns a dense rank.
 
Inflation Rate
This calculates the year over year percentage increase in total expense. I achieved it by comparing total expense for the selected period to the same period in the previous year, using time intelligence to shift the date context.
 
Projected Spend
This is a forward looking estimate of future expenses. I created it using a forecasting or linear regression calculation, based on historical monthly averages.
  
