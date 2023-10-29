# Home_Sales
Module 22 Challenge - Big Data

# Introduction
In this challenge, you'll use your knowledge of SparkSQL to determine key metrics about home sales data. Then you'll use Spark to create temporary views, partition the data, cache and uncache a temporary table, and verify that the table has been uncached.

# Project setup
The project started by importing the necessary Python packages to set up the environment and work with SparkSQL.

![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/1ca05851-be04-4c30-9500-88cb672d880a)
![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/2f49463b-acb6-4ffa-86e3-f30b7fa8eae8)

A SparkSession is essential for connecting to Spark and working with SparkSQL. 

![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/d8d4372f-442e-4c31-a7ff-8d225abaeaa6)

In this project, home sales data was retrieved from an AWS S3 bucket. 

![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/2e146944-f39b-460d-a3f1-4ef40251a4fc)

# Data Processing and Analysis
A temporary view named "home_sales" was created for the DataFrame using createOrReplaceTempView() method. This allowed for running SQL queries on the DataFrame.

![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/79ab32ea-5d01-4c18-b576-9f4e51bfde06)

Question 1:
*	What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/ba8a7388-d70c-4e5a-8cca-70f2c0ef42d0)
![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/a18d8a96-8157-40aa-8396-f4adeb5aa673)

Question 2:
*	What is the average price of a home for each year the home was built that have 3 bedrooms and 3 bathrooms rounded to two decimal places?
![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/4e9acd0d-f477-455c-98d5-6e219b4de9de)
![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/07c53f6b-62e8-45ce-bce0-8a40d45fc414)

Question 3:
*	What is the average price of a home for each year built that have 3 bedrooms, 3 bathrooms, with two floors, and are greater than or equal to 2,000 square feet rounded to two decimal places?
![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/2b641f02-cf33-446f-bf02-d89b72bff411)
![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/997f6fe9-373f-4000-bc4f-101ea4957924)

