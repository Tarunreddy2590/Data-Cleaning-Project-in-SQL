# 📊 Data Cleaning Projects in SQL

This project demonstrates practical data cleaning techniques using **MySQL**, focusing on transforming raw, messy data into a clean and usable format. It covers common real-world issues such as duplicates, inconsistent formats, null values, and unnecessary columns.

---

## 📁 Project Structure


---

## 🧹 Cleaning Tasks Performed

### ✅ 1. **Removed Duplicates**
- Used `ROW_NUMBER()` with `PARTITION BY` on all columns to identify duplicate rows.
- Deleted rows where row number > 1.

```sql
SELECT *, 
       ROW_NUMBER() OVER (PARTITION BY col1, col2, col3, ...) AS rn
FROM raw_table;
