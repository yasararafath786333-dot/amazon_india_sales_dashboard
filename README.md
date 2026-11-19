# Amazon India Sales & Business Performance Dashboard

**Sapphire IQ — Data Analytics Internship (Project 1 of 4)**  
**Prepared by:** R. Yasar Arafath

---

## Project Overview

This project builds a clear, management-ready Microsoft Excel dashboard for **Manoj** to present to his non-technical manager, **Ravi**. Using 10,000 Amazon India order records from **January 2024 to August 2026**, the workbook tracks overall sales and profit, category and product performance, order status, payment methods, fulfillment channels, and state-wise performance in one place.

---

## File in This Repository

- `Amazon_India_Sales_Dashboard.xlsx` — Complete Excel workbook containing 7 tabs:
  - **`Dashboard`**: Main executive view with 6 dynamic KPI cards, 6 charts, and a management summary.
  - **`Raw_Data`**: All 10,000 original order records formatted as a native Excel Table (`AmazonSalesData`) with `Year_Month` and `Order_Year` helper columns.
  - **`Objective_1`**: Overall KPIs, yearly monthly-average comparison, 32-month sales/profit trend, and Q&A notes.
  - **`Objective_2`**: Category performance, Top 10 products, Bottom 5 products needing attention, and 3 charts.
  - **`Objective_3`**: Delivered, Shipped, Returned, and Cancelled order metrics, category-wise breakdown, and revenue exposure note.
  - **`Objective_4`**: Payment method, fulfillment method, and all 10 states ranked by sales, profit, and order volume.
  - **`Read_Me`**: Data quality checks, metric definitions, and direct answers to all 4 business questions.

---

## Key Headline KPIs

| Metric | Value |
| :--- | ---: |
| **Total Sales** | ₹155,789,894 |
| **Total Profit** | ₹33,167,008 |
| **Total Orders** | 10,000 |
| **Total Units Sold** | 24,926 |
| **Average Order Value (AOV)** | ₹15,579 |
| **Profit Margin** | 21.3% |
| **Return Rate** | 4.9% (485 orders) |
| **Cancellation Rate** | 5.0% (500 orders) |

---

## Data Quality & Cleaning Audit

Before building the dashboard, I verified the source file (`Amazon Sales Data India.xlsx`) without changing or deleting any original records:

- **Record Count:** 10,000 rows and 13 original columns.
- **Missing Values & Duplicates:** 0 blank cells, 0 duplicate rows, and 0 duplicate `Order_ID` values.
- **Formula Accuracy Check:** Verified `Quantity × Unit_Price_INR × (1 - Discount_Pct) = Total_Sales_INR` on all 10,000 rows with ₹0.00 discrepancy.
- **Zero-Profit Check:** 985 rows record ₹0 profit — 100% match Cancelled (500) and Returned (485) orders; 0 rows have negative profit.
- **Field Integrity:** Only actual dataset columns (`Category`, `Product`, `Ship_State`, etc.) were used without inventing missing fields like Subcategory, City, or Region.

---

## Answers to the 4 Business Objectives

### 1. Overall Sales & Profit Performance
- **How is the business performing overall?**  
  Performance is strong and steadily improving. Average monthly sales grew from **₹4,751,068** in 2024 to **₹4,785,573** in 2025, and reached **₹5,168,775** in 2026 (Jan–Aug). Monthly profit rose from **₹1,010,926** to **₹1,104,184** over the same period.
- **Peak vs. Slowest Month:** **July 2026** was the peak month (**₹6,443,679** sales across 374 orders), while **April 2025** was the slowest (**₹3,889,801** across 280 orders). Profit margins stayed steady between **19.1%** and **22.9%** every month.

### 2. Category & Product Performance
- **Which categories and products drive the business?**  
  **Electronics & Mobiles** leads with **79.3%** of total sales (**₹123,569,507**) and **₹26,310,257** in profit, followed by **Home & Kitchen** (**11.5%**; **₹17,973,219**). **Apparel & Fashion** ranks #2 in volume (**6,452 units**) but contributes **6.3%** of sales due to lower unit prices.
- **Top Performers:** All top 5 products are Electronics & Mobiles, led by **Laptop Backpack** (**₹26,529,187**), **Power Bank 20000mAh** (**₹25,548,449**), and **5G Smartphone** (**₹24,330,766**). The top 10 products generate **90.9%** of total revenue.
- **Products Needing Attention:** All bottom 5 items are in **Pantry & Groceries**, led by **Filter Coffee Powder** (**₹247,593**). By order issues, **Matte Lipstick** (**13.1%**) and **Sports Shoes** (**11.5%**) have the highest combined return and cancellation rates.

### 3. Order Status & Potential Revenue Exposure
- **How many orders are completed vs. lost?**  
  **8,147 orders (81.5%)** were Delivered and **868 (8.7%)** are Shipped (**90.2%** healthy fulfillment). **500 orders (5.0%)** were Cancelled and **485 (4.9%)** were Returned.
- **Exposure vs. Actual Loss:** The **₹15,648,743** across those 985 Cancelled and Returned orders represents **recorded order value exposure** (with ₹0 recorded profit in the dataset), not automatic net cash loss, since cancelled orders are generally not dispatched and returned stock can often be resold.
- **Category Hotspots:** **Electronics & Mobiles** has the highest return count (**164 returns; 5.4%**), while **Apparel & Fashion** has the highest cancellation count (**148 cancellations; 5.7%**).

### 4. Payment, Fulfillment & Geographic Performance
- **Payment Methods:** **UPI** leads with **50.4%** of sales (**₹78,515,436** across 4,972 orders), followed by **Credit/Debit Card** (**19.9%**; **₹31,069,231**) and **Cash on Delivery** (**14.8%**; **₹23,101,584**).
- **Fulfillment Channels:** **Amazon (FBA)** generates **69.0%** of sales (**₹107,528,288**; **21.3%** margin). **Seller Flex** achieves the highest margin (**21.8%**), while **Merchant (FBM)** has the smallest share (**11.0%**) and lowest margin (**20.3%**).
- **Top States:** **Maharashtra** (**₹29,554,237**), **Karnataka** (**₹24,415,704**), and **Delhi** (**₹22,361,687**) drive **49.0%** of total revenue, with **Tamil Nadu** 4th (**₹17,889,855**). **Rajasthan** (**₹6,620,697**) and **Kerala** (**₹6,611,724**) are the smallest markets.

---

## Recommendations for Management

1. **Smooth Seasonal Dips:** Run targeted offers during slower spring months (Feb–Apr) and stock top Electronics SKUs ahead of peak mid-year demand.
2. **Reduce Category Friction:** Add stricter pre-dispatch checks and clearer specs on Electronics (especially Smartwatches at 6.1% returns) and faster order confirmation on Apparel (especially Sports Shoes at 7.8% cancellations).
3. **Focus on High-Performing Channels:** Keep UPI checkout frictionless, prioritize FBA/Seller Flex inventory near Maharashtra, Karnataka, and Delhi, and test regional promotions in Rajasthan and Kerala.

---

## Tools & Excel Skills Used

- **Microsoft Excel:** Native Excel Tables, Dynamic Formulas (`SUM`, `SUMIF`, `COUNTIF`, `COUNTIFS`, `TEXT`, `YEAR`), Conditional Formatting Data Bars, KPI Cards, Line/Column/Bar/Stacked/Doughnut Charts, and Management Dashboard Design.
-
