# MAVEN MARKET SALES ANALYSIS
## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Preparation](#data-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results](#results)
- [Recommendations](#recommendations)
## Project Overview

This initiative aims to offer insights into the sales performance of Maven Market, providing an overview of customer engagement and details about returned purchases. Through the comprehensive analysis of various data aspects, the project seeks to pinpoint trends, comprehend customer behavior, generate data-driven recommendations, and enhance understanding of the market's overall performance.
<img width="507" alt="MM SALES" src="https://github.com/Modupe-Adeniyi/MAVEN-MARKET-SALES-ANALYSIS-/assets/151841781/0d51f6e8-71f5-43ce-b184-427b6c22c047">
<img width="479" alt="MM CUSTOMER" src="https://github.com/Modupe-Adeniyi/MAVEN-MARKET-SALES-ANALYSIS-/assets/151841781/6aa7edce-d461-4694-9081-d4352dcd5002">
<img width="535" alt="MM MARKET BASKET" src="https://github.com/Modupe-Adeniyi/MAVEN-MARKET-SALES-ANALYSIS-/assets/151841781/d0855fa8-6c2c-4a5a-a9be-bfceb90fd681">
<img width="566" alt="MM RETURN" src="https://github.com/Modupe-Adeniyi/MAVEN-MARKET-SALES-ANALYSIS-/assets/151841781/7142ea07-eea3-4e56-a48e-e3a30729de61">
<img width="639" alt="MM model" src="https://github.com/Modupe-Adeniyi/MAVEN-MARKET-SALES-ANALYSIS-/assets/151841781/06532b33-91c0-4e70-9007-c1bc0fb5c0d3">

## Data Sources

The primary dataset employed for this analysis is "Maven Market_Dataset.csv" sourced from Kaggle.com. This dataset encompasses detailed information on each sale, customer interactions, and product returned within Maven Market.

## Tools

- Excel was utilized for data cleaning
- PowerBI was employed for data analysis and report creation

## Data Preparation

In the initial preparation phase, the following tasks were executed:
1.	Data loading and inspection.
2.	Handling missing values.
3.	Data cleaning and formatting.
4.	Data modeling.

## Exploratory Data Analysis
EDA involved exploring the dataset to address key questions such as:
- What is the overall sales trend, and when are the peak sales periods?
- Which country boasts the highest sales figures?
- Which store achieved the highest sales overall?
- What is the customer demographic overview for the market?
- Which three products are most frequently returned after purchase?

## Data Analysis
Created calculated columns and measures using PowerBI, some include:
``` Market Basket = CALCULATE(CONCATENATEX(Sales,Sales[product_id],"-"),FILTER(ALL(Sales),Sales[customer_id]=EARLIER(Sales[customer_id])))```

``Age Bucket = 
SWITCH(TRUE(),
 MavenMarket_Customers[Age] >= 30
 && MavenMarket_Customers[Age] <= 50, " Adults",
 MavenMarket_Customers[Age] >= 50
 && MavenMarket_Customers[Age] <= 65, "Middle-Age Adults",
 MavenMarket_Customers[Age] >= 66
 && MavenMarket_Customers[Age] <= 99, "Old Adults",
 "Others"
 )``

## Results
The findings of the analysis are outlined as follows:
#### * Overall Sales Trend and Peak Sales Period 
The cumulative sales demonstrated a consistent upward trend, experiencing a significant 163.86% surge from January 1997 to December 1998. Notably, the sales began a pronounced upward trajectory in January 1998, marking a growth of 22.42% (22,005.56) over an 11-month period. The steepest incline occurred between January 1998 and December 1998, with cumulative sales rising from 98,155.28 to 120,160.84. Sales in 1998 surpassed those in 1997, with the peak sales period identified in the month of December.
#### * Country with the Highest Sales
The United States (USA) emerged as the leading country in terms of sales.
#### * Store with the Highest Sales
Store 13 stood out with the highest overall sales.
#### * Customer Demographics and Overview
The total customer count reached 10,281, comprising 5,184 males and 5,097 females. The majority of customers (60.18%) were homeowners, and there was only a marginal 0.02% difference between married and single customers. A predominant number of customers (5,703) held a bronze membership card, and the largest age group consisted of older adults (66-99 years old) with 5,008 customers.
#### * Top Three Products Returned
A total of 7,903 products were returned. Notably, Hermanos Red Pepper had the highest quantity returned, while Walrus Merlot Wine and Hermanos Oranges tied for second place. Hermanos Red Pepper accounted for 34.78% of the total quantity returned, signifying its significant impact on returns.

## Recommendations
####  1. Inventory Management for December
Ensure a higher quantity of products is available in the month of December to prevent shortages during the festive period, considering the peak in sales during that month.
####  2. Replication of Successful Advert Strategies
Replicate successful advertising strategies employed in store 13 across other stores and implement the effective advertising methods used in the USA in other countries. This can help boost sales by capitalizing on proven successful marketing approaches.
####  3. Strategic Promotion of Landslide Sesame Oil
Increase advertising efforts for Landslide Sesame Oil, given its high average profit of 70.69%, despite relatively lower sales. A focused marketing campaign can potentially enhance its sales performance.
####  4. Investigation into Old Adults with $30K - $50K Income
Conduct an investigation to understand why there is a higher percentage of customers among old adults, particularly in the $30K - $50K income range. This analysis can provide insights into the preferences and needs of this demographic, leading to targeted marketing strategies.
####  5. Quality Control for Returned Products
Implement an intense quality control check on Hermanos Red Pepper, Walrus Merlot Wine, and Hermanos Oranges, the topmost returned products. Additionally, investigate the reasons behind the higher rate of product returns in the month of November. Identifying and addressing quality issues can improve customer satisfaction and minimize returns.

By incorporating these recommendations, the business can optimize its sales strategy, enhance customer satisfaction, and mitigate challenges associated with product returns. Continuous monitoring and adaptation will be crucial for maintaining competitiveness in the market.
