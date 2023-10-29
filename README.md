# Home_Sales
Module 22 Challenge - Big Data

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

Question 4:
*	What is the "view" rating for the average price of a home, rounded to two decimal places, where the homes are greater than or equal to $350,000? Although this is a small dataset, determine the run time for this query.
![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/cf26b5d2-405e-4f02-be74-06a8e8d03821)
![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/bfb0aaa7-0488-4870-ab7f-523b57068ba0)

Next step was to cache the temporary table and re-run query 4 to compare running times

![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/3a82f158-3076-4236-8136-35c41ad6624a)


Final step was to partition the home sales data by the date_built field and re-run query 4 to compare running times

![image](https://github.com/CRGMBC/Home_Sales/assets/134125287/231ff294-c910-4c86-9fcb-ed6c2533092f)

Timing comparison between original data, cached data and parquet formatted data:

* Original data


* Cached data


* Parquet formatted data



Based on the runtime results, it's evident that both the cached data and the Parquet formatted data have faster runtimes compared to the original data. This can be attributed to the optimizations and benefits offered by caching and using the Parquet data format.

# Conclusion
Caching the data, as performed in your code, stores the data in memory. When you query the cached data, it can be retrieved directly from memory, eliminating the need for reading the data from disk.

Parquet is a columnar storage format specifically designed for efficient data processing. Parquet organises the data into columns, which allows queries to skip irrelevant columns and partitions during query execution.

Parquet formatted data demonstrates the best runtime among the three options. This can be attributed to its optimized storage format, efficient compression, and the ability to leverage columnar optimisations during query execution. By utilizing Parquet, you can achieve faster query performance, reduced storage requirements, and improved overall data processing efficiency.
  
