# Home_Sales
UCI Data Analyst Module 22 - Big Data Module

# Home Sales Analysis with SparkSQL

This project leverages SparkSQL to analyze and calculate key metrics from home sales data. The project involves creating temporary views, partitioning data, caching, and uncaching tables, as well as comparing runtimes for optimized and non-optimized queries.

---

## Project Setup

### Repository
- **Repository Name:** `Home_Sales`
- This project should be stored in a new GitHub repository named `Home_Sales`. Do not add this project to an existing repository.
- Clone the repository to your local machine and push all changes to GitHub.

---

## Files
The following files are included to help you get started:
- `Home_Sales.ipynb`
- `home_sales_revised.csv`

Rename `Home_Sales_starter_code.ipynb` to `Home_Sales.ipynb` before beginning the project.

---

## Instructions

### Initial Setup
1. Import the necessary PySpark SQL functions.
2. Load the `home_sales_revised.csv` data into a Spark DataFrame.
3. Create a temporary table named `home_sales`.

### Analysis Using SparkSQL
Answer the following questions using SparkSQL:

1. **Average Price for Four-Bedroom Houses (By Year Built)**  
   - Calculate the average price of four-bedroom houses sold for each year.
   - Round the results to two decimal places.

2. **Average Price of Three-Bedroom, Three-Bathroom Houses (By Year Built)**  
   - Calculate the average price of houses with three bedrooms and three bathrooms for each year the house was built.
   - Round the results to two decimal places.

3. **Average Price of Specific Houses (By Year Built)**  
   - Calculate the average price of houses with:
     - Three bedrooms
     - Three bathrooms
     - Two floors
     - Size ≥ 2,000 square feet
   - Round the results to two decimal places.

4. **Average Price Per "View" Rating**  
   - Calculate the average price of houses per "view" rating where the average home price is ≥ $350,000.
   - Round the results to two decimal places.
   - Determine the runtime for this query.

### Data Optimization and Comparison
1. **Cache the `home_sales` Temporary Table**
   - Cache the `home_sales` table and verify its status.
   - Re-run the query for average price per "view" rating and compare runtime with the uncached version.

2. **Partition the Data**
   - Partition the home sales data by the `date_built` field and save it in parquet format.
   - Create a temporary table from the parquet data.
   - Re-run the query for average price per "view" rating and compare runtime with the uncached version.

3. **Uncache the Table**
   - Uncache the `home_sales` temporary table.
   - Verify that the table is no longer cached.

---
