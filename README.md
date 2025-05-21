# 🛒 Power BI Retail Purchases Data Pipeline and Visualization

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

1. **Prepare the MySQL Database**
   - Create a database named `sample_purchases_pwc`.
   - Update the MySQL credentials and CSV path in `csv_to_MySQL.py`.

2. **Import the CSV into MySQL**
   - Run the Python script to load the CSV into a new table:
     ```bash
     python csv_to_MySQL.py
     ```
   - The script dynamically creates a table (`sales_data`) and populates it with all records from the CSV file.

3. **Validate and Explore the Data**
   - Open `DataQualityCheck.sql` in MySQL Workbench (or any SQL client).
   - This script includes:
     - Total row count checks
     - Sample record views
     - Null/missing value analysis on key fields
     - Aggregated metrics grouped by `Store`, `Brand`, and `Classification` to prepare for visualization

4. **Visualize Insights in Power BI**
   - Open `PowerBI_DataVisualisation.pbix`.
   - Connect it to the MySQL database/table (`sales_data` or `samplepurchase`, depending on what you named it).
   - The dashboard includes:
     - Store-level and brand-level performance views
     - Purchase value summaries
     - Vendor distribution and classification breakdowns

## 📈 Sample Data Columns

- `InventoryId`, `Store`, `Brand`, `Description`, `Size`, `VendorNumber`, `VendorName`
- `PONumber`, `PODate`, `ReceivingDate`, `InvoiceDate`, `PayDate`
- `PurchasePrice`, `Quantity`, `Dollars`, `Classification`

## 🔮 Future Improvements

- Add automated data profiling or anomaly detection
- Schedule periodic ETL with Airflow or Prefect
- Publish Power BI to Power BI Service with auto-refresh
