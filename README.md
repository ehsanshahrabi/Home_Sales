
# 🏠 SparkSQL: Home Sales Data Exploration 🎇

## 🎢 Journey Itinerary

### 1️⃣ 🛠️ Environment Setup

Our adventure begins by configuring the necessary environment variables for Spark. The script automatically installs Spark and initializes a SparkSession, the entry point to any Spark functionality.

### 2️⃣ 📦 Data Loading

The script pulls in a dataset residing in an AWS S3 bucket and loads it into a DataFrame, which is essentially a distributed collection of data neatly organized into named columns.

### 3️⃣ 🖼️ Temporary View Creation

To employ SQL operations on our DataFrame, the script creates a temporary view. This temporary view allows the application of SQL-based perspectives on the data.

### 4️⃣ 📊 Data Analysis

With the power of SQL operations, the script embarks on answering intriguing questions about the average prices of houses. It dives into determining the average price for four-bedroom houses sold each year (rounded to two decimal places) and houses that were built with 3 bedrooms and 3 bathrooms.

### 5️⃣ 🏘️ Advanced Home Analysis

The script further refines the data analysis by focusing on the average price of homes that have specific attributes - three bedrooms, three bathrooms, two floors, and a size of at least 2,000 square feet.

### 6️⃣ 👁️ View Ratings and Performance Measurement

The script evaluates the 'view' rating for the average price of a home, where the homes are valued at $350,000 or higher. Simultaneously, it tracks the runtime for this operation, providing a real-time performance measure.

### 7️⃣ 🚀 Data Caching

To increase the efficiency of data operations, the script caches the 'home_sales' temporary table. Caching results in faster queries, especially noticeable in repeated data access scenarios.

### 8️⃣ 🕵️ Cache Verification

The script verifies if the table 'home_sales' is successfully cached, ensuring the efficiency of subsequent operations.

### 9️⃣ 🔄 Cached Query Execution and Runtime Comparison

With the cached data, the script reruns the query about 'view' ratings and average price, and once again tracks its runtime. This allows for a comparison of performance before and after caching.

### 🔟 🔲 Data Partitioning and Formatting

The script demonstrates the use of partitioning and Parquet formatting for optimization. It partitions the DataFrame by the 'date_built' field and writes it in Parquet format.

### 1️⃣1️⃣ 📂 Parquet Data Loading

Bringing the Parquet formatted data back into the scenario, the script loads it into a new DataFrame, preparing for further operations.

### 1️⃣2️⃣ 🏢 Temporary View Creation for Parquet Data

With the loaded Parquet data, a new temporary view is created, paving the way for SQL operations on this optimized data.

### 1️⃣3️⃣ 📈 Parquet Data Analysis and Performance Measurement

The script performs SQL operations on the Parquet DataFrame and measures its runtime, facilitating a comparison with the cached version's performance.

### 1️⃣4️⃣ 💨 Uncaching

The script concludes the caching process by uncaching the 'home_sales' temporary table, ensuring a clean wrap-up of the caching procedure.

### 1️⃣5️⃣ 🔍 Cache State Verification

Finally, the script checks if the 'home_sales' table has been correctly uncached.
