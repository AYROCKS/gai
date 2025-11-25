Here you go Atharv — **super simple, clean, exam-friendly pseudocode** for all labs.
Each block is **short**, **easy**, and looks perfect in practicals.
No unnecessary complexity.

---

# ✅ **1. Structured / Semi-structured / Unstructured Data + Ingest CSV & API**

### **Pseudocode**

```
# Load CSV File
import pandas as pd
data_csv = read_csv("data.csv")

# Load JSON (Semi-Structured)
data_json = read_json("data.json")

# Load Unstructured (text file)
file = open("notes.txt")
text_data = file.read()

# Fetch data from API
import requests
response = GET("https://api.example.com/data")
api_data = convert_json(response)

# Display samples
print(head(data_csv))
print(head(data_json))
print(first_100_chars(text_data))
print(head(api_data))
```

---

# ✅ **2. Data Cleaning (Missing values, rename cols, type change, join)**

### **Pseudocode**

```
import pandas as pd

data = read_csv("data.csv")

# Handle missing values
data.fillna("Unknown")
data.dropna()

# Rename columns
data.rename({"old_name": "new_name"})

# Change data types
data["age"] = data["age"].astype(int)

# Load second dataset
data2 = read_csv("data2.csv")

# Join datasets
merged = merge(data, data2, on="id")

print(merged)
```

---

# ✅ **3. Data Profiling + Feature Engineering**

### **Pseudocode**

```
data = read_csv("data.csv")

# Basic Profiling
print(data.shape)
print(data.info())
print(data.describe())

# Feature Selection
selected = data[["age", "income", "gender"]]

# Encoding categorical
from sklearn.preprocessing import LabelEncoder
encoder = LabelEncoder()
data["gender_encoded"] = encoder.fit_transform(data["gender"])

# Scaling features
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
data_scaled = scaler.fit_transform(data[["age","income"]])
```

---

# ✅ **4. Exploratory Data Analysis (EDA)**

### **Pseudocode**

```
import matplotlib.pyplot as plt
import seaborn as sns

data = read_csv("data.csv")

# Histogram
plt.hist(data["age"])

# Boxplot
sns.boxplot(x=data["income"])

# Pair plot
sns.pairplot(data)

# Heatmap
sns.heatmap(data.corr())
```

---

# ✅ **5. Build an ETL Pipeline (Extract → Transform → Load)**

### **Pseudocode**

```
# Extract
csv_data = read_csv("input.csv")
api_data = GET("https://api.example.com/users")
api_data = json_to_dataframe(api_data)

# Transform
cleaned = csv_data.dropna()
cleaned["age"] = cleaned["age"].astype(int)

# Combine both datasets
final = concatenate(cleaned, api_data)

# Load to CSV
final.to_csv("output.csv")

# Load to SQLite
import sqlite3
conn = connect("database.db")
final.to_sql("users_table", conn)
```

---

# ✅ **6. Power BI — Import + Dashboard**

*(Power BI has no code, so pseudocode style)*

### **Pseudocode Steps**

```
Open Power BI Desktop
Load data → "Import Data" → choose CSV dataset
Clean data using Power Query:
    - Remove nulls
    - Change data types
Create Visuals:
    - Bar chart → Sales by Category
    - Pie chart → Sales by Region
    - Map → Customer locations
Add Filters:
    - Slicer for Year
    - Slicer for Product Type
Save Dashboard
```

---

# ✅ **7. Data Warehouse vs Data Lake vs Lakehouse Simulation**

### **Pseudocode**

```
data = read_csv("dataset.csv")

# Save to Warehouse (Structured → SQL Table)
save_to_sql("warehouse.db", table="sales", data)

# Save to Data Lake (Raw files)
save_as("lake/sales_raw.csv", data)

# Save to Lakehouse (Parquet format)
save_as_parquet("lakehouse/sales.parquet", data)

# Comparison report (short)
print("Warehouse = structured, schema-on-write")
print("Lake = raw data, schema-on-read")
print("Lakehouse = mix of both, supports BI + ML")
```

---

# 🟢 Done!

If you want, I can convert this into **Notion format**, **PDF**, or **exam-ready handwritten style**.
