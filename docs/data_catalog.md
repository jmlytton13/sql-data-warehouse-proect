# Data Dictionary for Gold Layer
## Overview
The Gold Layer is the business-level data representation, structured to support analytical and reporting use cases. It consists of **dimension tables** and **fact tables** for specific metrics.

1. gold.dim_customers
. Purpose: Stores customer details enriched with demographic and geographic data
. Columns:
| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| customer_key | INT | Surrogate key |
| customer_id | INT | CRM customer ID |
| customer_number | VARCHAR(50) | Business key |
| first_name | VARCHAR(50) | Customer first name |
| last_name | VARCHAR(50) | Customer last name |
| country | VARCHAR(50) | Customer country |
| gender | VARCHAR(10) | Customer gender |
| birthdate | DATE | Date of birth |
| create_date | DATE | Customer creation date |

2. gold.dim_products


3. gold.fact_sales
