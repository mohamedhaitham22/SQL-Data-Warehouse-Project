# SQL Data Warehouse Project

This project implements a modern **three-tier data architecture** using SQL. It transforms raw data from business systems into a clean and structured format for reporting and analytics. The data flows through three layers: **Bronze, Silver, and Gold**, each with a specific purpose.

## 🏗️ Architecture Overview

The project follows a clear three-layer design:

- **Bronze Layer (Raw Data):**  
  This is the landing zone. It stores raw data directly from the source systems with almost no changes. This helps keep the original format for future reference.

- **Silver Layer (Cleaned Data):**  
  This layer cleans and validates the data. Business rules and data quality checks are applied. The data becomes more organized and easier to work with.

- **Gold Layer (Dimensional Model):**  
  This layer is used for reporting and analytics. The data is transformed into a **dimensional model** (star schema), which makes it easier for business users to analyze.

## 🔗 Data Sources

- **CRM System:**  
  Includes customer information, product details, and sales transactions.

- **ERP System:**  
  Provides extra customer data, location details, and product categories.

## 📊 Dimensional Model (Star Schema)

In the Gold layer, the data is modeled using a star schema with:

- **Fact Table:**  
  - `fact_sales` — Contains the business metrics such as sales amounts or quantities.

- **Dimension Tables:**  
  - `dim_customers` — Contains customer information (e.g., name, location).  
  - `dim_products` — Contains product details (e.g., name, category).

All tables are connected using **surrogate keys** for better performance and consistency.

## ⚙️ ETL Process Overview

The data pipeline uses ETL (Extract, Transform, Load) steps:

1. **Database and Schema Initialization**
2. **Table Creation for Each Layer**  
   (Bronze, Silver, Gold)
3. **Data Extraction** from source systems and loading into Bronze
4. **Data Transformation** and validation in Silver
5. **Dimensional Modeling** in Gold for analysis and reporting

## 📚 More Information

For detailed explanations of each layer and how the ETL process is done, please check the [Wiki](#) pages (or create wiki pages in the repo if not done yet).

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).  
You are free to use, modify, and distribute this project with proper credit.


