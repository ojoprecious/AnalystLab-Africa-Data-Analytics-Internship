# Global Superstore Sales Dashboard

**AnalystLab Africa - Week 2 Project**

## About this project
For my Week 2 internship assignment, I built an interactive Power BI dashboard to analyze sales and profitability for the Global Superstore. The main goal was to take raw transaction data and turn it into a single, clean view that management can use to track performance, spot unprofitable areas, and make better decisions.

## The Data
I used the Global Superstore dataset, which contains around 51,000 order records from 2011 to 2014. It includes details about customers, product categories, shipping locations, sales, discounts, and profit. 

## What I did
1. **Data Cleaning:** I used Power Query to fix date formats, remove duplicate rows, handle missing postal codes, and create a new column to calculate shipping duration.
2. **DAX Measures:** I wrote formulas to calculate the main KPIs: Total Sales ($12.64M), Total Profit ($1.47M), Total Orders (~25,000), Average Sales, and Profit Margin (11.6%).
3. **Visualizations:** I built column charts, bar charts, a line graph for trends, a map for geographic sales, and a matrix table. 
4. **Interactivity:** I added slicers for Market, Category, and Year so users can filter the entire dashboard with a few clicks.

## Main findings from the data
* The business grew steadily between 2011 and 2014, more than doubling its sales.
* The US market converts sales into profit very well, but regions like APAC and the EU have high sales with very thin profit margins.
* Technology is the most profitable category. Furniture generates a lot of sales but frequently loses money, mostly due to heavy discounts.
* Deep discounts (above 40-50%) are the main reason the overall profit margin is only 11.6%.

## Tools Used
- **Power BI Desktop** – building the dashboard
- **Power Query** – cleaning the data
- **DAX** – calculating the KPIs
- **Microsoft Excel** – source data
- **GitHub** – hosting the project

## Author
**Ojo Precious Mojolaoluwa**
