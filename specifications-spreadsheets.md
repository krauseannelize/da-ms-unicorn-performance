# Analysis with Spreadsheets

## All data in one table in CSV format

[Click here to access the data](/unicorn-dataset.csv)

## Introduction

For this part of the project, you’ll use Google Spreadsheets.

In the second part of the project, before you dive deeper into your own unguided data research,  answer the following questions by Spreadsheet querying.

Prepare a doc with answers to the following questions and a short description of the method you used in Spreadsheets. Add the link to your spreadsheet with new columns, pivot tables etc.

## Differences between Database and Spreadsheet Columns

There is an important difference between the columns available in the Database Table vs. the Spreadsheet:

- The spreadsheet is missing the following columns:
  - Customer_id: Probably because we have the names of all the clients in each row, so the id could have been considered redundant.
  - Shipping_postal_code: It was not considered essential, as all orders have already been shipped.
  - Shipping_country: Since all orders in the spreadsheet are from the USA, it was considered redundant to have this column.
  - Order_details_id: Since all the details of the order are in every row, this was not added to the spreadsheet.
  - Product_id: Every row contains the specific product ordered, so the id for it was considered redundant.

There is one additional column in the spreadsheet: Shipping_price. This does not exist in the Database, since it was added after the items were already shipped.

The differences help us observe and understand how things can be managed differently when using a Relational Database vs. using spreadsheets to manage information.

## 🏎️ Questions to Answer

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

![Question 19 spreadsheet output](/specifications-spreadsheets-q19.png)

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

## The section below is optional; it’s not part of the Quiz. Here are some additional guidelines to help the Unicorn DA team to monitor their data every day:

1. Use a combination of functions and conditional formatting to create a dashboard that visualizes the total sales, profit, and average discount for each region.
2. Create a new sheet that uses a formula to calculate the monthly sales, profit, and profit margin for each category and sub-category. Use a chart to visualize the results.
3. Open a new tab in your Spreadsheet tool and create a table that is filtered dynamically by year.
4. Use your filtered table to create a “Profit per year” dashboard. In that dashboard, you can choose a year, and all the data should change dynamically. Your dashboard should contain at least the following:
- A histogram of the profit column with a bucket size of 20 and an outlier percentile of 5% and/or a chart that shows the profit over the months (you could do a line chart or a waterfall chart). (Note: the months should be placed in the correct order!)
- Top five profitable subcategories
- Bottom five profitable subcategories
- Top 10 profitable customers
- Bottom ten profitable customers.

In addition to the charts, your dashboard should include the following numbers (which should change dynamically by year) , these are:

- Sum of positive profit
- Sum of negative profit
- Number of distinct orders

🦄

Good luck!
