# 📘 Data Modeler Project – Power BI Star Schema Design

A complete Power BI modeling project demonstrating **Star Schema**, **fact/dimension modeling**, **inactive relationships**, **hierarchies**, and **data cleaning**.

---

# 📸 Project Screenshots

### **📊 Sales by Category / Region**

[Click here to open output
](https://github.com/DharmikPansuriya00/all-ss/blob/main/Screenshot%202025-12-11%20164949.png)


---

### **🔁 Returns by Fiscal Year**

*(Included inside the same screenshot above – return matrix visible)*

---

### **💰 Revenue by Customer Segment**

*(Included inside the same screenshot above – revenue matrix visible)*

---

### **🧩 Full Data Model Diagram**

![Data Model](attachment:6a80214f-df5e-4826-9c8b-19835b22e094.png)

---

# 📌 Project Objective

Build an optimized **Star Schema data model** in Power BI using multiple fact and dimension tables.

🎯 Key Skills Covered:

* ⭐ Star Schema Design
* 🔗 Relationship Management
* 🧠 Cardinality & Filter Flow
* ⏳ Inactive Relationship Handling
* 🧱 Fact vs. Dimension Tables
* 🗂 Hierarchies & Data Categorization
* ⚙ Best Modeling Practices

---

# 📂 Dataset Summary

| File                  | Description                                   |
| --------------------- | --------------------------------------------- |
| **Sales_Fact.xlsx**   | Main fact table (Quantity, Revenue, Discount) |
| **Customer_Dim.xlsx** | Customer demographic & segment data           |
| **Product_Dim.xlsx**  | Product details: Category, Subcategory, Brand |
| **Region_Dim.xlsx**   | Location hierarchy: Country → State → City    |
| **Date_Dim.xlsx**     | Calendar + Fiscal year attributes             |
| **Returns_Fact.xlsx** | Return transactions & reasons                 |

---

# 🧪 Power Query Transformations

✔ Removed blank/duplicate rows
✔ Applied correct data types (Whole Number, Text, Date, Currency)
✔ Verified unique primary keys
✔ Cleaned column names
✔ Loaded tables to Model View

---

# 🌐 Data Model Architecture

### **⭐ Central Fact Table**

* **Sales_Fact**

### **🔹 Dimension Tables**

* Customer_Dim
* Product_Dim
* Region_Dim
* Date_Dim

### **🔸 Secondary Fact Table**

* **Returns_Fact** (connected to Sales_Fact & Date_Dim)

---

# 🔗 Relationship Summary

| From         | To           | Key           | Type | Filter Direction |
| ------------ | ------------ | ------------- | ---- | ---------------- |
| Sales_Fact   | Customer_Dim | CustomerID    | 1:*  | Single           |
| Sales_Fact   | Product_Dim  | ProductID     | 1:*  | Single           |
| Sales_Fact   | Region_Dim   | RegionID      | 1:*  | Single           |
| Sales_Fact   | Date_Dim     | DateKey       | 1:*  | Single           |
| Returns_Fact | Sales_Fact   | SalesID       | *:1  | Single           |
| Returns_Fact | Date_Dim     | ReturnDateKey | *:1  | **Inactive** ⭐   |

🔄 **All relationships are single-direction** (best practice).
⭐ Inactive relationship used for ReturnDateKey → DateDim.

---

# 📦 Hierarchies

### 📅 **Date Hierarchy**

* Year → Quarter → Month → Date

### 🌍 **Region Hierarchy**

* Country → State → City

### 📦 **Product Hierarchy**

* Category → Subcategory → Product Name

---

# 📊 Verification Visuals

✔ Sales by **Product Category → Region**
✔ Returns grouped by **Fiscal Year**
✔ Revenue by **Customer Segment**

These matrices validate that dimension filters flow correctly across fact tables.

---

# 📁 Deliverables

* ✔ **Power BI .pbix file** (cleaned tables + modeling + visuals)
* ✔ **README documentation** (this file)
* ✔ Optional: Summary in **.txt/.docx** format

---

# 🎉 Final Notes

This project demonstrates mastery of:

* Dimensional modeling
* Star & Snowflake architecture
* Complex relationships
* Clean ETL practices
* Professional data modeling in Power BI

If you want this README **converted to PDF, DOCX, or GitHub Markdown with auto-upload instructions**, just tell me!
