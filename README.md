# Customer-Behavior-Analysis
End-to-end analysis of customer shopping behavior using Python, SQL, and Power BI.

# Customer Behavior Analysis Project

This is an end-to-end data analysis project that explores a customer shopping behavior dataset. The project involves cleaning data with Python, storing it in a MySQL database, analyzing it with SQL, and visualizing insights in a Power BI dashboard.

## 🏁 Final Dashboard

Here is a preview of the final Power BI dashboard.

![Customer Behavior Dashboard](dashboard/dashboard_preview.png)

---

## 🛠️ Tools Used

* **Data Cleaning:** Python (Pandas, NumPy)
* **Database:** MySQL
* **Data Analysis:** SQL
* **Data Visualization:** Power BI
* **IDE:** Jupyter Notebook, MySQL Workbench

---

## Project Workflow

This project follows a 4-step process:

### 1. Data Cleaning and Preparation
* **File:** `notebook/1_Data_Cleaning_and_Database_Load.ipynb`
* Loaded the raw `customer_shopping_behavior.csv` file into a pandas DataFrame.
* Cleaned column names (lowercase, underscores).
* Handled missing values in `review_rating` by imputing the median rating by category.
* Engineered a new `age_group` column using quantile-based binning.
* Dropped the `promo_code_used` column as it was redundant with `discount_applied`.

### 2. Database Storage
* **File:** `notebook/1_Data_Cleaning_and_Database_Load.ipynb`
* Established a connection to a local MySQL server.
* Created a new database named `Project_1`.
* Loaded the cleaned pandas DataFrame into a new table named `customer` in the `Project_1` database using `df.to_sql()`.

### 3. SQL Analysis
* **File:** `sql/2_Customer_Analysis_Queries.sql`
* Answered 10 key business questions by writing SQL queries.
* Analysis includes:
    * Revenue by gender and age group.
    * Top 5 products by review rating.
    * Customer segmentation (New, Returning, Loyal).
    * Top 3 most purchased products within each category (using a Window Function).

### 4. Data Visualization
* **File:** `dashboard/Customer_Behavior.pbix`
* Connected Power BI directly to the `Project_1` MySQL database.
* Created an interactive dashboard to visualize the SQL query results and key metrics like average purchase amount, subscriber count, and revenue by category.

---

## How to Run This Project

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YourUsername/Customer-Behavior-Analysis.git](https://github.com/YourUsername/Customer-Behavior-Analysis.git)
    ```
2.  **Data Cleaning & DB Load:**
    * Ensure you have a local MySQL server running.
    * Update the `username`, `password`, and `host` variables in the `1_Data_Cleaning_and_Database_Load.ipynb` notebook.
    * Run the entire notebook to clean the data and load it into the `customer` table.
3.  **SQL Analysis:**
    * Run the queries in `2_Customer_Analysis_Queries.sql` against the `Project_1` database in MySQL Workbench or your preferred SQL tool.
4.  **View Dashboard:**
    * Open the `Customer_Behavior.pbix` file in Power BI Desktop.
    * You may need to refresh the data source and update credentials to connect to your local MySQL database.
