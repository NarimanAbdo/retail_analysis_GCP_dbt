## 📊 Retail Data Warehouse Project on GCP with dbt

This project sets up a modern data warehouse using **Google BigQuery** and **dbt Cloud** for managing and transforming retail data.

### ✅ Project Setup Summary

- A new BigQuery **dataset `retail`** was created to hold all dimension and fact tables.
- Tables were manually created using BigQuery SQL and filled with **synthetic data** using `UNNEST(GENERATE_ARRAY(...))` to simulate:
  - `dim_customers`
  - `dim_products`
  - `dim_stores`
  - `dim_employees`
  - `dim_time`
  - `fact_sales`
  - `fact_inventory`

### 🛠 dbt Cloud Configuration

- Connected dbt Cloud to BigQuery using a **service account key (JSON)** with appropriate IAM roles.
- Defined a source YAML file to connect to the raw tables in BigQuery:
  ```yaml
  sources:
    - name: retail
      database: itiproject-465310
      schema: retail
      tables:
        - name: dim_customers
        - name: dim_employees
        - name: dim_products
        - name: dim_stores
        - name: dim_time
        - name: fact_sales
        - name: fact_inventory
