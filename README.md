# Amazon-Sales-Report-Dashbord 
# 📦 Amazon Sales Report Dashboard

An interactive Power BI report built to explore and analyze Amazon order-level sales data — covering order status, fulfilment method, product categories, courier performance, and shipping geography.

## 📝 Description

The Amazon Sales Report Dashboard is a Power BI report designed to help users quickly understand order and revenue patterns from Amazon transaction data. It surfaces total sales, top-selling categories, fulfilment and delivery-partner breakdowns, courier status, product size distribution, and state-wise shipping volume — all filterable by date. This tool is intended for e-commerce analysts, operations teams, and business stakeholders who need a fast, visual read on sales and logistics performance.

## 🛠️ Tech Stack

The dashboard was built using the following tools and technologies:

* 📊 **Power BI Desktop** – Main data visualization platform used for report creation.
* 📂 **Power Query** – Data transformation and cleaning layer for reshaping and preparing the data.
* 🧠 **DAX (Data Analysis Expressions)** – Used for aggregations such as total sales (`Sum(Amount)`) and category/status counts.
* 📝 **Data Modeling** – A `Date` relationship links the `Amazon Sale Report` fact table to an auto-generated date table, enabling time-based filtering.
* 📁 **File Format** – `.pbit` (Power BI Template) for development.

## 📂 Data Source

The report is built on the **Amazon Sale Report** table, containing order-level e-commerce data with the following fields:

* **Order details:** `Date`, `Status`, `Fulfilment`, `Sales Channel`, `ship-service-level`, `Courier Status`, `fulfilled-by`
* **Product details:** `Category`, `Size`, `Qty`, `Amount`
* **Shipping details:** `ship-city`, `ship-state`, `ship-postal-code`, `ship-country`
* **Order type:** `B2B` (flags business-to-business orders)

## ✨ Features / Highlights

### Business Problem
E-commerce teams handle high volumes of order and shipping data daily, but raw transaction logs make it hard to quickly answer questions like: Which categories drive the most sales? How are orders being fulfilled? Where are shipments concentrated geographically? How reliable is delivery performance?

### Goal of the Dashboard
To deliver a single-page, interactive view that:
* Summarizes total sales at a glance.
* Breaks down orders by category, size, fulfilment type, and delivery partner.
* Tracks courier/delivery status to spot fulfillment issues.
* Shows state-wise shipping distribution.
* Lets users filter the entire report by date.

### Walkthrough of Key Visuals

* **Total Sales (Card)** — A single KPI card showing the sum of `Amount` across all orders.
* **Date Slicer** — An interactive filter that lets users narrow all visuals down to a specific date or date range.
* **Top 5 Categories (Bar Chart)** — Ranks product categories by order count, highlighting best-selling product types.
* **Courier Status (Pie Chart)** — Breaks down orders by courier status (e.g., shipped, delivered, cancelled) to assess delivery performance.
* **Delivery Partner (Column Chart)** — Shows order volume by the `fulfilled-by` field, indicating which delivery partner handled fulfillment.
* **Fulfilment (Column Chart)** — Compares order counts by fulfilment method (e.g., Amazon vs. Merchant fulfilled).
* **Size (Clustered Bar Chart)** — Displays order distribution across product sizes.
* **Ship - States (Clustered Column Chart)** — Ranks Indian states by shipping volume, revealing regional demand hotspots.

### Business Impact & Insights
* **Sales Monitoring:** Instantly track total revenue and category-level performance without digging through raw spreadsheets.
* **Operations Optimization:** Identify which fulfilment methods and delivery partners are used most, helping optimize logistics decisions.
* **Delivery Reliability:** Courier status breakdown helps flag shipping or cancellation issues early.
* **Regional Strategy:** State-wise shipment data helps identify high-demand regions for marketing or inventory planning.
* **Product Strategy:** Category and size distributions inform inventory and product-line decisions.

## 📸 Screenshots / Demo
https://github.com/Dhruvrwt/Amazon-Sales-Report-/blob/main/Snapshort%20of%20Amazon%20Dashbord.png

## 🚀 How to Use

1. Clone or download this repository.
2. Open `Amazon_Sales_Report_Dashbord.pbit` in Power BI Desktop.
3. When prompted, load your Amazon sales dataset (matching the schema above) or connect to your own data source.
4. Use the date slicer at the top to filter all visuals by a specific time period.
