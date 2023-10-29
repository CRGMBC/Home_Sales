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


