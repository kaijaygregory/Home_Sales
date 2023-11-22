# __Home_Sales__

__Home Sales Data Analysis with SparkSQL__

This project involves using SparkSQL to derive key metrics from home sales data. The tasks include creating temporary views, data partitioning, caching and uncaching tables, and evaluating performance differences between cached and uncached data.

__Environment__

__Google Colab:__ This project was developed using Google Colab for collaborative Python programming.

__Data Handling__

__Data Reading:__ To begin, I read the home_sales_revised.csv data into a Spark DataFrame and created a temporary table named home_sales using Spark.

__Used SparkSQL To Answer The Following Questions__

__Question 1:__ Determined the average price for a four-bedroom house sold each year, rounded to two decimal places.

__Question 2:__ Found the average price of a home for each year it was built with three bedrooms and three bathrooms, rounded to two decimal places.

__Question 3:__ Calculated the average price of a home each year with specific criteria (3 bedrooms, 3 bathrooms, 2 floors, >= 2,000 sq. ft.), rounded to two decimal places.

__Question 4:__ Derived the "view" rating for homes costing >= $350,000. Record the query runtime rounded to two decimal places.

__Caching and Performance Analysis__

__Cache Table:__ Cached the temporary table home_sales.
__Check Cache:__ Verified if home_sales is cached.
__Cached Query:__ Ran a query using cached data. Filtered view ratings with an average price >= $350,000. Recorded runtime to compare to  uncached runtime.

__Data Partitioning and Further Analysis__

__Partition Data:__ Partitioned the formatted parquet home sales data by the "date_built" field.
__Parquet Temporary Table:__ Created a temporary table for the parquet data.
__Query Performance:__ Ran a query filtering view ratings with an average price >= $350,000 on the parquet data. Recorded runtime to compare to uncached runtime.

__Uncaching and Verification__
__Uncache Table:__ Uncached the home_sales temporary table.
__Verification:__ Verified the uncaching of the home_sales temporary table using PySpark.
