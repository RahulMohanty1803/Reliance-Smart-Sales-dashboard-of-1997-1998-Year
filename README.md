# Reliance-Smart-Sales-dashboard-of-1997-1998-Year
To develop an interactive Reliance Smart Sales dashboard of 1997-1998 Year using Power Bi that provides real-time insights into key performance metrics and trends, enabling stakeholders to monitor and analyze the Sales and Profit effectively.

# Project Insights Sales Report of 1997-1998 Year-->


• Overall revenue is 1.76M


• Total Profit is 1.05M


• Total transaction amount is 270K


• Male customers are contributing more in revenue 891.73K, female 872.82K


• USA contributing more profit of 66.75%


• Top 3 Revenue Generate Store State are Salem, Tacoma, Seattle contributing to 25%


• Revenue increased to 112% in 1998 Year( 1997-5,65,238.13 & 1998-11,99,308.31)


# DAX queries used-


• M_All_Returns = CALCULATE([M_Total_Returns],ALL('f_Returns-1997-1998'))

• M_All_transactions = CALCULATE([M_Total_Transactions],ALL(f_Transactions))

• M_Previous_Month_Profit = CALCULATE([M_Total_Profit],PREVIOUSMONTH(d_Calendar[date]))

• M_Previous_Month_Returns = CALCULATE([M_Quantity_Returned],PREVIOUSMONTH(d_Calendar[date]))

• M_PreviousMonth_Revenue = CALCULATE([M_Total_Revenue],PREVIOUSMONTH(d_Calendar[date]))

• M_PreviousMonth_Transactons = CALCULATE([M_Total_Transactions],PREVIOUSMONTH(d_Calendar[date]))

• M_Profit_Margin = [M_Total_Profit]/[M_Total_Revenue]

• M_Quantity_Returned = SUM('f_Returns-1997-1998'[quantity])

• M_Quantity_sold = SUM(f_Transactions[quantity])

• M_Total_Cost = SUMX(f_Transactions,f_Transactions[quantity]*RELATED(d_Products[product_cost]))

• M_Total_Profit = [M_Total_Revenue] - [M_Total_Cost]

• M_Total_Returns = COUNTA('f_Returns-1997-1998'[return_date])

• M_Total_Revenue = SUMX(f_Transactions,f_Transactions[quantity]*RELATED(d_Products[product_retail_price]))

• M_Total_Transactions = COUNTA(f_Transactions[store_id])

• M_Unique_Products = DISTINCTCOUNT(d_Products[product_id])

• M_Weekend_transactions = CALCULATE([M_Total_Transactions],d_Calendar[Weekend] = "Y")

• M_YTD_Revenue = CALCULATE([M_Total_Revenue],DATESYTD(d_Calendar[date]))

• M_Previous_Year_Sales = CALCULATE([M_Total_Revenue],SAMEPERIODLASTYEAR(d_Calendar[date]))

• Revenue_Diff = DIVIDE([Revenue 1998]-[PreviousYearSales],[PreviousYearSales],0)



