# End-to-End BMW Sales Analysis (Python, SQL, Power BI)

> **Note:** View a summary of this project and the final dashboard on my [**LinkedIn Post**](https://www.linkedin.com/posts/pgudilshan_dataanalytics-portfolioproject-powerbi-activity-7388877493925076992-TScB?utm_source=share&utm_medium=member_desktop&rcm=ACoAAF-q3BUBsl-DjW0ndOchJC_uNQMSfqYydL0).

This project demonstrates a complete end-to-end data analysis workflow using a dataset of BMW worldwide sales records from 2010-2024 (sourced from Kaggle). The goal was to practice using multiple core data analysis tools together to extract insights and create a final visualization.

---

## 🛠️ Tools Used

* **Python:**
    * **Pandas:** For data loading, cleaning, manipulation, and initial analysis (EDA).
    * **Matplotlib & Seaborn:** For exploratory visualizations within the Jupyter Notebook.
    * **sqlite3:** To create and query an SQLite database from the cleaned data.
* **SQL:** To query the SQLite database and prepare aggregated data for visualization.
* **Power BI:** To build the final interactive dashboard.
* **Jupyter Notebook:** As the primary development environment.

---

## 📊 Analysis Process

1.  **Data Loading & Cleaning (Python/Pandas):** Loaded the 50,000-row CSV dataset. Checked for missing values and duplicates (found none). Explored data types and unique values.
2.  **Exploratory Data Analysis (EDA) (Python/Pandas & Matplotlib):** Analyzed trends and patterns, including:
    * Sales Volume over Years (Line Chart).
    * Sales Volume by Region (Bar Chart).
    * Top 10 Selling Models (Bar Chart).
    * Price vs. Sales Volume (Scatter & Hexbin Plots).
    * Sales Volume by Fuel Type (Bar Chart).
    * Sales Volume by Region & Fuel Type (Heatmap).
3.  **Database Creation & SQL Querying (Python/sqlite3 & SQL):**
    * Saved the cleaned Pandas DataFrame into an `.sqlite` database file.
    * Practiced writing `SQL` queries (using `GROUP BY`, `SUM`, `AVG`, `ORDER BY`) within Python to extract aggregated data needed for the dashboard.
4.  **Data Preparation for BI (Python/Pandas):** Executed a final SQL query to get data grouped by Year, Region, and Model, then saved this aggregated data to a new CSV (`bmw_analysis_for_bi.csv`).
5.  **Dashboard Creation (Power BI):** Imported the final CSV into Power BI and built an interactive dashboard featuring key charts and slicers (Year, Region).

---

## 💡 Key Findings

* **Overall Trend:** BMW sales volume generally increased from 2010 to 2024, with a significant peak in **2022**.
* **Top Region:** **Asia** showed the highest total sales volume.
* **Top Model:** The **7 Series** was the best-selling model overall during this period.
* **Price vs. Sales:** No strong, simple correlation was found between Price and Sales Volume; sales occurred across the entire price range.
* **Fuel Type Impact:** Average sales volume was surprisingly **similar across all fuel types** (Petrol, Diesel, Hybrid, Electric).
* **Region-Fuel Interaction:** While most regions showed similar sales across fuel types, **Hybrid** vehicles had particularly high sales in **Asia**, and **Electric/Hybrid** showed strength in **North America**.

---

## 🏃 How to Run

1.  Clone this repository.
2.  Ensure you have Python, Pandas, Matplotlib, Seaborn, and Jupyter Notebook installed.
3.  Place the `BMW_sales_data_2010_2024.csv` file in the same directory.
4.  Run the `BMW.ipynb` Jupyter Notebook. This will perform the analysis, create the `bmw_sales.sqlite` database, and generate the `bmw_analysis_for_bi.csv` file.
5.  (Optional) Open the `bmw_analysis_for_bi.csv` file in Power BI or Tableau to recreate the dashboard.
