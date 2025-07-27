# Unicorn Performance Analysis

## Table of Contents

- [Tools & Skills Used](#tools--skills-used)
- [Collaborators](#collaborators)
- [Quick Access](#quick-access)
- [Project Overview](#project-overview)
- [Project Deliverables](#project-deliverables)
- [About Unicorn Company](#about-unicorn-company)
- [Unicorn's Database](#unicorns-database)
- [Data Exploration using SQL](#data-exploration-using-sql)
- [Analysis with Spreadsheets](#analysis-with-spreadsheets)
- [Getting Insights using Tableau](#getting-insights-using-tableau)
- [Executive summary and presentation](#executive-summary-and-presentation)

## Tools & Skills Used

![Collaboration](https://img.shields.io/badge/Collaboration-Group%20Project-%23e91e63)
![Collaboration](https://img.shields.io/badge/Collaboration-Data%20Presentation-%23e91e63)
![SQL](https://img.shields.io/badge/SQL-Data%20Exploration-%233298DA)
![Jupyter%20Notebook](https://img.shields.io/badge/Jupyter%20Notebook-Interactive%20Analysis-%23c35817)
![Google Sheets](https://img.shields.io/badge/Google%20Sheets-Data%20Analysis-%2334a853)
![Tableau](https://img.shields.io/badge/Tableau-Dashboard-%235778a4)

## Collaborators

Meet our team behind the analysis:

| Name | Role | GitHub | LinkedIn |
| --- | --- | --- | --- |
| Annelize Krause | Project Co-ordinator & SQL | [krauseannelize](https://github.com/krauseannelize) | [annelizekrause](https://www.linkedin.com/in/annelizekrause/) |
| Reha Rabi Binti Mat | Spreadsheets & Tableau | [reharabi](https://github.com/reharabi) | []() |
| Atukunda Shakirah | Tableau & Report | []() | []() |
| Sajjad Mirzapour | Presentation & Report | []() | [sajjad-mirzapour](https://www.linkedin.com/in/sajjad-mirzapour-1b8476295/) |

[Back to Top](#table-of-contents)

## Quick Access

- [Raw Data Extract](/unicorn-dataset.csv)
- [Metadata](/unicorn-metadata.md)

[Back to Top](#table-of-contents)

## Project Overview

This group project forms part of the Masterschool Data programme to combine what we have learned on SQL, Spreadsheets, and Tableau. We will exlore the sales performance of Unicorn Company, an e-commerce business offering a wide range of products, for the years 2015 to 2018 to identify performance trends, weaknesses, and growth opportunities. The project consist of 4 main parts:

- Data Exploration using SQL
- Analysis with Spreadsheets
- Getting Insights using Tableau
- Executive summary and presentation

[Back to Top](#table-of-contents)

## Project Deliverables

These deliverables, submitted to Masterschool as part of our final project using public links, showcase our technical methods, strategic insights, and the collaborative effort behind our work:

- SQL document containing the SQL queries used to answer the questions in the [Data Exploration using SQL](#data-exploration-using-sql) section of the project.
- The Spreadsheet used to analyze the data to answer the questions in the [Analysis with Spreadsheets](#analysis-with-spreadsheets) section.
- Tableau Public dashboard communicating our insights.
- One-page PDF report with an executive summary containing our main insights and recommendations.
- Video recording (up to 5 minutes) of the team sharing their insights and explaining the process followed.
- Presentation in PDF format if a slide deck was used in our video presentation.

[Back to Top](#table-of-contents)

## About Unicorn Company

Unicorn is a family business and is owned by 2 stakeholders who are very invested in their business. They already have a small data analytics team but want to expand it significantly over the next few months. As part of the interview process for a new DA postion, they provide a sample dataset from their sales data. The interview task is to analyze the data, find interesting insights, and identify weak areas and opportunities for Unicorn to boost its business growth.

[Back to Top](#table-of-contents)

## Unicorn's Database

URL to PostgreSQL dataset: `postgresql://Test:bQNxVzJL4g6u@ep-noisy-flower-846766-pooler.us-east-2.aws.neon.tech/Unicorn?sslmode=require`

Below is a schema of Unicorn's database:

![Unicorn's Database Schema](/unicorn-database-schema.png)

For a more details description of the database, consult the [metadata sheet](/unicorn-metadata.md).

[Back to Top](#table-of-contents)

## Data Exploration using SQL

To kick off the analysis, we use SQL to answer a series of core business questions about the Unicorn sales database, covering customer trends, city profitability, and product performance.

- The [SQL Specifications](/specifications-sql.md) detail the required queries.
- All SQL code and outputs are documented in our [Jupyter Notebook](/unicorn_exploration.ipynb).
- The [full joined dataset CSV export](/unicorn_extract.csv) from the bonus question is also available for review.

[Back to Top](#table-of-contents)

## Analysis with Spreadsheets

In this stage, we use spreadsheets to clean and further analyze the Unicorn dataset, addressing data quality issues and performing targeted business analysis.

- Detailed requirements are in the [Spreadsheet Specifications](/specifications-spreadsheets.md).
- All data cleaning steps, analyses, and answers are documented in our [Google Sheets workbook](https://docs.google.com/spreadsheets/d/1m67MvPY3IG0gM0Y3MYFQa8PUrFpDLqbW26qmhYt5CsU/edit?usp=sharing), with a downloadable copy available as [Spreadsheet workbook (.xlsx)](/unicorn-analysis.xlsx).

## Getting Insights using Tableau

In this phase, we create interactive dashboards in Tableau to visualize key business metrics and uncover actionable insights from the cleaned and explored Unicorn dataset.

- Suggested metrics to explore and guidelines are in the [Tableau Specifications](/specifications-tableau.md).
- The published Dashboard can be viewed on [Tableau Public](https://public.tableau.com/views/unicornprojectfinal_17533900132030/Dashboard).
- The [Tableau workbook (.twbx)](/unicorn-dashboard.twbx) is also included to allow offline exploration.

[Back to Top](#table-of-contents)

## Executive summary and presentation

This final section presents a concise overview of our data analysis findings tailored for key stakeholders.

- Watch the [Video Presentation](https://drive.google.com/file/d/12QtyPwSb2Fidx_r17CvwDr7ZTxiUF9Qi/view?usp=sharing).
- Read the [Executive Summary (PDF)](/unicorn-executive-summary.pdf) highlighting main insights and recommendations.
- Review the [Presentation Slide Deck (PDF)](/unicorn-slide-deck.pdf) used during the presentation.

[Back to Top](#table-of-contents)
