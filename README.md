Data Modeler Project**

## **Objective**

Build a clean, normalized **Star Schema** data model in Power BI using multiple fact and dimension tables. All transformation is done in **Power Query** and all relationships in **Model View**.

---

## **Dataset Used**

* **Sales_Fact** (SalesID, CustomerID, ProductID, RegionID, DateKey, Qty, Revenue, Discount)
* **Customer_Dim** (CustomerID, FullName, Age, Gender, Segment)
* **Product_Dim** (ProductID, ProductName, Category, Subcategory, Brand)
* **Region_Dim** (RegionID, Country, State, City)
* **Date_Dim** (DateKey, Date, Month, Quarter, Year, Fiscal Year)
* **Returns_Fact** (ReturnID, SalesID, ReturnDateKey, Reason)

---

## **Modeling Steps**

* Cleaned all files in **Power Query** (data types, removed blanks, formatted fields).
* Loaded all tables into the model.
* Created relationships:

  * Sales_Fact → Customer_Dim
  * Sales_Fact → Product_Dim
  * Sales_Fact → Region_Dim
  * Sales_Fact → Date_Dim
  * Returns_Fact → Sales_Fact
  * Returns_Fact → Date_Dim (**inactive**)

---

## **Schema Design**

* **Star Schema** with Sales_Fact as central table.
* **Returns_Fact** added as an additional fact table (snowflake extension).
* All relationships are **1-to-Many**, **single direction**.
* Inactive path used for ReturnDateKey → Date_Dim.

---

## **Enhancements**

* Proper data formats (currency, whole numbers, dates).
* Data categories applied (City, Country, Product).
* Hierarchies built:

  * Date: Year → Quarter → Month → Date
  * Region: Country → State → City
  * Product: Category → Subcategory → ProductName

---

## **Verification**

Created a matrix to validate:

* Sales by Product Category & Region
* Returns by Fiscal Year
* Revenue by Customer Segment



