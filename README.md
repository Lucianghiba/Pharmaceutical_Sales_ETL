# 🏥 Pharmaceutical Sales ETL Pipeline

## 📌 Project Overview
This project demonstrates an **ETL (Extract, Transform, Load) pipeline** for pharmaceutical drug sales data.  
The goal is to extract data from a **CSV file**, clean and transform it, and store it in an **SQLite database** for further analysis.

## 📊 Technologies Used
- **Python** (pandas, sqlite3, matplotlib)
- **SQLite** (for database storage)
- **Jupyter Notebook** (for development)
- **GitHub** (for version control & portfolio showcase)

## 🚀 ETL Process Breakdown
1️⃣ **Extract**: Load sales data from `Sample_Pharmaceutical_Drug_Sales.csv`.  
2️⃣ **Transform**:  
   - Convert `sale_date` to proper datetime format.  
   - Extract `year` from the `sale_date` column.  
   - Remove `$` sign from `revenue` and convert it to a float.  
3️⃣ **Load**: Store cleaned data into an **SQLite database (`pharma_sales.db`)**.  
4️⃣ **Analyze**:
   - Find **total revenue per year**.
   - Identify **top-selling drugs**.
   - Visualize **revenue trends over time**.

## 📂 Project Structure
```
Pharmaceutical_Sales_ETL/
│── data/
│   ├── Sample_Pharmaceutical_Drug_Sales.csv  # Raw dataset
│── scripts/
│   ├── etl_pipeline.ipynb  # Jupyter Notebook
│── README.md  # Project documentation
│── pharma_sales.db  # SQLite database
```

## 📈 Example Insights
### 🔹 **Total Revenue Per Year**
```sql
SELECT year, SUM(revenue) as total_revenue FROM pharma_sales GROUP BY year;
```
📌 This query helps track **yearly sales performance**.

### 🔹 **Top 5 Best-Selling Drugs**
```sql
SELECT drug_name, SUM(units_sold) as total_units
FROM pharma_sales
GROUP BY drug_name
ORDER BY total_units DESC
LIMIT 5;
```
📌 This query identifies the **top-performing drugs** in terms of sales.


## 🛠 How to Run the Project
1️⃣ **Clone this repo**:
   ```sh
   git clone https://github.com/Lucianghiba/Pharmaceutical_Sales_ETL.git
   ```
2️⃣ **Install dependencies**:
   ```sh
   pip install pandas sqlite3 matplotlib
   ```
3️⃣ **Run the Jupyter Notebook** (`Pharma_Sales_ETL_Pipeline.ipynb`) step by step.

## 🎯 Future Improvements
- Automate the ETL pipeline using **Apache Airflow**.
- Deploy it as an **API** for real-time data processing.
- Integrate with **cloud storage (AWS/Azure)**.

## 📬 Contact
If you have any questions or suggestions, feel free to reach out!  
📧 **ghibalucian9@yahoo.com**  
🔗 [Lucian Ghiba LinkedIn](https://www.linkedin.com/in/lucian-ghiba-34014a175)
