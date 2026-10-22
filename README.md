# FInancial-Business-analysis-Dashboard
Interactive Power BI dashboard analyzing sales, revenue,  performance, and business KPIs.
Financial & Business Analysis Dashboard
📌 Project Overview
This project presents an interactive Financial & Business Analysis Dashboard built with Microsoft Power BI. It brings key financial and operational indicators into one place to help users monitor performance, explore trends, and compare results across time periods, event types, terminals, and locations.
Data note: The values shown in the dashboard screenshot (such as Total Profit of 120M, Total Revenue of 257.26M, and 84K orders) should be validated against the final dataset and Power BI measures before being used in formal reporting.

🎯 Project Objectives
- Provide a consolidated view of financial and operational performance.
- Monitor revenue, profit, profit margin, and order volume.
- Identify trends and changes over time.
- Compare performance by event type, year, quarter, terminal, and location.
- Highlight areas for further investigation.
- Present information in a clear, interactive format.
🧰 Tools & Technologies
- Microsoft Power BI Desktop — dashboard development and report authoring.
- Power Query — data import, cleaning, and transformation, where used.
- DAX — calculations and measures, where used.
- Power BI visuals — KPI cards, line charts, bar/column charts, donut charts, and map visuals.
- GitHub — project documentation and portfolio presentation.
Keep only the tools and techniques you actually used.
📊 Dashboard Overview
1. KPI Cards
- Total Profit — total profit in the selected filter context.
- Total Revenue — total revenue in the selected filter context.
- Profit Margin — profit as a proportion of revenue.
- Total Orders — number of orders represented by the dataset.
The screenshot displays example values of 120M total profit, 257.26M total revenue, 46.52% profit margin, and 84K total orders. Verify these against the final report.
2. Analysis Over Time
Date slicers and visuals support exploration across purchase dates, hire dates, and relevant time periods.
3. Monthly Trend by Profit Margin
A line chart compares profit margin across months, helping identify stronger or weaker periods and fluctuations that may need investigation.
4. Revenue by Event Type
A category visual compares revenue by event type, shown as Delivery and Pickup in the screenshot.
5. Quarterly Fuel Gallon
A donut chart summarizes fuel gallons by quarter. Confirm the unit and definition of the source field.
6. Profit by Year
A donut chart compares the distribution of profit across years.
7. Cost of Maintenance Yearly
A chart compares maintenance costs by year to help identify periods that may need a deeper cost review.
8. Incident / Cost Analysis
The report includes incident-related cost visuals by year and quarter. Confirm the exact meaning of each field before drawing conclusions.
9. Top 20 Terminal by Total Revenue
A ranked bar chart compares revenue across terminals, helping identify high-revenue locations for further analysis.
10. State by Total Profit
A map visual plots total profit geographically across states. Results depend on accurate location fields and geocoding.
11. Vehicle / OIL Image Panel
The dashboard includes a vehicle image panel labelled “OIL.” Treat it as contextual branding unless it is connected to a specific measure.
📐 KPI Definitions and Example DAX
The following formulas are templates, not verified formulas from the Power BI model. Replace table and column names with the names in your dataset and validate each business definition.
Total Revenue
Total Revenue =
SUM ( 'YourTable'[Revenue] )
Total Profit
Total Profit =
SUM ( 'YourTable'[Profit] )
Profit Margin
Profit Margin =
DIVIDE ( [Total Profit], [Total Revenue], 0 )
Format this measure as a percentage.
Total Orders
If each row represents one order:
Total Orders =
COUNTROWS ( 'YourTable' )
If a unique order identifier exists, use a distinct count:
Total Orders =
DISTINCTCOUNT ( 'YourTable'[Order ID] )
Choose the formula that matches the dataset grain. If one order can occupy multiple rows, do not count rows as orders.
Revenue by Event Type
Revenue by Event Type =
[Total Revenue]
Place the event-type field on the chart axis or legend. The visual's filter context provides the category breakdown, so a separate measure may not be needed.
Total Fuel Gallons
Total Fuel Gallons =
SUM ( 'YourTable'[Fuel Gallons] )
Total Maintenance Cost
Total Maintenance Cost =
SUM ( 'YourTable'[Maintenance Cost] )
Total Incident Cost
Total Incident Cost =
SUM ( 'YourTable'[Incident Cost] )
Average Revenue per Order (optional)
Average Revenue per Order =
DIVIDE ( [Total Revenue], [Total Orders], 0 )
Use the actual column names and confirm whether costs are stored as positive expenses or negative values.
🔎 Key Analysis Questions
1. How do total revenue and total profit change over time?
2. Which months show higher or lower profit margins?
3. What proportion of revenue comes from each event type?
4. How is fuel consumption distributed across quarters?
5. How does profit vary between years?
6. Which years account for the largest maintenance costs?
7. Which quarters or years show the highest incident-related costs?
8. Which terminals contribute the most revenue?
9. Which states have the highest or lowest total profit?
10. Do changes in revenue coincide with changes in profit margin?
💡 Business Recommendations
These are investigation-led recommendations. Validate them against the dataset before presenting them as confirmed findings.
- Monitor profitability alongside revenue: Review total profit and profit margin together so revenue growth is not mistaken for improved profitability.
- Investigate low-margin periods: Check whether pricing, costs, event mix, or operating conditions explain weaker monthly margins.
- Review event-type performance: Compare Delivery and Pickup revenue with associated costs and margins before reallocating resources.
- Manage maintenance costs: Investigate unusual cost increases while considering fleet size, utilization, and maintenance requirements.
- Examine incident-related costs: Identify periods with high incident costs and investigate root causes and preventive actions.
- Compare terminal performance: Assess high-revenue terminals alongside cost, capacity, volume, and profit—not revenue alone.
- Use geographic results carefully: Validate location data and compare state-level profit with sales volume and cost before changing regional strategy.
- Review KPIs regularly: Establish a consistent cadence for reviewing revenue, profit, margin, orders, fuel, and cost measures.
⚠️ Limitations
- Data quality: Insights depend on the completeness and reliability of the source data.
- Metric definitions: Revenue, profit, order count, fuel, maintenance cost, and incident cost need consistent definitions.
- Historical reporting: The dashboard summarizes available data; it does not automatically forecast future results.
- Causality: A chart trend or correlation does not prove that one factor caused another.
- Geographic accuracy: Map results can be affected by missing, ambiguous, or incorrectly geocoded locations.
- Filter context: KPI values can change with slicers and report filters; check selected periods and categories before comparing values.
- Screenshot values: Reconcile displayed figures with the final Power BI file before external reporting.
- Example formulas: The DAX templates must be adapted and tested against the actual model.
📚 Data Sources & References
  
- Dataset: [Add dataset name and source URL]
- Microsoft Power BI documentation: https://learn.microsoft.com/en-us/power-bi/
- DAX function reference: https://learn.microsoft.com/en-us/dax/
- Power Query documentation: https://learn.microsoft.com/en-us/power-query/
🚀 How to Use This Project
  
financial-business-analysis/
├── README.md
├── screenshots/
│   └── dashboard-overview.png
├── data/
│   └── README.md
└── Financial-Business-Analysis.pbix
Only include data if you have permission to share it. If the dataset is confidential or too large, document how to obtain it instead. Share the .pbix file only if doing so is safe and permitted.
👤 Author
Peter Kess
- Portfolio: https://canva.link/a3iaibbhnnz0b75
- LinkedIn: https://www.linkedin.com/in/kess-peter-bb851
📌 Conclusion
This project demonstrates an approach to combining financial and operational metrics in an interactive Power BI report. It brings together headline KPIs, time-based trends, category comparisons, terminal performance, cost analysis, and geographic views to support further investigation and informed business decisions.
