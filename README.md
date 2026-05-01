# Northwind Traders Dashboard

> A 3-page Power BI dashboard suite that tracks sales revenue, product & category performance, regional operations, and employee contribution across time and geography.

<img width="3132" height="2261" alt="Northwind Traders Dashboard" src="https://github.com/user-attachments/assets/257e7e04-0de8-4ac7-bfd6-a2d4d8f39858" />

---

## 📋 Table of Contents

- [Overview](#overview)
- [Dashboard Pages](#dashboard-pages)
  - [Sales & Revenue Overview](#1-sales--revenue-overview)
  - [Product & Category Intelligence](#2-product--category-intelligence)
  - [Regional & Operational Performance](#3-regional--operational-performance)
- [Key Metrics & KPIs](#key-metrics--kpis)
- [Relationship Model](#relationship-model)
- [Dataset Schema](#dataset-schema)
- [File Structure](#file-structure)
- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Usage & Filters](#usage--filters)
- [Insights Summary](#insights-summary)

---

## Overview

The **Northwind Traders Dashboard** is a Power BI report built to monitor sales performance, product intelligence, and operational efficiency for the Northwind Traders business. It equips sales managers, category analysts, and operations leads with the data needed to track revenue trends, evaluate discount strategies, monitor logistics performance, and benchmark employee contribution all from a single dataset.

### 🎯 Business Objectives

- Track total and segmented revenue performance against prior periods (YoY and MoM)
- Identify which product categories and individual products generate the most revenue and volume
- Understand the impact of discounting on revenue and sales volume per category
- Monitor regional and customer-level revenue contribution across countries and cities
- Measure operational efficiency through shipping performance and delivery delay metrics
- Benchmark individual employee revenue contribution across the sales team

---

## Dashboard Pages

### 1. Sales & Revenue Overview

> *Tracks revenue performance, order trends, and customer contribution across time and geography.*

<img width="1571" height="864" alt="Sales   Revenue Overview" src="https://github.com/user-attachments/assets/917b49a4-12f8-4ac3-8f26-53a8d370f8b6" />

#### KPI Cards

| KPI | Value | YoY | MoM |
|-----|-------|-----|-----|
| **Total Revenue** | $1.27M | ▲ 179.31% ($812,606) | ▲ 1.47% ($18,334) |
| **Total Orders** | 830 | ▲ 170.36% (523) | ▲ 1.72% (14) |
| **Avg Order Value** | $1.53K | ▲ 3.31% ($48.87) | ▼ 0.24% (-$3.70) |
| **Sales Volume** | 51K | ▲ 157.10% (31,357) | ▲ 1.83% (921) |

#### Slicer Filters

| Filter | Options |
|--------|---------|
| **Year / Month** | Date range selector |
| **Product Category** | All categories in dataset |
| **Employees** | All employees in dataset |
| **Country** | All countries in dataset |
| **Shippers Company** | All shipping company in dataset |

#### Visuals

**Total Revenue and Avg Order Value by Month — Combo Chart** *(Drill down to quarter and year)*
- Revenue bars overlaid with an Avg Order Value trend line, with MoM % change labels on each bar
- Reveals seasonality, pricing shifts, and demand patterns month over month
- April is the peak revenue month (▲23.3% MoM); May–June show the steepest dips (▼59.2%, ▼32.4%)

**Total Revenue by Company Name — Bar Chart** *(Drill down to contact_name)*
- Ranks top customers by total revenue generated
- Quick-Stop ($110K), Ernst Handel ($105K), and Save-A-Lot Markets ($104K) lead the ranking
- Helps identify high-value accounts for retention and growth focus

**Customer Revenue Contribution % by Country — Bar Chart** *(Drill down to city)*
- Shows each country's percentage share of total revenue
- USA leads at 12.28%, followed by Germany (11.15%) and Austria (8.29%)
- Drill-down surfaces city-level contribution within each country

---

### 2. Product & Category Intelligence

> *Analyses product and category performance, sales trends, and discount impact.*

<img width="1567" height="865" alt="Product   Category Intelligence Dashboard" src="https://github.com/user-attachments/assets/6a20f1fe-f232-432d-b5c3-f3dc3f16ee79" />

#### KPI Cards

| KPI | Value | YoY | MoM |
|-----|-------|-----|-----|
| **Total Revenue** | $1.27M | ▲ 179.31% ($812,606) | ▲ 1.47% ($18,334) |
| **Active Revenue** | $1.08M | ▲ 177.53% ($691,362) | ▲ 1.36% ($14,493) |
| **Discontinued Revenue** | $184.99K | ▲ 190.20% ($121,244) | ▲ 2.12% ($3,841) |
| **Discounted Revenue** | $515.09K | ▲ 166.64% ($321,914) | ▲ 1.99% ($10,055) |

#### Slicer Filters

| Filter | Options |
|--------|---------|
| **Year / Month** | Date range selector |
| **Product Category** | All categories in dataset |
| **Employees** | All employees in dataset |
| **Country** | All countries in dataset |
| **Shippers Company** | All shipping company in dataset |

#### Visuals

**Total Revenue and Sales Volume by Category — Combo Chart** *(Drill down to products)*
- Revenue bars per category overlaid with a sales volume trend line
- Beverages leads at $141K, followed by Dairy Products ($118K), Meat & Poultry ($80K), Confections ($47K), Grains & Cereals ($43K), and Produce ($42K)
- Drill-down reveals product-level revenue and volume within each category

**Avg Discount %, Sales Volume and Total Revenue by Category — Bubble Chart** *(Drill down to products)*
- Bubble size represents sales volume; x-axis is average discount %; y-axis is sales volume
- Shows how discount depth relates to volume and revenue generation per category
- Beverages and Dairy Products cluster at high volume with moderate discounts (~5.5–6%)

**Sales Volume Trend Over Time by Category — Matrix / Heatmap**
- Monthly sales volume per category displayed across 2013–2015
- Darker cells indicate higher volume; supports spotting growth periods and seasonal patterns
- Confections and Dairy Products show the most consistent volume across months

---

### 3. Regional & Operational Performance

> *Tracks regional sales, operational efficiency, and employee performance.*

<img width="1569" height="866" alt="Regional   Operational Performance Dashboard" src="https://github.com/user-attachments/assets/e493191b-4a47-4d78-91d9-2a0d36218d02" />

#### KPI Cards

| KPI | Value | YoY | MoM |
|-----|-------|-----|-----|
| **Total Orders** | 830 | ▲ 170.36% (523) | ▲ 1.72% (14) |
| **Avg Order Value** | $1.53K | ▲ 3.31% ($48.87) | ▼ 0.24% (-$3.70) |
| **Avg Delivery Delay** | 20 days | ▲ 1.67% (0.33 days) | ▼ 0.05% (0.01 days) |
| **On Time Delivery %** | 95.54% | ▲ 0.45% (0.43%) | ▲ 0.08% (0.08%) |

#### Slicer Filters

| Filter | Options |
|--------|---------|
| **Year / Month** | Date range selector |
| **Product Category** | All categories in dataset |
| **Employees** | All employees in dataset |
| **Country** | All countries in dataset |
| **Shippers Company** | All shipping company in dataset |

#### Visuals

**Avg Delivery Delay and On Time Delivery % by Month — Combo Chart** *(Drill down to quarter and year)*
- Bars show average delivery delay per month; dashed line tracks on-time delivery percentage
- MoM % change labels on each bar; supports identifying seasonal shipping degradation
- October shows the highest delivery delay spike (▲13.7% MoM)

**On Time Delivery % by Shipping Company — Bar Chart**
- Compares on-time delivery rates across the three shippers
- Federal Shipping leads at **96.47%**, followed by Speedy Express **(95.18%)** and United Package **(95.09%)**
- Identifies the most reliable logistics partner for routing decisions

**Total Revenue and Total Orders by Country — Combo Chart** *(Drill down to city)*
- Revenue bars per country overlaid with total orders trend line
- USA ($0.25M) and Germany ($0.23M) are the top two markets by revenue
- Drill-down surfaces city-level detail for targeted account planning

**Total Revenue by Employee Name — Bar Chart**
- Horizontal bar chart ranking all employees by revenue generated
- Margaret Peacock leads at **18.40%**, followed by Janet Leverling **(16.02%)** and Nancy Davolio **(15.18%)**
- Supports performance reviews, quota planning, and incentive design

---

## Key Metrics & KPIs

| KPI | Definition |
|-----|-----------|
| **Total Revenue** | Sum of all order revenue (UnitPrice × Quantity × (1 – Discount)) |
| **Active Revenue** | Revenue from orders containing currently active (non-discontinued) products |
| **Discontinued Revenue** | Revenue attributed to discontinued product lines |
| **Discounted Revenue** | Revenue from orders where a discount greater than 0% was applied |
| **Total Orders** | Count of all distinct orders placed in the selected period |
| **Avg Order Value (AOV)** | Total Revenue ÷ Total Orders |
| **Sales Volume** | Total units sold across all orders |
| **Avg Delivery Delay** | Mean number of days between required date and shipped date |
| **On Time Delivery %** | Percentage of orders shipped on or before the required date |
| **Revenue YoY** | Current period revenue vs. the same period in the prior year |
| **Revenue MoM** | Current month revenue vs. the immediately preceding month |
| **Orders YoY / MoM** | Order count change year-over-year and month-over-month |
| **Avg Discount %** | Mean discount rate applied across all discounted orders |
| **Employee Revenue %** | Each employee's revenue as a share of total team revenue |

---

## Relationship Model

| From (FK) | To (PK) | Join Column |
|-----------|---------|-------------|
| Orders.CustomerID | Customers.CustomerID | CustomerID |
| Orders.EmployeeID | Employees.EmployeeID | EmployeeID |
| Orders.ShipperID | Shippers.ShipperID | ShipperID |
| Order_Details.ProductID | Products.ProductID | ProductID |
| Products.CategoryID | Categories.CategoryID | CategoryID |
| Products.SupplierID | Suppliers.SupplierID | SupplierID |
| Orders.OrderDate | DateTable.Date | Date |

---

## Dataset Schema

| Column | Type | Description |
|--------|------|-------------|
| `OrderID` | Integer | Unique identifier for each order |
| `OrderDate` | Date | Date the order was placed |
| `RequiredDate` | Date | Date the customer required delivery |
| `ShippedDate` | Date | Actual date the order was shipped |
| `ShipperID` | Integer (FK) | References Shippers table |
| `CustomerID` | String (FK) | References Customers table |
| `EmployeeID` | Integer (FK) | References Employees table |
| `ProductID` | Integer (FK) | References Products table |
| `CategoryID` | Integer (FK) | References Categories table |
| `UnitPrice` | Decimal | Unit price at time of order |
| `Quantity` | Integer | Number of units ordered |
| `Discount` | Decimal | Discount applied (0.0 – 1.0 scale) |
| `TotalRevenue` | Decimal *(Calculated)* | UnitPrice × Quantity × (1 – Discount) |
| `DeliveryDelay` | Integer *(Calculated)* | ShippedDate – RequiredDate in days |
| `Country` | String | Country |
| `City` | String | City |
| `CompanyName` | String | Customer company name |
| `ContactName` | String | Customer contact name |
| `EmployeeName` | String | Employees names |
| `ShippingCompanyName` | String | Shipper name from Shippers table |
| `CategoryName` | String | Product category name |
| `ProductName` | String | Individual product name |
| `Discontinued` | String | Whether the product has been discontinued or active |
| `Year / Month / Quarter` | Integer / String | Date dimensions for time-intelligence DAX measures |

---

## File Structure

```
northwind-traders-dashboard/
│
├── 📊 Northwind_Traders_Dashboard.pbix     # Main Power BI file
│
├── 📁 screenshots/
│   ├── Sales___Revenue_Overview.png
│   ├── Product___Category_Intelligence_Dashboard.png
│   └── Regional___Operational_Performance_Dashboard.png
│
├── 📂 data/
│   └── Northwind_Database.xlsx             # Source data file
│
└── 📄 README.md                            # This file
```

---

## Getting Started

### Prerequisites

| Tool | Version | Purpose |
|------|---------|---------|
| [Power BI Desktop](https://powerbi.microsoft.com/desktop/) | Latest | Open & edit `.pbix` |
| Microsoft Excel | 2016+ | View/edit source dataset (if applicable) |

### Installation & Setup

1. **Clone or download the repository**
   ```bash
   git clone https://github.com/your-username/northwind-traders-dashboard.git
   cd northwind-traders-dashboard
   ```

2. **Open the dashboard**
   - Launch **Power BI Desktop**
   - Go to `File → Open` and select `Northwind_Traders_Dashboard.pbix`

3. **Verify data source connection**
   - Navigate to `Home → Transform Data → Data Source Settings`
   - Update the path to your local source dataset if prompted
   - Click `Refresh` to load the latest data

4. **Refresh data**
   ```
   Home → Refresh
   ```

---

## Usage & Filters

The dashboard includes a slicer pane on all pages supporting the following filters:

- 📅 **Year / Month** : Filter to a specific month or year range
- 🌍 **Country** : Focus on a specific geographic market
- 📦 **Product Category** : Isolate performance by category

### Navigation

Use the **left-hand page navigator** to switch between:
- `Sales & Revenue Overview` — top-line revenue, orders, and customer breakdown
- `Product & Category Intelligence` — category revenue, discount analysis, and product trends
- `Regional & Operational Performance` — shipping KPIs, country rankings, and employee performance

Use the **RESET button** (top-right of each page) to clear all active slicer selections at once.
Us the **Back button** (bottom left of each page) to retuen to the previous dashboard.

### Drill-Down Interactions

Several visuals support drill-down for deeper analysis:

| Visual | Primary Level | Drill-Down Level |
|--------|--------------|-----------------|
| Revenue & AOV by Month | Month | Quarter → Year |
| Revenue by Customer | Company Name | Contact Name |
| Revenue Contribution by Country | Country | City |
| Revenue & Volume by Category | Category Name | Product Name |
| Discount Bubble Chart | Category Name | Product Name |
| Delivery Delay & OTD % by Month | Month | Quarter → Year |
| Revenue & Orders by Country | Country | City |

> **Tip:** Click the drill-down arrow icon in the top-right corner of any visual to activate drill mode, then click a data point to go deeper. Use the **Up arrow** to return to the parent level.

---

## Insights Summary

1. **Revenue has more than doubled year-over-year** : Total revenue of $1.27M represents a **▲179.31% YoY** increase, indicating strong business growth. Order volume and sales units show comparable growth trajectories.

2. **April is the revenue peak but May–June are a cliff** : April delivers a **23.3% MoM revenue surge**, likely driven by Q2 order cycles, but is immediately followed by drops of **59.2%** and **32.4%** in May and June. This seasonal dip warrants pipeline review and promotional planning.

3. **Beverages dominates revenue, but Dairy Products wins on volume** : Beverages leads all categories at **$141K** in total revenue, yet Dairy Products generates comparable volume at **$118K** with higher per-unit sales. Produce ($42K) significantly underperforms all other categories.

4. **Discounting is driving over 40% of revenue** : Discounted revenue at **$515.09K** represents more than 40% of total revenue. While discounts drive volume, the Bubble Chart reveals diminishing returns as categories with the deepest discounts (Meat & Poultry at ~6.5%) do not proportionally outperform on volume.

5. **Discontinued products still contribute meaningfully** : $184.99K (roughly **14.6%** of total revenue) is still coming from discontinued product lines, up **190.20% YoY**. This signals that transitions off these products are incomplete and customer substitution plans may be needed.

6. **Customer concentration is a risk** : The top three customers. Quick-Stop ($110K), Ernst Handel ($105K), and Save-A-Lot Markets ($104K) represent a disproportionate share of revenue. Loss of any single account would have a material impact on the business.

7. **Logistics performance is strong** : On-time delivery sits at a healthy **95.54%**, with Federal Shipping leading at **96.47%**

8. **USA and Germany are the anchor markets** : The USA contributes **12.28%** of total revenue and Germany contributes **11.15%**, together accounting for nearly a quarter of all revenue. These two markets should be prioritized for key account management and growth investment.

9. **Top performers carry the team** : Margaret Peacock generates **18.40%** of total revenue, nearly 2.4x the contribution of the lowest performer. The top three employees (Peacock, Leverling, Davolio) collectively account for approximately **50%** of total revenue thus suggesting significant pipeline concentration at the individual level.

---

## Author

**M1deTheAnalyst**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/m1detheanalyst)
[![GitHub](https://img.shields.io/badge/GitHub-Profile-181717?style=for-the-badge&logo=github)](https://github.com/M1deTheAnalyst)
[![X](https://img.shields.io/badge/X-Folllow-000000?style=for-the-badge&logo=twitter&logoColor=white)](https://x.com/M1deTheAnalyst)

---

*Built with ❤️ using Power BI | Data-driven decisions for sales, operations, and category teams*
