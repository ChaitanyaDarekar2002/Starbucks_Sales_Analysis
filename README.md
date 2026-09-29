# ☕ Starbucks Analysis Dashboard

A two-part analytics project for Store #101 (Seattle Flagship) that turns raw order data into real-time, actionable insight — a live web-based Sales Manager app backed by PostgreSQL, and a companion Power BI report for deeper, offline-style analysis.


# 📖 Overview
This project simulates a Starbucks store-operations dashboard, combining:

**Starbucks Sales Manager (Web App)** — a live order-management console with real-time PostgreSQL-backed metrics: total sales, order volume, average order value, and top-selling item, plus a searchable/filterable transactions table.

**Power BI Report** — a polished "Daily Sales Performance" report with hourly breakdowns of average spend, revenue, and units sold, alongside order/customer/quantity KPIs.

Together they cover the full loop: raw transactional data → operational dashboard → executive reporting.


# 🖼️ Preview

**Starbucks_Sales_dashboard**

Real-time order tracking with search, filters (payment mode, customer type, date), and a live transactions table pulled straight from PostgreSQL.

<img width="1907" height="979" alt="image" src="https://github.com/user-attachments/assets/742fa8ec-0a8f-458d-8ffc-72d8953c5078" />


**Power BI — Daily Sales Performance**

Hourly sales insights: average spend per order, revenue, and units sold, with order/customer/amount/quantity summary rings.

<img width="1906" height="975" alt="image" src="https://github.com/user-attachments/assets/394ab32e-3f07-45a8-a0b3-cd2afd566d6b" />


**Dashboard Detail View**

<img width="1905" height="974" alt="image" src="https://github.com/user-attachments/assets/0ce59a4c-c1d6-47d3-bc5d-c13e2958ab62" />


**Repository / Data View**

<img width="1905" height="975" alt="image" src="https://github.com/user-attachments/assets/6ce1953f-24d5-489c-9a5d-41b4392c946d" />


# ✨ Key Features

Web App

Live KPI cards — Total Sales, Total Orders, Avg Order Value, Top Item
Orders Transactions Table with search by Transaction ID / Customer / Item
Filters for Payment Mode, Customer Type, and Date
One-click "Create Order" / "New Order" flow
Real-time PostgreSQL aggregation, scoped per store (e.g. Store #101)
Power BI Report

Order Count, Customer Count, Total Amount, Total Quantity summary
Average Spend per Order by Hour
Revenue by Hour
Units Sold by Hour
Auto-labeled "Last Updated" timestamp for freshness tracking
🛠️ Tech Stack
Layer	Technology
Frontend	React / Next.js (Starbucks web app)
Backend / DB	PostgreSQL
Reporting	Power BI (.pbix)
Data	CSV extracts (customers, items, sales)
Queries	Raw SQL (SQL Queries.txt)
📂 Project Structure
Starbucks Analysis Dashboard/
├── Starbucks web app/        # Web application source (React/Next.js + PostgreSQL)
├── img/                      # App/report assets (logos, icons, etc.)
├── Dashboard imgs/           # README/preview screenshots
├── SQL Queries.txt           # SQL used to build/aggregate the dataset
├── Starbucks Dashboard.pbix  # Power BI report file
├── customers.csv             # Customer records
├── items.csv                 # Menu item catalog
├── sales.csv                 # Transaction / order-level sales data
└── README.md
🚀 Getting Started
1. Power BI Report
Install Power BI Desktop.
Open Starbucks Dashboard.pbix.
If prompted, point the data source connections at your local copies of customers.csv, items.csv, and sales.csv (or your PostgreSQL instance).
Refresh the report to load the latest data.
2. Web App
# from the "Starbucks web app" directory
npm install

# configure your PostgreSQL connection
cp .env.example .env
# edit .env with your DB host, user, password, and database name

npm run dev
The app runs at http://localhost:3000 by default.

3. Loading the Data
Use SQL Queries.txt as a reference for the schema and aggregation queries, and import customers.csv, items.csv, and sales.csv into your PostgreSQL database to seed the app.

📊 Data Files
File	Description
customers.csv	Customer ID, name, and customer-type metadata
items.csv	Menu items, categories, and pricing
sales.csv	Transaction-level order data (qty, price, payment mode, timestamp)
🗺️ Roadmap
 Multi-store support beyond Store #101
 Automated Power BI refresh from live PostgreSQL data
 Order-level drill-down analytics in the web app
 Authentication & role-based access for store managers
🤝 Contributing
Issues and pull requests are welcome — please open an issue first to discuss significant changes.

📄 License
This project is licensed under the MIT License.
