

# 🛍️ HCL Hackathon – Retail Analytics

## 📌 Description

Retail Analytics pipeline using Informatica Cloud and Power BI to clean, transform, and analyze retail data, generating insights on revenue, customers, products, and sales trends.

---

## 📊 Overview

This project implements an **end-to-end ETL pipeline** using **Informatica IICS** and visualizes insights in **Power BI**.

It follows a structured approach:

* Raw data ingestion
* Data cleaning
* Dimension & fact table creation
* Dashboard visualization

---

## 🧱 Architecture

### 🔹 ETL Layers

#### 1. Data Cleaning

* `CUSTOMER_CLEANING`
* `ORDER_CLEANING`
* `PRODUCTS_CLEANING`

Operations:

* Filtering invalid records
* Data standardization
* Sorting & preprocessing

---

#### 2. Dimension Tables

* `DIM_CUSTOMERS`
* `DIM_PRODUCTS`
* `DIM_TIME`

Transformations used:

* Lookup
* Expression
* Aggregator
* Sorter

---

#### 3. Fact Table

* `FACT_ORDERS`

Flow:

```
Orders + Products → Join → Subtotal → Discount → Grand Total
```

---

## 🔄 Taskflow

Main Taskflow: **RETAIL_ANALYSIS**

Execution:

```
Start
 ↓
Parallel Cleaning
 ↓
Transformation Layer
 ↓
Parallel Execution:
   FACT_ORDERS
   DIM_TIME
   DIM_CUSTOMERS
   DIM_PRODUCTS
 ↓
End
```

---

## ⭐ Data Model

### Star Schema

**Fact Table**

* FACT_ORDERS

**Dimension Tables**

* DIM_CUSTOMERS
* DIM_PRODUCTS
* DIM_TIME

---

## 📈 Power BI Dashboard

### Key KPIs

* 💰 Total Revenue: 1.40M
* 📦 Total Orders: 394
* 👥 Total Customers: 95
* 🔁 Repeat Customer Rate: 67.37%

### Visuals

* Monthly Sales Growth
* Top Products
* Customer Lifetime Value
* Revenue by Category

---

## ⚙️ Technologies Used

* Informatica Cloud (IICS)
* SQL / Expressions
* Power BI
* Data Warehousing (Star Schema)

---

## 📂 Repository Structure

```
HCL-HACKATHON-RETAIL-ANALYTICS/
│
├── Explore/HCL Tech/
│   ├── CUSTOMER_CLEANING.MTT.zip
│   ├── ORDER_CLEANING.MTT.zip
│   ├── PRODUCTS_CLEANING.MTT.zip
│   ├── DIM_CUSTOMERS.MTT.zip
│   ├── DIM_PRODUCTS.MTT.zip
│   ├── DIM_TIME.MTT.zip
│   ├── FACT_ORDERS.MTT.zip
│   ├── *.DTEMPLATE.zip
│   └── RETAIL_ANALYSIS.TASKFLOW.xml
│
├── SYS/
│   ├── Source_*.Connection.zip
│   ├── Target_*.Connection.zip
│   └── AgentGroup.zip
│
├── exportMetadata.v2.json
├── exportPackage.chksum
└── README.md
```

---

## 🚀 How to Use

1. Import the exported package into **Informatica Cloud (IICS)**
2. Configure:

   * Source connections
   * Target connections
3. Run the **RETAIL_ANALYSIS Taskflow**
4. Load output data into Power BI
5. Open `.pbix` dashboard

---

## 🔥 Key Features

* End-to-end ETL pipeline
* Parallel task execution
* Modular design (cleaning → dimension → fact)
* Business-ready analytics dashboard
* Scalable architecture

---

## 📌 Future Improvements

* Real-time data pipeline
* ML-based sales forecasting
* Advanced DAX measures
* Cloud deployment (AWS/Azure)

---

## 👨‍💻 Author

 ## PHANTOM TROUPE
