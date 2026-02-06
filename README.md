# Hotel-Analytics-Pipeline
End-to-end hotel analytics pipeline built with Databricks and PySpark, including Bronze → Silver → Gold layers, KPI calculation, and data quality/drift monitoring.


## Setup Instructions

### 1. Run on Databricks CE

1. Upload the project folder to **Databricks Repos**
2. Create a cluster
3. Run notebooks **in order**:
   - `01_bronze_ingestion`
   - `02_silver_cleaning`
   - `03_gold_kpis`
   - `04_data_quality_drift_monitoring`
4. All tables are written as **Delta tables**:
   - `hotel_bronze.bookings_raw`
   - `hotel_silver.bookings_clean`
   - `hotel_gold.daily_kpis`
   - `hotel_monitoring.data_quality_results`

### 2. Run Locally (PySpark)

1. Install dependencies:

```bash
pip install pyspark pandas mlflow
