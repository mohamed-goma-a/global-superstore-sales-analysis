# 🌍 Global Superstore — Sales & Profit Analysis (Power BI)

A Power BI dashboard that analyzes global retail sales data — covering customers, products, locations, and month-over-month performance — to answer real business questions from a public Kaggle dataset.


---

## 📌 Overview

This project analyzes sales data from a global superstore that operates across multiple markets — US, EU, APAC, LATAM, EMEA, Africa, and Canada.

The goal is to understand sales, profit, customer behavior, product performance, and shipping efficiency. The data was cleaned in Power Query, modeled using a star schema, and visualized in a 5-page Power BI dashboard.

## 📂 Data Source

- **Dataset:** [Global Super Store Dataset](https://www.kaggle.com/datasets/apoorvaappz/global-super-store-dataset) (Kaggle)
- Contains order details, customers, products, locations, sales, profit, discount, and shipping information.

## ❓ Business Questions

**Customer Analysis**
- Profile customers based on their purchase frequency
- Do high-frequency customers contribute more revenue?
- Are they also more profitable? What is the profit margin across each bucket?
- Which customer segment is most profitable each year?
- How are customers distributed across countries?

**Product Analysis**
- Which country has the top sales?
- Which are the top 5 profit-making product types on a yearly basis?
- What is the average delivery time across countries?

> Country-level detail is available through **Drill Down** (Market → Country) on the market charts. Top 5 products by year can be explored using the **Year slicer** together with the Profit by Product chart.

## 🧩 Data Model

The dashboard uses a star schema — one fact table connected to four dimension tables.

| Table | Holds |
|---|---|
| `fact_sales` | Sales, profit, quantity, discount — one row per order line |
| `dim_customer` | Customer name, segment, frequency (Loyal, Frequent, Repeat, Low Frequency) |
| `dim_product` | Category, sub-category, product name |
| `dim_location` | Country, region, market |
| `dim_order_details` | Ship mode, order priority |
| `dim_date` | Day, month, year |

## 📊 Dashboard Pages

1. **Overview** — Total Sales (12.64M), Total Profit (1.47M), Total Orders (25K), Active Customers (2K), plus trends by year, sub-category, and market.
2. **Customer Analysis** — Profit margin (11.61%), retention rate (53.31%), customer frequency buckets, top customers, profit by segment.
3. **Product Analysis** — Top products and categories by profit, sales/profit/discount by sub-category.
4. **Location Analysis** — Average days to ship (3.97), average shipping cost (26.38), shipping cost by ship mode, sales & profit by market.
5. **MoM Performance** — Month-over-month comparison of sales, profit, and orders, broken down by sub-category.

## 🔍 Key Insights

- APAC and EU are the top markets for sales and profit.
- Technology is the most profitable category (45.23% of profit).
- Tables is the only sub-category losing money.
- Frequent Customers bring the highest total profit (879K).
- Profit dropped faster than sales this period (-25.36% vs -9.39%), signaling weaker margins.
- Same Day shipping is the fastest but has a lower cost share than Standard Class.

## 💡 Recommendations

- Add conditional formatting to highlight negative profit values (like Tables) in red.
- Investigate why Tables is losing money — check if its discount level is too high.
- Look into why profit is dropping faster than sales — may point to rising costs or heavier discounting.
- Add a product price/cost field in future versions to enable price-based analysis.
- Focus retention efforts on Low Frequency customers — the largest group, with the lowest profit margin (9.31%).

## 🛠️ Tools Used

- **Power Query** — data cleaning and shaping
- **Power BI** — data modeling and dashboard design
- **DAX** — measures like MoM %, Retention Rate, and Profit Margin

---

### 📎 Links

- Dataset: [Kaggle - Global Super Store Dataset](https://www.kaggle.com/datasets/apoorvaappz/global-super-store-dataset)
