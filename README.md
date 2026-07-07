# Supply Chain Control Tower

**Enterprise Supply Chain Analytics | Power BI | Advanced Data Modeling | Predictive Inventory Intelligence**

An enterprise-grade Supply Chain Control Tower built in Power BI that enables executives, procurement teams, warehouse managers, and finance leaders to monitor operational performance, identify bottlenecks, predict inventory shortages, evaluate supplier performance, and simulate supply chain disruptions using interactive What-If analysis.

---

## Overview

Modern supply chains generate enormous amounts of operational data, yet many organizations still rely on static reports that explain what happened yesterday rather than helping decision-makers understand what will happen tomorrow. 

This project bridges that gap by building a centralized Supply Chain Control Tower that combines logistics, procurement, inventory management, warehouse operations, and supplier performance into a single interactive analytical platform.

Rather than simply displaying KPIs, the dashboard focuses on:
* Operational monitoring
* Root cause analysis
* Inventory risk prediction
* Supplier performance evaluation
* Executive decision support
* Scenario simulation using What-If Parameters

---

## Business Problem

Supply chain leaders frequently struggle with questions such as:
* Which supplier is causing most delivery delays?
* Are increasing freight costs improving delivery performance?
* Which warehouses are nearing capacity?
* Which SKUs are likely to stock out soon?
* Which suppliers should procurement prioritize?
* How would supplier delays impact inventory availability?

Answering these questions typically requires combining information across multiple operational systems. This dashboard centralizes those insights into a single executive decision-making platform.

---

## Objectives

* Monitor enterprise-wide supply chain health
* Measure delivery performance using OTIF
* Track logistics costs over time
* Optimize warehouse utilization
* Predict future inventory shortages
* Evaluate supplier reliability
* Simulate procurement risks using What-If analysis
* Enable executives to quickly identify operational bottlenecks

---

# Dataset Information

This project uses synthetically generated supply chain data created specifically for portfolio and demonstration purposes.

The dataset does not contain confidential company information, real customer records, personal data, or proprietary operational data.

## Included Tables

- `dim_products.csv`
- `dim_suppliers.csv`
- `dim_warehouses.csv`
- `fact_inventory.csv`
- `fact_shipments.csv`

The files were designed to support a Power BI star-schema model covering logistics, inventory, warehouse, product, and supplier performance.


## Dashboard Pages

### Page 1: Executive Overview
The Executive Overview provides a high-level operational health snapshot designed for senior management.

* **KPIs:** Total Logistics Cost, On-Time In-Full (OTIF %), Average Supplier Lead Time, Stockout Risk (Imminent SKUs)
* **Visualizations:** OTIF Performance Trend, Logistics Cost Trend, Supplier Delay Ranking, Executive Summary (Dynamic Narrative)
* **Business Insights:** Executives can instantly determine overall supply chain performance, delivery reliability, transportation spending, supplier delays, inventory risk, and overall operational health.

### Page 2: Inventory & Warehouse Intelligence
This page focuses on warehouse operations and inventory optimization.

* **KPIs:** Current Inventory Value, Inventory Turnover, Warehouse Utilization, Days Inventory Remaining
* **Visualizations:** Warehouse Utilization, SKU Velocity Analysis, Days Inventory Remaining, Inventory Distribution, Warehouse Performance
* **Business Insights:** Warehouse managers can identify dead stock, overstocked inventory, low inventory items, fast-moving SKUs, and warehouses nearing capacity.

### Page 3: Supplier Performance & Procurement Intelligence
The supplier scorecard evaluates procurement performance and supplier reliability.

* **KPIs:** OTIF %, Average Lead Time, High Risk Suppliers, Logistics Cost
* **Visualizations:** Supplier Performance Matrix, OTIF Trend, Supplier Performance Table, Procurement Executive Insight, What-If Supplier Delay Simulation
* **Business Insights:** Procurement teams can compare supplier performance, identify strategic/high-risk suppliers, evaluate lead times, monitor risk, and simulate future supplier disruptions.

---

## Key Business Metrics

**OTIF (On-Time In-Full)**
Measures supplier delivery reliability. Higher OTIF indicates stronger supplier performance.
$$OTIF\%=\frac{OrdersDeliveredOnTime}{TotalOrders}$$

**Inventory Turnover**
Measures inventory efficiency. Higher turnover indicates efficient inventory management.
$$InventoryTurnover=\frac{TotalCOGS}{AverageInventoryValue}$$

**Average Lead Time**
Measures the average supplier delivery duration. Lower lead times improve operational efficiency.

**Stockout Risk**
Predicts inventory shortages based on Daily Demand, Current Stock, and Days Inventory Remaining. This transforms the dashboard from descriptive analytics into predictive analytics.

**Warehouse Utilization**
Measures warehouse occupancy relative to capacity.

**Logistics Cost**
Tracks enterprise freight spending over time.

---

## Unique Selling Proposition (USP)

Unlike traditional dashboards that report historical performance, this project introduces predictive supply chain intelligence. The dashboard proactively identifies SKUs likely to stock out within the next 14 days by combining Current Stock, Daily Demand, and Inventory Remaining. This enables procurement teams to reorder inventory before shortages impact customer sales, moving the project beyond descriptive reporting into operational decision support.

---

## Advanced Features

* **Predictive Stockout Detection:** Automatically flags inventory likely to become unavailable before demand can be fulfilled.
* **What-If Simulation:** Users can adjust a Supplier Delay parameter to simulate supplier disruptions. The dashboard dynamically recalculates Stockout Risk, Procurement Impact, and Supplier Performance, enabling scenario planning without modifying source data.
* **Supplier Performance Matrix:** Segments suppliers into strategic quadrants (Preferred, Strategic, Improve Performance, High Risk) based on Average Lead Time and OTIF %.
* **Executive Dynamic Narrative:** A DAX-powered executive summary automatically changes based on report filters and KPIs, highlighting overall performance, best/highest-risk suppliers, and procurement recommendations.
* **Interactive Drill-Down Analysis:** Users can drill from enterprise KPIs down to individual suppliers, warehouses, SKUs, categories, and locations to support rapid root cause analysis.

---

## Data Model

The solution follows an enterprise Star Schema consisting of One-to-Many Relationships, a Calendar Dimension, Surrogate Keys, Parameter Tables, and a Measure Table for relationship optimization.

### Fact Tables

| Table Name | Fields |
| :--- | :--- |
| **Fact Shipments** | Order ID, Order Date, Expected Delivery Date, Actual Delivery Date, Supplier ID, Warehouse ID, SKU, Freight Cost, Order Quantity |
| **Fact Inventory** | Date, Warehouse ID, SKU, Stock On Hand, Average Daily Demand |

### Dimension Tables

| Table Name | Fields | Description |
| :--- | :--- | :--- |
| **Calendar** | Standard Date Fields | Complete enterprise date dimension supporting time intelligence. |
| **Suppliers** | Supplier ID, Supplier Name, Country, Contracted Lead Time, Baseline Defect Rate | Tracks all vendor-related data. |
| **Products** | SKU, Category, Unit Price, COGS | Tracks item-level master data. |
| **Warehouses** | Warehouse ID, Location, Capacity, Storage Cost | Tracks physical storage parameters. |

---

## Technical Implementation

### DAX Features
Over 40+ reusable measures were created utilizing advanced DAX functions, including:
* CALCULATE, FILTER, VAR, SWITCH, DIVIDE
* SUMX, AVERAGEX
* SELECTEDVALUE, TOPN, RANKX
* ALL, REMOVEFILTERS, IF, UNICHAR
* Time Intelligence Functions

### Power BI Features Used
* Star Schema Modeling & Advanced DAX
* Dynamic KPIs & Field Parameters
* What-If Parameters & Dynamic Text Narratives
* Conditional Formatting & Cross Filtering
* Drill Through & Report Tooltips
* Bookmarks & Navigation Buttons
* Interactive Scatter Charts & Matrix Visualizations
* Custom Executive Dashboard Design

### Tech Stack
* Power BI Desktop
* Power Query
* DAX
* Star Schema Data Modeling
* Microsoft Excel (Data Generation & Preparation)

---

## Skills Demonstrated

* Business Intelligence & Power BI Development
* Data Modeling & DAX Programming
* Supply Chain, Procurement & Inventory Analytics
* Dashboard Design & Executive Reporting
* Predictive Analytics & Root Cause Analysis
* Scenario Planning

---

## Key Takeaways

This project demonstrates how enterprise BI solutions can evolve from static reporting into intelligent operational decision-support systems. By integrating logistics, inventory, warehouse, and supplier data into a unified analytics platform, the dashboard empowers stakeholders to monitor performance, diagnose operational bottlenecks, predict future inventory risks, and evaluate the impact of supplier disruptions through interactive scenario analysis. The result is a scalable, executive-ready Supply Chain Control Tower that showcases advanced Power BI development, business-focused storytelling, and real-world analytics capabilities suitable for enterprise environments.
