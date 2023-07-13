
# 🏠 SparkSQL: Home Sales Data Exploration 🎇

The provided code is a Python script that uses SparkSQL to analyze home sales data. It performs various operations such as reading data from a CSV file, creating temporary views, executing SQL queries, caching and uncaching tables, and working with parquet formatted data. Here's a breakdown of the script:

### Set up the environment:

It sets the Spark version and installs Spark and Java dependencies.

It imports the necessary packages and initializes SparkSession.

### Read the data:

The script reads home sales data from an AWS S3 bucket into a DataFrame.

The DataFrame is displayed using the show() method.

### Create a temporary view:

The DataFrame is registered as a temporary view named "home_sales".

### Calculate the average price for four-bedroom houses sold each year:

A SQL query is executed using SparkSQL to calculate the average price for four-bedroom houses sold in each year.

The result is displayed using the show() method.

### Calculate the average price for homes with three bedrooms and three bathrooms, grouped by the year built:

Another SQL query is executed to calculate the average price for homes with three bedrooms and three bathrooms, grouped by the year built.

The result is displayed using the show() method.

### Calculate the average price for homes with three bedrooms, three bathrooms, two floors, and a minimum size of 2,000 square feet, grouped by the year built:

A SQL query is executed to calculate the average price for homes with specific criteria, grouped by the year built.

The result is displayed using the show() method.

### Calculate the average view rating for homes with an average price greater than or equal to $350,000:

A SQL query is executed to calculate the average view rating for homes with an average price above a certain threshold.

The result is displayed using the show() method.

The query execution time is measured using time.time().

### Cache the temporary table:

The temporary table "home_sales" is cached using the cache table SQL command.

### Check if the table is cached:

The isCached method is used to check if the "home_sales" table is cached.

### Re-run the query on the cached data:

The same query from Step 7 is executed again on the cached table.

The result is displayed, and the query execution time is measured.

### Partition and write the DataFrame in parquet format:

The DataFrame is partitioned by the "date_built" field and written to disk in parquet format.

### Read the parquet formatted data:

The parquet data is read into a DataFrame named "p_df".

### Create a temporary view for the parquet data:

The DataFrame "p_df" is registered as a temporary view named "home_sales_parquet".

### Re-run the query on the parquet data:

The same query from Step 7 is executed on the parquet data.

The result is displayed, and the query execution time is measured.

### Uncache the temporary table:

The temporary table "home_sales" is uncached using the uncache table SQL command.

### Check if the table is no longer cached:

The isCached method is used to verify that the "home_sales" table is no longer cached.

### Stop the SparkSession:

The SparkSession is stopped to release resources.
