# ✈️ Airlines Data Analysis — Large-Scale PySpark Processing (118M+ Records)

This project analyzes 22 years of US domestic flight data (1987–2008) using **PySpark**, processing over **118 million records** to uncover trends in flight traffic, cancellations, and airline performance.

It demonstrates how to handle **large-scale data processing, optimization, and distributed analytics** using the Spark ecosystem.

---

## 📊 Problem Statement

Analyzing decades of flight data involves:
- Massive datasets exceeding local memory limits  
- Complex aggregations across time and routes  
- Data quality challenges (missing values, cancellations)

This project aims to:
- Build a scalable data processing pipeline using PySpark  
- Analyze airline performance and cancellation trends  
- Identify high-traffic routes and travel patterns  

---

## ⚙️ Tech Stack

**Language:** Python  
**Engine:** PySpark (Spark SQL, DataFrames)  
**Visualization:** Pandas, Matplotlib, Seaborn  
**Environment:** Jupyter Notebook  

---

## 🚀 Data Engineering Workflow

### 🔹 1. Large-Scale Data Ingestion

- Ingested **22 years of CSV data (1987–2008)**  
- Used `glob` + `unionByName()` to merge datasets  
- Created a unified Spark DataFrame:

👉 **118,914,458 rows × 29 columns**

---

### 🔹 2. Data Cleaning & Optimization

- **Column Pruning**
  - Removed 18 unnecessary columns (TaxiIn, TaxiOut, CancellationCode, etc.)
  - Reduced memory usage and improved performance  

- **Missing Value Handling**
  - Removed canceled flights  
  - Dropped null values using `na.drop()`  

👉 Result: Clean, optimized dataset for analysis  

---

### 🔹 3. Distributed Data Processing

- Performed aggregations using Spark DataFrames  
- Leveraged distributed computation for:
  - Route-level traffic analysis  
  - Time-based trends (Year, Month, DayOfWeek)  
  - Carrier performance evaluation  

---

## 📈 Key Analysis & Insights

### ✈️ High-Traffic Routes

- Identified busiest flight routes:
  - **SFO ↔ LAX**
  - Major hubs: ORD, ATL, LAX  

👉 Consistent high-volume corridors across years  

---

### 📅 Temporal Trends

- Analyzed traffic patterns across:
  - Years  
  - Months  
  - Days of the week  

👉 Identified peak travel periods and seasonal trends  

---

### ⚠️ Cancellation Analysis

- Aggregated cancellation rates by **airline (Unique Carrier)**  
- Identified carriers with higher operational disruptions  

👉 Provided insights into airline reliability  

---

## 📊 Visual Insights

- 📊 Pie Charts → Cancellation distribution by airline  
- 📊 Bar Charts → Traffic trends (yearly, monthly)  
- 📊 Route Analysis → Top 10 busiest flight paths  

---

## 📂 Repository Structure

```bash
Airlines-Data-Analysis/
├── bigdata.py.ipynb              # PySpark data pipeline & analysis
├── ALY6110_Final_project.docx   # Detailed report and findings
