This Power BI dashboard suite is built on top of the BigBasket Quick Commerce SQL Analytics project, reusing the curated Gold-layer tables and views from that repository for consistent, high-quality metrics. The original SQL project (data modeling, ETL and analytics) is available here: [BigBasket SQL Analytics](https://github.com/rohittydvv/bigbasket-sql-analytics).
# 📊 BigBasket Quick Commerce Analytics – Power BI Dashboard Suite

End-to-end Business Intelligence solution for a BigBasket-style quick commerce business, powered by a reusable SQL data pipeline and interactive Power BI dashboards.

## 🎯 Project objective

Deliver a fast, reliable and business-friendly analytics layer for quick commerce that:

- Reuses the cleaned and modeled SQL Gold layer from the BigBasket project to ensure consistent KPI definitions and a single source of truth.
- Provides role-based dashboards for executives, category, marketing, operations and CX teams with clear, actionable insights.
- Demonstrates job-ready skills in data modeling, DAX, interactive reporting and BI design using a real-world e-commerce scenario.

**Key takeaway:** This project shows how to go from SQL data pipeline → semantic model → interactive Power BI app while keeping performance, clarity and reusability in focus.

## 🏗️ Data pipeline & model

The report uses the Gold layer from the BigBasket SQL project as its data source:

**SQL data pipeline**
- Source CSVs → Bronze (raw) → Silver (cleaned) → Gold (business-ready facts and aggregates).
- Gold layer includes: orders, order items, marketing campaigns, customer RFM, product performance and feedback.
- This pipeline guarantees clean KPIs, consistent calculations and reusability across all dashboards.

**Power BI data model**
- Import mode on top of Gold-layer tables/views for fast performance.
- Star-schema style relationships between fact tables (orders, order items, marketing, feedback, RFM) and dimensions (customers, products, campaigns, delivery partners, date).
- Relationships and cross-filtering configured to support page-level filters, drill-downs and consistent totals across pages.

**Power Query**
- Used to connect to SQL, rename fields, enforce data types, derive small helper columns (buckets, labels) and hide technical columns before modeling.

## 🧮 DAX, interactivity, and UX

The report uses a rich DAX layer and interactive features:

**DAX measures**
- Revenue & Profit: Total Revenue, Total Profit, Profit per Order, Avg Order Value.
- Customer value: Active Customers, Avg CLV, Frequency, Recency, RFM segment KPIs.
- Marketing: Spend, Campaign Revenue, ROI, Cost per Conversion, Revenue per Conversion.
- Operations: On Time %, Late Orders %, Avg Delivery Time, Avg Delivery Delay.
- Experience: Avg Rating, Low Rating %, Negative Rating %, sentiment distributions and trends.

**Relationships & filters**
- Proper relationships between orders, items, customers, campaigns and feedback to enable cross-page filtering.
- Visual-level, page-level and report-level filters tuned to keep each page focused while preserving global slicers (Year, Month, Channel, etc.).

**UX features**
- Bookmarks and buttons for navigation and "Clear Filters" actions.
- Role-based Landing page with tiles for each dashboard.
- Consistent color palette, card design and typography across all pages.

## 📈 Dashboards

| Dashboard | Key KPIs | Key Visuals |
|-----------|----------|-------------|
| **Landing / Home** | Navigation hub | Branded entry with tiles for all dashboards |
| **Executive Overview** | Revenue, Profit, Orders, On Time % | Category trends, payment methods, YoY deltas |
| **Product Performance** | Units Sold, Profit/Order, AOV | Margin by category, top/bottom products |
| **Customer Analytics (RFM)** | Active Customers, CLV, Frequency | RFM segments, scatterplots |
| **Marketing Performance** | Spend, ROI, Cost/Conversion | Channel performance, funnel analysis |
| **Delivery & Operations** | On Time %, Delivery Time | Monthly trends, delay analysis |
| **Feedback & Sentiment** | Avg Rating, Negative % | Sentiment distribution, rating trends |

## 🖼️ Screenshot

![Diagram](screenshots/dashboard_overview.jpg)

## 📁 Repository Structure

```text
bigbasket-powerbi-analytics/
├── README.md
├── BigBasket_QuickCommerce_Analytics.pbix           # Main Power BI report
├── screenshots/
│ ├── dashboard_overview.jpg
│ ├── 01_home_landing.jpg
│ ├── 02_executive_overview.jpg
│ ├── 03_product_performance.jpg
│ ├── 04_customer_analytics_rfm.jpg
│ ├── 05_marketing_performance.jpg
│ └── 06_feedback_sentiment.jpg
└─ BigBasket_QuickCommerce_PowerBI_Report.pdf        # PDF export of dashboards
```
## ▶️ How to use this report

1. Clone or download this repository
2. Open `BigBasket_QuickCommerce_Analytics.pbix` in Power BI Desktop
3. Navigate via Home page buttons or page tabs
4. Use slicers (Year, Month, Channel, etc.) to filter insights
5. Compare metrics across dashboards using consistent SQL Gold layer KPIs

**⚠️ Note:** Contains imported data snapshot; no live DB connection.

## 👤 Author

**Author:** Rohit Yadav  
**SQL Project:** [BigBasket SQL Analytics](https://github.com/rohittydvv/bigbasket-sql-analytics)  
**Email:** rohit.ydvv23@gmail.com  
**LinkedIn:** [Rohit Yadav](https://www.linkedin.com/in/rohittydvv/)

*Demonstrates SQL → Power BI end-to-end analytics for quick commerce.*

