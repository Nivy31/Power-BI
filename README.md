

# Blinkit-Dashboard

## Problem Statement

Blinkit, a leading grocery delivery service, aims to optimize its operations and enhance customer satisfaction through data-driven decision-making. To achieve this, Blinkit needs a comprehensive dashboard that provides real-time insights into various aspects of the business. The dashboard should help the management team monitor performance, identify trends, and make informed decisions to improve efficiency, customer experience, and overall profitability.

### Business Requirements

- KPI's Requirement:
1. Total Sales : The overall Revenue generated   from all items sold.

2. Average sales : The average revenue per sales.

3. Number of items : Total count of different items sold.

4. Average Rating : Average customer rating for items sold.

- Chart's Requirement:
1.Total sales by fat content

2.Total sales by item type

3.Total sales by outlet establishment

4.Fat content by outlet for total sales

5.Sales by outlet size

6.sales by outlet Location

7.All metrics by Outlet type

Steps Followed:
- Step 1 : Load data into Power BI Desktop, dataset is a excel file.

- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.

- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".

- Step 4 : Four card visuals were added to the canvas,representing total sales, average sales, number of items and average rating.

DAX Expressions for the above metrics:
Total Sales = SUM('BlinkIT Grocery Data'[Sales])

Avg Sales = AVERAGE('BlinkIT Grocery Data'[Sales]) 

Number of items = COUNTROWS('BlinkIT Grocery Data')

Avg Rating = AVERAGE('BlinkIT Grocery Data'[Rating])

- Step 5 : Donut chart is used to analyze the impact of fat content on total sales.
Also asseses how other KPI metrics(Total Sales,Avg Sales,Number of items,Avg Rating) vary with fat content.

Create a Field Parameter:

Name it "Select Metric".
Add Total Sales, Average sales,Number of items and average rating as fields.

Add to Visual:
Create a Donut chart.
Drag the "Select Metric" parameter to the Values field of the chart.

Create a Slicer:
Add a slicer to the report.
Use the "Select Metric" parameter in the slicer.
Now, users can use the slicer to switch between Total Sales,Average sales,Number of items and average rating in the donut chart dynamically.

- Step 6 : Bar chart is used to identify the performance of different item types in terms of total sales.
Also asseses how other KPI metrics(Total Sales,Avg Sales,Number of items,Avg Rating) vary with fat content. 
In bar chart, 
          X axis - metrics 
          Y axis - item type

- Step 7 : Stacked column chart is to compare total sales across different outlets segmented by fat content.
Also asseses how other KPI metrics(Total Sales,Avg Sales,Number of items,Avg Rating) vary with fat content.
In stacked column chart, 
           X axis - metrics 
           Y axis - outlet location type.

- Step 8 : Line chart is used to evaluate how the age or type of outlet establishment influences total sales.
In line chart, 
     X axis - outlet establishment year  
     Y axis - total sales

- Step 9 : Donut chart is used to analyze the correlation between total sales and outlet size.
In donut chart, 
              legend - outlet size 
              values - total sales

- Step 10 : Funnel map is used to evaluate the geographic distribution of sales across different locations.
In funnel map,
     Category - Outlet location type
     Values - Total sales

- Step 11 : Matrix card is used to provide a comprehensive view of all key metrics(Total Sales, Average sales,Number of items and average rating) broken down by different outlet types.
In matrix card,
      Rows - Outlet type
      Values - Total sales, Number of items,avg sales,avg rating and item visibility.

- Step 12 :In the report view, under the insert tab, three text boxes were added to the canvas, in one of them blinkit was mentioned & in the other one company's tagline and filter panel was written.

- Step 13 : In the report view, under the filter panel,slicers was inserted for outlet location type,outlet size and item type.

- Step 14 : The report was then published to Power BI Service.










  



