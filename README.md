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

In the first part of the project, we dive deeper into our unguided data research by answering the following questions utilizing SQL queries:

1. How many customers do we have in the data?
1. What was the city with the most profit for the company in 2015?
1. In 2015, what was the most profitable city's profit?
1. How many different cities do we have in the data? Please refer just to the city name and not similar city names in different states
1. What is the most profitable city in the State of Tennessee?
1. What is the distribution of customer types in the data?
1. Which was the biggest order regarding sales in 2015?
1. Display customer names for customers who are in the segment ‘Consumer’ or ‘Corporate.’ How many customers are there in total?
1. Calculate the difference between the largest and smallest order quantities for product id ‘100.’
1. Calculate the percent of products that are within the category ‘Furniture.’
1. Display the manufacturers with more than 1 product in the product table, with their number of products. (Note: Do not sort your results, and do not use distinct because it affects output order)
1. Show the product_subcategory and the total number of products in the subcategory. Show the order for the _most_ to _least_ number of products.
1. Show the product_id(s), the sum of quantities, where for each sale of product quantities is greater than or equal to 100.

:star: **Bonus question:** Join all database tables into one dataset that includes all unique columns and download it as a .csv file.

## Data Cleaning using Spreadsheets

## Getting Insights using Tableau

## Executive summary and presentation