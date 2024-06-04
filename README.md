# Indian-Start-up-Ecosystem-Project

## Table of content
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Data Analysis](#data-analysis)
- [Insights](#insights)
- [Contact Information](#contact-information)


## Project Overview

My team is looking to venture into the Indian start-up ecosystem and so I, as a data expert has been tasked with investigating this start-up ecosystem in India, to recommend the best course of action for the team. My research is going to focus on the details of funding for these start-ups in India, where I will dive deep into a data containing all the details about fundings received by the start-ups and communicate my findings and recommendations to the team in the best way possible.

I will be leveraging the widely used CRISP-DM Framework for this project.

The CRISP-DM (Cross-Industry Standard Process for Data Mining) framework is a widely used methodology for data mining and data analysis projects. It provides a structured approach for planning and executing data projects. The process is cyclic and iterative, consisting of six phases:

1. Business Understanding
2. Data Understanding
3. Data Preparation
4. Modeling
5. Evaluation
6. Deployment

Though in this project, steps 4 and 5 won't be implemented

## Data Sources

For this project, I had to gather data from different sources. The data for 2018 is hosted in a github repository [here](https://github.com/Azubi-Africa/Career_Accelerator_LP1-Data_Analysis/blob/main/startup_funding2018.csv)

The data for 2019 was hosted on OneDrive, which I downloaded to my local stotage and uploaded to my github repo to be read in to pandas from there. Data for 2020 and 2021 were hosted on an SQL Server database that was accessed using the right credentials like username, database name, password and server.

below are the common fields/columns for 2019, 2020 and 2021 and their descriptions

| Field           | Description                                                     |
|-----------------|-----------------------------------------------------------------|
| Company_Brand   | Name of start-up company                                        |
| Founded         | Year it was founded                                             |
| HeadQuarter     | Headquarters or location of the company                         |
| Sector          | Sector of the company                                           |
| What_it_does    | A brief description of what the company does                    |
| Founders        | Name(s) of the founder(s) of the company                        |
| Investor        | Name(s) of the investor(s) of the company                       |
| Amount          | Amount invested into the company by investor(s)                 |
| Stage           | Current stage of the startup (e.g. Pre-seed, Pre-series, Series A, Series D) |


2018 had different column names but most had the same meaning as the columns for 2019, 2020 and 2021

| Field           | Description                                                     |
|-----------------|-----------------------------------------------------------------|
| Company Name    | Name of start-up company                                        |
| Industry        | Sector of the company                                           |
| Round/Series    | Current stage of the startup                                    |
| Amount          | Amount invested into the company by investor(s)                 |
| Location        | Headquarters or location of the company                         |
| About Company   | A brief description of what the company does                    |

At the end the concatenation and feature engineering, these were the current columns

| Field           | Description                                                     |
|-----------------|-----------------------------------------------------------------|
| Company_Brand   | Name of start-up company                                        |
| Founded         | Year it was founded                                             |
| HeadQuarter     | Headquarters or location of the company                         |
| Sector          | Sector of the company                                           |
| What_it_does    | A brief description of what the company does                    |
| Currency        | Currency from the 'Amount' column                               |
| Investor        | Name(s) of the investor(s) of the company                       |
| Amount          | Amount invested into the company by investor(s)                 |
| Stage           | Current stage of the startup (e.g. Pre-seed, Pre-series, Series A, Series D) |
| Num_of_Investors| Number of investor(s) of the startup company                    |
| Num_of_Founders | Number of founders of the startup company                       |
| new_amount      | cleaned version of the 'Amount' column                          |


## Data Cleaning and Preparation

Before the data cleaning process begins, differing column names in all the 4 datasets were replaced with the right names to make concatenation successful. Then a 'Year' column was added to each of the dataset to help when running a yearly analysis on the data. After concatenation, the data contained 2879 rows and 11 columns.

The data had a lot of missing values in the columns which will later be imputed with the right central tendency value and also duplicates which were dropped during the data cleaning process.

The cleaning process was done by tackling one column before the next column and some of the issues solved during the process were;

- #### Problems with the 'HeadQuarter' column
  - Incorrect city names (wrong spellings)
  - Having the country attached to it (Trivandrum, Kerala, India)
  - Missing values

- #### Problems with the 'Sector' column
  - Double Sectors
  - dash entries ('-')
  - missing values

- #### Problems with the 'Amount' column
  - missing values
  - currency mix-up
  - figures without currencies (some in Rupees while some in Dollars)
  - invalid entries(Seed, $, Undisclosed)
  - mixed up data types

- #### Problems with the 'Stage' Column
  - Invalid stages
  - url links as entries
  - missing values

- #### Problems with the 'Num_of_Investors', 'Num_of_Founders', and 'Currency' columns
  - missing values

- #### Exploratory Data Analysis
Visualizing the distribution of the numerical columns in the data and identifying trends

## Data Analysis

In this section I will first test my three hypothesis which were;

- Hypothesis 1: Startups headquartered in major metropolitan areas of India likely to receive higher funding amounts than other areas. 
- Hypothesis 2: Startups with multiple investors are likely to receive higher amounts of funding.
- Hypothesis 3: Funding amounts vary across sectors.

I then go ahead to answer my business questions;

1. what is the overall trend in funding amounts over the specified time period? 
   - Total and average funding amounts over the years?

2. Which year had the most investors?

3. Which startups received the highest funding amount for each year?
   - Which sectors are those companies from?
   - What does these companies do?

4. What are the top 5 and bottom 5 start-ups according to funding amount and Which sectors are they from?

5. What are the top 5 and bottom 5 sectors by Total Funding amount received?

6. What is the number of startups by sectors?

7. Top 10 HQ locations by average funding amounts.
   
8. What is the number of fundings per HQ locations?

9. What is the average amount of funds received by startups at different stages?

10. What is the average number of founders per startup?
    - Show a distribution plot of the number of founders.

## Insights

Some key findings from the analysis will be listed here with recommendations at the end of the project.



## Contact Information

For any questions or suggestions, please contact:

email : [my email](richmondyeboah299@gmail.com)

GitHub: [richmond-yeboah](https://github.com/richmond-yeboah)






