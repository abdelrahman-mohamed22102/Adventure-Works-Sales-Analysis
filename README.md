# Power BI Orders Analysis – AdventureWorks 2019

## Overview

This project presents an end-to-end **Power BI business intelligence solution** built on the **AdventureWorks2019 OLTP database**. The focus is on analyzing customer orders across territories, product categories, quantities, prices, and time, with an emphasis on data modeling, DAX, and interactive reporting.

The solution demonstrates strong capabilities in data preparation, dimensional modeling, and analytical storytelling using Power BI.

---

## Data Source

* **Database:** AdventureWorks2019 (OLTP version)
* **Format:** SQL Server backup (`.bak`)
* **Official Source:** Microsoft Learn (AdventureWorks sample database)
* **Fact Table Size:** ~121,000 rows (order line level)
* **Order Period:** May 2011 – June 2014
* **Notable Pattern:** Significant behavioral changes observed starting June 2013

---

## Mission & Scope

Analyze sales orders with respect to:

* Sales territories
* Product categories and subcategories
* Order quantities and pricing
* Order, ship, and due dates

The goal is to identify performance drivers, concentration of demand, and temporal order behavior.

---

## Data Preparation & Modeling

### Data Cleaning & Feature Engineering

* Cleaned raw OLTP tables and resolved data quality issues
* Performed feature engineering and column selection
* Calculated financial attributes at order level
* Denormalized transactional data for analytical efficiency

### Data Model

* Designed and implemented a **Star Schema**
* Optimized relationships for DAX performance

**Core Tables:**

* FactOrders / FactOrderDetails
* DimDate
* DimProduct
* DimTerritory

<img width="1410" height="837" alt="image" src="https://github.com/user-attachments/assets/250bfc81-1e6e-48ea-904c-2b329fe97d80" />


---

## Measures & Calculations

### Key Measures (DAX)

* Total Orders
* Total Order Lines
* Total Product Quantity

### Calculated Columns (DAX)

* Subtotal
* Total Tax
* Total Freight
* Total Due

---

## Hierarchies

* **Date Hierarchy:** Year → Quarter → Month → Day
* **Product Hierarchy:** Category → Subcategory → Product

These hierarchies enable intuitive drill-down and drill-through analysis.

---

## Report Features

* Interactive dashboards with KPI cards
* **Custom informative tooltips** linked across visuals
* **Drill-through pages** for detailed order analysis
* **Drill-down functionality** in treemap using product hierarchy
* Slicers for:

  * Territory
  * Total Due (value-based filtering)
  * Order Date

---

## Date Behavior Analysis

A dedicated analytical page compares:

* Order Date
* Ship Date
* Due Date

Key observations:

* High concentration of orders at the **end of each month**
* Ship dates typically fall within the **first week of the following month**
* Due dates are commonly scheduled **one week after shipping**

<img width="1158" height="653" alt="image" src="https://github.com/user-attachments/assets/a6ed67fb-5d15-4a0d-a9ff-64fb66659c13" />


---

## Key Insights

* **50% of total orders** originate from **Australia, Southwest, and Northwest** territories
* **Accessories** account for **65%+ of total orders**, making it the highest-selling category
* **Tires and Tubes** dominate Accessories, contributing:

  * 50%+ of Accessories orders
  * ~30% of total orders overall
* Dataset contains approximately:

  * **31,000 orders**
  * **121,000 order lines**
  * **~123 million** in total order value
* The majority of impactful order activity occurred during **2013–2014**

---

## Dashboard Preview


https://github.com/user-attachments/assets/b899fe5d-9990-4855-8fb0-7b261e836c7d



https://github.com/user-attachments/assets/b7596946-f474-45b2-a253-e661ad94633e


* Overview dashboard
* Territory performance analysis
* Product category and hierarchy analysis
---

## Tools & Technologies

* Power BI Desktop
* DAX (Measures & Calculated Columns)
* SQL Server (AdventureWorks2019)
* Data Modeling (Star Schema)


---

## How to Use

1. Restore the AdventureWorks2019 database in SQL Server
2. Connect Power BI to the SQL Server instance
3. Refresh the dataset
4. Explore dashboards using slicers, drill-down, and drill-through

---

## Author

**Abdelrahman Mohamed Abdelrahman Abdellatif**

## License

This project is intended for educational and portfolio demonstration purposes.
