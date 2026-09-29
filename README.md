# 🐼 Pandas Study & Practice Guide

Welcome to the **Pandas Study Repository**! This repository serves as a hands-on learning collection covering fundamental to intermediate data manipulation and analysis operations using Python's `pandas` library.

---

## 📁 Repository Contents & Topics Covered

The practice scripts and notebooks in this repository cover the following key Pandas workflows:

| Topic / Category | Description & Methods Covered |
| :--- | :--- |
| **1. Dataset Inspection & Exploration** | `pd.read_csv()`, `df.head()`, `df.tail()`, `df.info()`, `df.describe()`, `df.shape`, `df.columns` |
| **2. Data Selection & Filtering** | Column selection (`df['col']`, `df[['col1', 'col2']]`), conditional filtering (`df[df['Salary'] > 40000]`) |
| **3. Adding & Inserting Columns** | Vectorized operations (`df['Bonus'] = df['Salary'] * 0.1`), targeted insertion (`df.insert()`) |
| **4. Updating Data** | Label-based indexing (`df.loc[row, col]`), bulk transformation (`df['col'] = df['col'] * 1.10`) |
| **5. Removing Columns** | Column deletion (`df.drop(columns=[...], inplace=True)`) |
| **6. Missing Data Handling** | Checking nulls (`df.isnull()`, `df.isnull().sum()`), filling missing values (`df.fillna()`), row deletion (`df.dropna()`) |
| **7. Data Interpolation** | Missing value estimation using linear interpolation (`df['col'].interpolate(method='linear')`) |
| **8. Sorting Data** | Ordering rows by column values (`df.sort_values(by='col', ascending=True)`) |
| **9. Aggregation & Summarization** | Summary metrics (`.mean()`, `.sum()`, `.min()`, `.max()`) |
| **10. Grouping Data** | Single & multi-column grouping (`df.groupby(['col1', 'col2'])['col3'].sum()`) |
| **11. Merging & Joining** | Combining datasets with relational keys using SQL-style joins (`pd.merge(..., how='inner')`) |

---

## 🚀 Quick Reference & Code Examples

### 1. Data Loading & Exploration
```python
import pandas as pd

# Load dataset with custom encoding
df = pd.read_csv('sales_data_sample.csv', encoding='ISO-8859-1')

# Quick inspection
print("Shape:", df.shape)
print("Columns:", df.columns)
display(df.head(5))
display(df.info())
print(df.describe())
