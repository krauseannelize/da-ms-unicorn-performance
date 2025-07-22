# Unicorn Performance Analysis

## Tools & Skills Used

![SQL](https://img.shields.io/badge/SQL-Data%20Exploration-%233298DA)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-Data%20Cleaning-%2334a853)
![Tableau](https://img.shields.io/badge/Tableau-Dashboard-%235778a4)  

## Collaborators

Meet our team behind the analysis:

| Name | Role | GitHub | LinkedIn |
| --- | --- | --- | --- |
| Annelize Krause | Project Co-ordinator & SQL | [krauseannelize](https://github.com/krauseannelize) | [annelizekrause](https://www.linkedin.com/in/annelizekrause/) |
| Reha Rabi Binti Mat | Spreadsheets | []() | []() |
| Atukunda Shakirah | Tableau & Report | []() | []() |
| Sajjad Mirzapour | Tableau & Report | []() | [sajjad-mirzapour](https://www.linkedin.com/in/sajjad-mirzapour-1b8476295/) |

## Quick Access

- [Raw Data Extract](/unicorn-dataset.csv)
- [Metadata](/unicorn-metadata.md)

## Project Overview

This group project forms part of the Masterschool Data programme to combine what we have learned on SQL, Spreadsheets, and Tableau. We will exlore the sales performance of Unicorn Company, an e-commerce business offering a wide range of products, for the years 2015 to 2018 to identify performance trends, weaknesses, and growth opportunities. The project consist of 4 main parts:

- Data Exploration by SQL
- Data Cleaning using Spreadsheets
- Getting Insights using Tableau
- Executive summary and presentation

## About Unicorn Company

Unicorn is a family business and is owned by 2 stakeholders who are very invested in their business. They already have a small data analytics team but want to expand it significantly over the next few months. As part of the interview process for a new DA postion, they provide a sample dataset from their sales data. The interview task is to analyze the data, find interesting insights, and identify weak areas and opportunities for Unicorn to boost its business growth.

## Unicorn's Database

URL to PostgreSQL dataset: `postgresql://Test:bQNxVzJL4g6u@ep-noisy-flower-846766-pooler.us-east-2.aws.neon.tech/Unicorn?sslmode=require`

Below is a schema of Unicorn's database:

![Unicorn's Database Schema](/unicorn-database-schema.png)

For a more details description of the database, consult the [metadata sheet](/unicorn-metadata.md).

## Data Exploration by SQL

In the first part of the project, we dive deeper into our unguided data research by answering questions utilizing SQL queries.

### Questions to answer

1. How many customers do we have in the data?
2. What was the city with the most profit for the company in 2015?
3. In 2015, what was the most profitable city's profit?
4. How many different cities do we have in the data? Please refer just to the city name and not similar city names in different states
5. What is the most profitable city in the State of Tennessee?
6. What is the distribution of customer types in the data?
7. Which was the biggest order regarding sales in 2015?
8. Display customer names for customers who are in the segment ‘Consumer’ or ‘Corporate.’ How many customers are there in total?
9. Calculate the difference between the largest and smallest order quantities for product id ‘100.’
10. Calculate the percent of products that are within the category ‘Furniture.’
11. Display the manufacturers with more than 1 product in the product table, with their number of products. (Note: Do not sort your results, and do not use distinct because it affects output order)
12. Show the product_subcategory and the total number of products in the subcategory. Show the order for the _most_ to _least_ number of products.
13. Show the product_id(s), the sum of quantities, where for each sale of product quantities is greater than or equal to 100.

### :star: Bonus question

Join all database tables into one dataset that includes all unique columns and download it as a .csv file.

## Data Cleaning using Spreadsheets

In the second part of the project, we will use spreadsheets to answer some questions as part of the deep dive. For this purpose, we are provided with an [extract of the dataset in csv format](/unicorn-dataset.csv). Important differences between the Unicorn Database and this extract:

- The following columns were omitted from the extract:
  - `customer_id`: As the names of all customers are included, the id was deemed redundant.
  - `Shipping_postal_code`: Not essential as all orders have already been shipped.
  - `Shipping_country`: Redundant as all orders are from the United States.
  - `Order_details_id`: As all order details are included, the id was deemed redundant.
  - `Product_id`: As all product information are included, the id was deemed redundant.
- The following columns were added to the extract:
  - `unit price`: Extracted from the database using `order_sales` divided by `order_discount` (if any), returning the pre-discount sales value that is inturn divided by `quantity` to give the price of each unit
  - `shipping_price`: Does not exist in the Database, since it was added after the items were already shipped.

### Questions to answer

1. What was the city with the highest sales?
2. What is the average discount given for all orders?
3. What is the most popular product among customers in the "Consumer" segment?
4. What is the total profit made for the "Office Supplies" category?
5. Who is the customer who has made the most purchases? (_Hint: use the “Order ID column to answer the question._)
6. What state made the most profit?
7. How many orders were shipped via "Standard Class" ship mode?
8. Which region had the highest sales in the month of June?
9. Calculate the price per unit of each product (before discounts), and put it in a separate column. What's the most expensive product? _Hint: use the quantity, sales, and discount columns._
10. Create a pivot table that shows the total sales for each manufacturer and category combination. In the "Technology" category, which manufacturer had the second highest sales?
11. What is the subcategory of “Xerox 1887”?
12. Create a new column that calculates the number of days between the order date and the ship date for each order. Create a conditional formatting “color scale” for this column, from greenish to reddish.
13. What is the number of days between order date and shipping date for order id - “CA-2015-100363”?
14. What is the shipping price for order id “CA-2015-100678”?
15. Create a new column that concatenates the customer name, city, and state into a single string for each order.
16. Use the IFS function to create a new column that categorizes each order as "**High**", "**Low**", or "**Loss**" based on profit and sales criteria.
- "**High**" is considered as:
  - If sales are above 200 and profit is above 20
  - If profit is above 40.
- For other cases:
  - If the profit is equal or below 0 this is categorized as “**Loss**”
  - Any other case this is categorized as "**Low**"
17. Use conditional formatting to color the columns with the values “**High**” in green, the value “**Low**” in yellow and the value “Loss” in red.
18. How many “**Loss**” cases do you have?
19. In a new sheet, create a dropdown of category and product which returns the price for a unit (which you previously solved in exercise 9). See the image below as a reference:

![Question 19 spreadsheet output](/p2-spreadsheet-q19.png)

_Hint:_

- _In order to make your job easier and for it to look cleaner, you should first define "named ranges" for every column you will use - product name, category, unit price._
- _Create a drop-down list of categories:_
  - _In a separate cell, use data validation to create a drop-down list of categories, using the category column in your data as the source._
  - _In the data validation criteria, use “Dropdown (from a range)” and put the named range of your category column in there._
- _In a separate sheet, use the “filter” function to filter the products based on your chosen category. Give this a named range too._
- _Create a drop-down list of product names based on the selected category; use this name range you have created in the separate sheet._
- _Use the INDEX MATCH function to find the corresponding product unit price. You could use this structure:_
  -  `=INDEX(unit_price, MATCH(1, (category=The_category_cell)*(product_name=The_product_cell), 0), 1)`
- _Note: Unit_price, category, and product_name are named ranges._
- _Note: If the named range doesn't work, try to insert the range itself_

### :star: Optional Questions

20. Use a combination of functions and conditional formatting to create a dashboard that visualizes the total sales, profit, and average discount for each region.
21. Create a new sheet that uses a formula to calculate the monthly sales, profit, and profit margin for each category and sub-category. Use a chart to visualize the results.
22. Open a new tab in your Spreadsheet tool and create a table that is filtered dynamically by year.
23. Use your filtered table to create a “Profit per year” dashboard. In that dashboard, you can choose a year, and all the data should change dynamically. Your dashboard should contain at least the following:
- A histogram of the profit column with a bucket size of 20 and an outlier percentile of 5% and/or a chart that shows the profit over the months (you could do a line chart or a waterfall chart).
Note: the months should be placed in the correct order!
- Top five profitable subcategories
- Bottom five profitable subcategories
- Top 10 profitable customers
- Bottom ten profitable customers.
24. In addition to the charts, your dashboard should include the following numbers (which should change dynamically by year) , these are:
- Sum of positive profit
- Sum of negative profit
- Number of distinct orders

## Getting Insights using Tableau

## Executive summary and presentation