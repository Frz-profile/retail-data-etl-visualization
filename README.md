# 🛒 Retail Purchases Data Pipeline and Visualization

This project demonstrates a complete data pipeline—from raw CSV import to data quality validation and final visualization using Power BI.

## 📁 Project Structure

.
├── PurchasesFINAL12312016.csv            # Raw purchase transaction data
├── csv_to_MySQL.py                       # Python script to load CSV into MySQL
├── DataQualityCheck.sql                  # SQL queries to validate and explore data
└── PowerBI_DataVisualisation.pbix        # Power BI dashboard for data visualization

## 🔍 Project Objective

To transform raw retail purchase data into actionable insights by:
- Loading and structuring data in a MySQL database
- Validating and summarizing key metrics using SQL
- Visualizing store, brand, and classification performance in Power BI

## 🛠️ Technologies Used

- **Python** (`pandas`, `mysql-connector-python`)
- **MySQL**
- **SQL**
- **Power BI**

## 📌 Key Features

- Automated CSV import to MySQL with dynamic column detection
- SQL checks for:
  - Row counts
  - Null values
  - Aggregated metrics by store, brand, and classification
- Power BI dashboard to visualize:
  - Sales performance
  - Vendor contribution
  - Product classification trends

## 🧪 How to Use

1. **Prepare MySQL database**
   - Create a database named `sample_purchases_pwc`
   - Update MySQL credentials in `csv_to_MySQL.py`

2. **Run the Python script**
   ```bash
   python csv_to_MySQL.py
