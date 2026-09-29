# Nova Retail Executive Sales Dashboard

## About the project

This is a Power BI project based on retail sales data. I built the dashboard to understand sales performance from different business perspectives — overall sales, products, customers, and regions.

The project started with raw data and was taken through data preparation, data modeling, DAX measures, and dashboard development.

My main focus was not only to create charts, but to understand what the data was showing and use the dashboard to answer practical business questions.

## Dashboard Preview

![Nova Retail Sales Overview](Screenshots/Sales%20Overview.png)

## Business questions

The dashboard was created to explore questions such as:

* How are sales changing month by month?
* Which products are performing well and which are performing poorly?
* Which customers contribute the most to sales?
* Which cities contribute the most to overall sales?
* How does category performance vary between cities?
* How does sales performance look on an MTD, QTD, and YTD basis?

## Data used

The project uses four tables:

* Sales
* Customers
* Products
* DateTable

The original data files are available in the `Data` folder.

## Data preparation

I used Power Query to prepare and understand the data before building the report.

The preparation included:

* Checking missing and blank values
* Reviewing data types
* Checking keys and relationships
* Understanding the grain of the Sales table
* Identifying potential data issues before modeling

## Data model

I used a star-schema approach for the Power BI model.

The model contains:

* `Sales` as the fact table
* `Customers` as a dimension table
* `Products` as a dimension table
* `DateTable` as the date dimension

The dimension tables are connected to the Sales table through one-to-many relationships with single-direction filtering.

A screenshot of the model and its relationships is included in the `Screenshots` folder.

## DAX and time intelligence

I created measures for:

* Total Sales
* Total Transactions
* Total Quantities
* Total Customers
* MTD Sales
* QTD Sales
* YTD Sales
* KPI-related calculations

A dedicated DateTable was used for the time-intelligence calculations.

## Dashboard pages

### Sales Overview

This page gives an overall view of sales performance using cards, monthly analysis, and MTD/QTD/YTD measures.

### Product Analysis

This page looks at sales at the product level.

It includes:

* Product and month slicers
* Top 5 product view
* All Products view
* Bookmarks
* Interactive buttons

### Customer Analysis

This page compares customer performance and includes a Top 10 customer analysis.

### Customer Details

This is a drillthrough page used to look at the details of a selected customer.

### Regional Analysis

This page analyzes sales across cities and categories and allows the data to be explored using different filters.

### Product Tooltip

I created a report tooltip to provide additional product-level information while interacting with the report.

## Some observations from the analysis

A few observations from the dashboard include:

* May had the highest monthly sales in the analyzed data.
* Furniture accounted for the largest share of sales among the three categories.
* Surat had the highest sales contribution among the analyzed cities.
* A relatively small group of top customers contributed a significant share of total sales.
* Product performance varied across both products and months.

These observations are based on the data used in this project.

## Power BI features used

* Power Query
* Data modeling
* Star schema
* DAX
* Time intelligence
* Slicers
* Top N filtering
* Bookmarks
* Buttons
* Drillthrough
* Report tooltips
* Interactive visual filtering

## Tools

* Microsoft Power BI
* Power Query
* DAX
* Microsoft Excel
* GitHub

## Repository structure

```text
Nova-Retail-PowerBI/
│
├── README.md
├── Nova Retail Executive Sales Dashboard.pbix
│
├── Business Requirement/
│   └── Business Requirement.xlsx
│
├── Data/
│   ├── Customers.csv
│   ├── Products.csv
│   ├── Sales.csv
│   └── DateTable.csv
│
└── Screenshots/
    ├── Sales Overview.png
    ├── Product Analysis.png
    ├── Customer Analysis.png
    ├── Customer Details.png
    ├── Regional Analysis.png
    ├── Product Tooltip.png
    └── Model View.png
```

## What I learned from this project

Building this project helped me understand the complete flow of a Power BI analysis:

**Raw data → Data understanding → Data preparation → Data modeling → DAX → Visualization → Business insights**

It also helped me understand that building a dashboard is not just about creating visuals. The important part is understanding the data, choosing the right model and measures, and then using the report to investigate business questions.
