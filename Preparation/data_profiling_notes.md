# Data Profiling Tools (Power Query)
> Focus: Identifying data quality issues before modeling.

In Power BI (Power Query), there are three main tools under the **View** tab to analyze data quality.

### 1. Column Quality
* **What it does:** Shows percentages of data in three categories: **Valid**, **Error**, and **Empty**.
* **Use Case:** Quickly identifying if an ID column has nulls or if a data type conversion (e.g., text to number) caused errors.

### 2. Column Distribution
* **What it does:** Displays a small bar chart at the top of each column showing data frequency. It highlights two key metrics:
    * **Distinct:** Total count of different values.
    * **Unique:** Count of values that appear exactly once.
* **Use Case:** Checking cardinality. For a Primary Key (PK), all values should be distinct.

### 3. Column Profile
* **What it does:** Provides a detailed statistical view at the bottom of the screen (Count, Min, Max, Average, Standard Deviation, etc.).
* **Use Case:** Analyzing data outliers, such as impossible dates (e.g., year 1900) or negative sales values that shouldn't exist.

---

### Pro Tip (Exam Trap: Profiling Status)
By default, Power Query performs profiling based on the **top 1000 rows**. If your error is on row 2000, it won't show up.
* **Solution:** Click the status bar at the bottom-left of Power Query ("Profiling based on top 1000 rows") and change it to **"Profiling based on entire dataset"**.
