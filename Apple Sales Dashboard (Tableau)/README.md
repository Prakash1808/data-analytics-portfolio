# 🍎 APPLE SALES ANALYTICS | Global Sales, Product & Warranty Intelligence

### Interactive Tableau Dashboard | Sales & Retail Analytics Portfolio Project

## 🔍 Project Overview

**Apple Sales Analytics** is an interactive Tableau business intelligence project developed to analyze global sales performance, product and store contributions, geographical trends, and warranty claims.

The project analyzes **1,040,200 sales records** and **30,000 warranty claims** across **10 product categories, 89 products, 75 stores, 47 cities, and 19 countries**.

The sales dataset covers **2020–2024**, with records from January 1, 2020, through November 12, 2024.

The project uses **Tableau Relationships, Calculated Fields, KPI Cards, Interactive Filters, Geographic Maps, and Data Visualizations** to provide insights into retail performance.

Three analytical dashboards enable users to explore revenue, product performance, store performance, warranty claims, and geographical sales patterns.

## 🎯 Business Objectives

- Analyze overall revenue and sales performance.
- Track units sold, total orders, and average order metrics.
- Identify top-performing product categories.
- Examine monthly revenue and sales quantity trends.
- Compare revenue contributions across categories.
- Analyze city-wise and country-wise sales performance.
- Track warranty claims and claim rates.
- Compare warranty claim patterns across product categories and countries.
- Provide interactive, filter-driven business insights.

## 📁 Dataset Overview

The project uses five interconnected CSV datasets.

| Dataset | Records | Description |
|---|---:|---|
| `sales.csv` | 1,040,200 | Sales transactions and quantities |
| `products.csv` | 89 | Product information and prices |
| `category.csv` | 10 | Product category details |
| `stores.csv` | 75 | Store and geographical information |
| `warranty.csv` | 30,000 | Warranty claims and repair statuses |

### Key Dataset Columns

| Dataset | Main Columns |
|---|---|
| Sales | sale_id, sale_date, store_id, product_id, quantity |
| Products | Product_ID, Product_Name, Category_ID, Launch_Date, Price |
| Category | category_id, category_name |
| Stores | Store_ID, Store_Name, City, Country |
| Warranty | claim_id, claim_date, sale_id, repair_status |

### Dataset Coverage

| Attribute | Details |
|---|---|
| Total Sales Records | 1,040,200 |
| Total Warranty Claims | 30,000 |
| Product Categories | 10 |
| Products | 89 |
| Stores | 75 |
| Cities | 47 |
| Countries | 19 |
| Sales Period | 2020–2024 |

### Product Categories

The dataset contains ten product categories:

1. Laptop
2. Audio
3. Tablet
4. Smartphone
5. Wearable
6. Streaming Device
7. Desktop
8. Subscription Service
9. Smart Speaker
10. Accessories

## 🔗 Data Modeling & Relationships

The project uses Tableau's relational data model to connect the five datasets.

### Tableau Data Model

![Tableau Data Model](assets/tableau-data-model.png)

**Primary Fact Table:** `sales.csv`

**Dimension Tables:** `products.csv`, `category.csv`, `stores.csv`

**Warranty Claims Table:** `warranty.csv`

### Table Relationships

| Primary Table | Related Table | Relationship Key |
|---|---|---|
| Sales | Products | product_id = Product_ID |
| Products | Category | Category_ID = category_id |
| Sales | Stores | store_id = Store_ID |
| Sales | Warranty | sale_id = sale_id |

The relationships allow sales, product, category, geographical, and warranty information to be analyzed together.

The supplied data has one-to-many relationships from categories to products, products to sales, and stores to sales. Each sale has zero or one linked warranty claim in the supplied records.

## 🧹 Data Preparation & Validation

The data preparation and analytical validation included:

- Loading all five CSV datasets into Tableau.
- Establishing relationships using matching identifier fields.
- Reviewing column names and data types.
- Validating identifiers and cross-table relationships.
- Examining missing values and duplicate identifiers.
- Converting and interpreting date fields.
- Creating revenue calculations using product prices and sales quantities.
- Extracting sale year and calendar month for trend analysis.
- Using geographical dimensions for city-level and country-level analysis.
- Creating calculated KPI measures.

### Data Validation Results

The supplied CSV files contain:

- **1,040,200 unique sale IDs.**
- **30,000 unique warranty claim IDs.**
- No missing values in the source columns.
- No duplicate primary identifiers.
- No unmatched product, category, store, or sale relationship keys.

### Calculated Measures

**Total Revenue**

Sum of Quantity × Product Price

**Total Units Sold**

Sum of Quantity

**Total Orders**

Distinct Count of Sale ID

**Average Order Size**

Total Units Sold ÷ Total Orders

**Revenue per Order**

Total Revenue ÷ Total Orders

**Claim Rate (%)**

Total Warranty Claims ÷ Total Sales Orders × 100

**Revenue Contribution (%)**

Category Revenue ÷ Total Revenue × 100

**Note:** Revenue is calculated from the dataset's product prices and recorded quantities. The source does not provide transaction-level discounts, tax, or refunds.

## 📊 Key Performance Indicators

### Sales Performance KPIs

| KPI | Overall Result |
|---|---:|
| Total Revenue | **$6.17B** |
| Total Units Sold | **5.72M** |
| Total Orders | **1.04M** |
| Average Order Size | **5.50** |
| Total Revenue per Order | **$5.93K** |

The underlying dataset calculations produce:

- Total Revenue: **$6,166,293,030**
- Total Units Sold: **5,721,344**
- Total Orders: **1,040,200**

### Warranty & Claims KPIs

| KPI | Overall Result |
|---|---:|
| Total Warranties | **1.04M** |
| Active Warranties | **214.82K** |
| Expired Warranties | **825.39K** |
| Total Claims | **30.00K** |
| Claim Rate | **2.88%** |

### Warranty Status Distribution

| Warranty Status | Percentage |
|---|---:|
| Active | 20.65% |
| Expired | 79.35% |

**Interpretation note:** The dashboard's Total Warranties KPI represents the sales-record population. The separate warranty claims table contains 30,000 claim records.

Active and expired warranty statuses are calculated dashboard classifications, not explicit source CSV columns. The dataset also contains a separate `repair_status` field for claim processing.

## 📈 Dashboard Visualizations

The Tableau project contains three analytical dashboard pages.

### 1. Executive Sales Overview

![Executive Sales Overview](assets/executive-sales-overview.png)

This dashboard provides an executive-level summary of global Apple product sales.

**Visualizations:**

1. **Revenue by Category** — Ranking of product categories based on generated revenue.
2. **Sales Trend – Revenue** — Monthly revenue trends across the dataset.
3. **Sales Trend – Units** — Monthly product sales volume.
4. **Sales by Country** — Geographic distribution of revenue using a filled map.

**KPI Cards:**

- Total Revenue
- Total Units Sold
- Total Orders
- Average Order Size
- Total Revenue per Order

### 2. Product & Store Performance

![Product and Store Performance](assets/product-store-performance.png)

This dashboard focuses on product category contributions, sales quantity, and geographical market performance.

**Visualizations:**

1. **Revenue Contribution % by Category** — Percentage contribution of each product category to total revenue.
2. **Top Cities by Revenue** — Comparison of revenue generated across major cities.
3. **Units Sold by Category** — Sales volume comparison across the ten product categories.
4. **Revenue vs Quantity** — Scatter plot exploring the relationship between sales quantities and revenue.

### 3. Warranty & Claims Analysis

![Warranty and Claims Analysis](assets/warranty-claims-analysis.png)

This dashboard analyzes warranty coverage classifications and claims across sales years, product categories, and countries.

**Visualizations:**

1. **Claim Rate Trend** — Annual claim-rate patterns grouped by year of sale.
2. **Claims by Country** — Country-wise comparison of claim rates.
3. **Claims by Category** — Product-category-wise claim rate analysis.
4. **Warranty Status Distribution** — Percentage distribution of active and expired warranties.

**KPI Cards:**

- Total Warranties
- Active Warranties
- Expired Warranties
- Total Claims
- Claim Rate

The claim-rate trend uses sale years from 2020–2024. Claim dates recorded in `warranty.csv` fall in 2024.

## 🎛 Interactive Dashboard Features

The Tableau dashboard provides four filtering dimensions.

**1. Category Name**

Analyze sales and warranty metrics for selected product categories.

**2. Year of Sale**

Explore performance across sales years from 2020 to 2024.

**3. Country**

Filter analytical results by individual countries.

**4. City**

Examine city-level sales and claims patterns.

The dashboard screenshots display the unfiltered **(All)** selections.

The analytical views use Tableau relationships, calculated metrics, geographic visualizations, and filters to support portfolio exploration.

## 💡 Key Analytical Findings

### 1. Tablets generate the highest revenue.

The Tablet category contributes approximately **$953.44M**, representing **15.46%** of total revenue.

The next leading categories are:

| Category | Revenue | Contribution |
|---|---:|---:|
| Tablet | $953.44M | 15.46% |
| Accessories | $927.12M | 15.04% |
| Smartphone | $865.15M | 14.03% |
| Audio | $794.98M | 12.89% |
| Laptop | $763.38M | 12.38% |

The top three categories contribute approximately **44.5%** of total revenue.

### 2. Accessories lead in total units sold.

Accessories record approximately **899.73K units sold**, followed by:

- Smartphone: **834.01K**
- Audio: **707.35K**
- Tablet: **645.30K**
- Desktop: **642.14K**

This demonstrates that the highest-volume category is not necessarily the highest-revenue category.

### 3. The United States is the largest country market.

The United States generates approximately **$1.23B** in revenue, contributing about **20%** of the total calculated revenue.

Other major revenue markets include Australia, China, Japan, and the UAE.

### 4. Dubai is the highest-revenue city.

The top revenue-generating cities are:

| City | Revenue |
|---|---:|
| Dubai | $329.42M |
| London | $328.97M |
| Paris | $325.66M |
| New York | $249.14M |
| Melbourne | $247.98M |
| Tokyo | $246.18M |

Dubai leads the analyzed city markets, followed closely by London and Paris.

### 5. March generates the highest aggregated monthly revenue.

March records approximately **$542.79M** in revenue and **503.68K** units sold when calendar months are aggregated across the dataset's years.

December shows approximately **$425.34M**, the lowest monthly total in the displayed trend.

The 2024 data ends on November 12, so monthly comparisons do not represent equally complete calendar-year coverage.

### 6. Overall warranty claim rate is 2.88%.

A total of **30,000 claims** are linked to **1,040,200 sales records**.

The claim rate indicates the share of sales records with associated warranty claims.

### 7. Smart Speaker has the highest category claim rate.

The Smart Speaker category records approximately **2.95%**, followed by:

| Product Category | Claim Rate |
|---|---:|
| Smart Speaker | 2.95% |
| Audio | 2.93% |
| Smartphone | 2.92% |
| Subscription Service | 2.91% |
| Laptop | 2.91% |

These category rates are relatively close and do not independently establish differences in product reliability.

### 8. Austria has the highest country claim rate.

Austria records approximately **3.25%**, followed by:

- Netherlands: **3.06%**
- Taiwan: **3.00%**
- UAE: **2.95%**
- United States: **2.93%**

### 9. Expired warranties dominate the calculated distribution.

The warranty dashboard classifies **79.35%** of sales records as expired and **20.65%** as active.

This reflects the dashboard's calculated classification and is not independently verified against contractual warranty-expiration dates.

## 🛠 Tools & Technical Skills

**Tableau | Tableau Relationships | Calculated Fields | Data Modeling | Data Validation | KPI Reporting | Sales Analytics | Retail Analytics | Geographic Mapping | Trend Analysis | Warranty Analytics | Business Intelligence | Data Visualization**

## 📂 Repository Structure

The GitHub project contains the README, source datasets, and dashboard screenshots.

```text
APPLE_Sales_Analytics_Tableau/
├── README.md
├── data/
│   ├── category.csv
│   ├── products.csv
│   ├── sales.csv
│   ├── stores.csv
│   └── warranty.csv
└── assets/
    ├── executive-sales-overview.png
    ├── product-store-performance.png
    ├── warranty-claims-analysis.png
    └── tableau-data-model.png
```

The supplied project package includes the datasets and screenshots. An editable Tableau workbook (`.twb` or `.twbx`) is not included.

## 🚀 Project Outcome

Developed an interactive Tableau sales analytics project demonstrating the ability to:

- Work with large-scale sales and claims datasets.
- Design a multi-table relational data model.
- Validate relationships and source data.
- Create reusable business KPI calculations.
- Develop executive-level analytical dashboards.
- Analyze product and store performance.
- Compare geographical sales distributions.
- Examine warranty and claims patterns.
- Communicate analytical findings using interactive data visualizations.

The project demonstrates practical skills in **Tableau, Data Modeling, KPI Development, Business Intelligence, and Sales Analytics**.

## 👤 Author

**Prakash Ananda Shelake**

Data Analyst | SQL | Python | Power BI | Tableau | Advanced Excel

**GitHub:** [Prakash1808](https://github.com/Prakash1808)
