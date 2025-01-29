
# SparkSQL Challenge  

## Table of Contents
- [Project Overview](#project-overview)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Features](#features)
- [Code Snippets](#code-snippets)
- [Acknowledgments](#acknowledgments)

---

## Project Overview  
This project utilizes SparkSQL to analyze home sales data and determine key metrics. It demonstrates the ability to create temporary views, partition data for optimized querying, and implement caching and uncaching operations to enhance performance. The goal of the project is to showcase how Spark can be used to efficiently handle large datasets and improve query performance through these operations. Key operations such as creating temporary views, partitioning data by columns, and verifying the uncaching of tables are performed as part of the analysis process.

---

## Technologies Used
- **Apache Spark**: For distributed data processing using SparkSQL.
- **PySpark**: Python library for Spark, used to interact with Spark SQL.
- **Jupyter Notebooks**: Used to run and test the project in an interactive Python environment.
- **Google Colab**: For executing the Jupyter Notebook in the cloud.

---

## Installation  
1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/username/sparksql-challenge.git ```

2. Open the Jupyter notebook file in Google Colab or a local Jupyter environment to run the code and view results.

## Features
- **SparkSQL Temporary Views**: Create and interact with temporary views in Spark.
- **Data Partitioning**: Use partitioning to optimize data handling.
- **Caching and Uncaching**: Cache tables to improve performance and uncash them when no longer needed.
- **Performance Verification**: Verify that the temporary table has been uncached correctly.

## Code Snippets
### Create Temporary View
This code creates a temporary view for the home sales data to run SQL queries against it.

```python
spark.sql("CREATE OR REPLACE TEMP VIEW home_sales AS SELECT * FROM home_sales_data")
```

### Data Partitioning
This snippet demonstrates partitioning the data by a specific column to optimize query performance.

``` python
home_sales_partitioned = home_sales_data.repartition("city")
```

### Caching and Uncaching
This code demonstrates caching and uncaching a Spark table.

```python
home_sales_data.cache()  # Cache the table for faster queries
home_sales_data.uncache()  # Uncache the table to free resources
```

## Acknowledgments
Special thanks to Xpert Learning Assistant for assistance debugging.
<br>
Dataset used in this project is sourced from the Rutgers Bootcamp Challenge 22 materials.

