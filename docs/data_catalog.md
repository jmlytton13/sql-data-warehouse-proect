# Data Dictionary for Gold Layer
## Overview
The Gold Layer is the business-level data representation, structured to support analytical and reporting use cases. It consists of **dimension tables** and **fact tables** for specific metrics.

---

### 1. gold.dim_customers
- **Purpose:** Stores customer details enriched with demographic and geographic data
- **Columns:**

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| customer_key | INT | Surrogate key uniqiely identifying each customer record in the customer dimension table. |
| customer_id | INT | Unique numerical identifier assigned to each customer |
| customer_number | NVARCHAR(50) | Alphanumeric identifier representing the customer, used for tracking and referencing |
| first_name | NVARCHAR(50) | Customer's first name, as recorded in the system |
| last_name | NVARCHAR(50) | Customer's last name or family name |
| country | NVARCHAR(50) | Customer's country of residence (e.g. 'Australia') |
| marital_status | NVARCHAR(50) | Customer's marital status (e.g. 'Married', 'Single') |
| gender | NVARCHAR(10) | Customer's gender (e.g. 'Male', 'Female', 'n/a' |
| birthdate | DATE | Customer's date of birth, formatted as YYYY-MM-DD (e.g. 1971-10-06) |
| create_date | DATE | Date and time when the customer's record was created in the system |

---

### 2. gold.dim_products
- **Purpose:** Provides information about the products and their attributes
- **Columns:**

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| product_key | INT | Surrogate key uniquely identifying each product record in the product dimension table. |
| product_id | INT | Unique numerical identifier assigned to each product |
| product_number | NVARCHAR(50) | Alphanumeric identifier representing the product, used for categorization or inventory |
| product_name | NVARCHAR(50) | Descriptive name of the product, including details such as type, color, size |
| category_id | NVARCHAR(50) | Identifier for product's category, linking to its high-level classification |
| category | NVARCHAR(50) | Broader classification of the product (e.g. Bikes, Components) to group related items |
| subcategory | NVARCHAR(50) | More detailed classification of the product within the category, such as product type |
| maintenance | NVARCHAR(10) | Indicates whether the product requires maintenance (e.g. 'Yes', 'No') |
| cost | INT | Cost or base price of the product, measured in monetary units |
| product_line | NVARCHAR(10) | Specific product line or series to which the product belongs (e.g. 'Road', 'Mountain') |
| start_date | DATE | Date when the product became available for sale or use |

---


### 3. gold.fact_sales
