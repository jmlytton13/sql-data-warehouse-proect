# Data Dictionary for Gold Layer
## Overview
The Gold Layer is the business-level data representation, structured to support analytical and reporting use cases. It consists of **dimension tables** and **fact tables** for specific metrics.
---
### 1. gold.dim_customers
- **Purpose:** Stores customer details enriched with demographic and geographic data
- **Columns:**

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| customer_key | INT | Surrogate key uniqiely identifying each customer record in the dimension table. |
| customer_id | INT | Unique numerical identifier assigned to each customer |
| customer_number | VARCHAR(50) | Alphanumeric identifier representing the customer, used for tracking and referencing |
| first_name | VARCHAR(50) | Customer's first name, as recorded in the system |
| last_name | VARCHAR(50) | Customer's last name or family name |
| country | VARCHAR(50) | Customer's country of residence (e.g. 'Australia') |
| marital_status | VARCHAR(50) | Customer's marital status (e.g. 'Married', 'Single') |
| gender | VARCHAR(10) | Customer's gender (e.g. 'Male', 'Female', 'n/a' |
| birthdate | DATE | Customer's date of birth, formatted as YYYY-MM-DD (e.g. 1971-10-06) |
| create_date | DATE | Date and time when the customer's record was created in the system |

### 2. gold.dim_products


### 3. gold.fact_sales
