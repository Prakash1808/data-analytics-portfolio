# 📊 INSURE-IQ | Insurance Portfolio & Claims Analytics

### Interactive Excel Dashboard | Data Analytics Portfolio Project

## 🔍 Project Overview

**INSURE-IQ** is an interactive insurance analytics dashboard developed in Microsoft Excel to analyze policy distribution, premium performance, claims activity, and insurance portfolio KPIs.

The project analyzes **10,000 insurance policy records** using Excel Tables, PivotTables, PivotCharts, Power Pivot/DAX measures, slicers, and dynamic KPI reporting.

The dashboard enables users to explore insurance performance across policy types, customer age groups, gender, claim statuses, and policy years.

## 🎯 Business Objectives

- Analyze insurance policy distribution across different policy types.
- Track premium amounts and claims-to-premiums ratios.
- Examine recorded claims and claim rates.
- Compare customer demographics and claim-status patterns.
- Evaluate average premium per policy.
- Provide interactive, filter-driven portfolio insights.

## 📁 Dataset Overview

| Attribute | Details |
|---|---|
| Total Records | 10,000 |
| Policy Types | Auto, Health, Home, Life, Travel |
| Policy Years | 2023–2024 |
| Claim Statuses | Pending, Rejected, Settled |
| Main Dimensions | Policy Type, Age Group, Gender, Claim Status, Policy Year |
| Main Measures | Premium Amount, Claim Amount, Policy Count, Recorded Claims |

## 🧹 Data Preparation & Validation

The analytical preparation involved:

- Reviewing column formats, date fields, and categorical values.
- Checking policy identifiers for uniqueness.
- Examining missing and placeholder claim dates.
- Validating claim-count logic using `ClaimFlag`.
- Reviewing policy-year and age-group information.
- Using an Excel Data Model for reusable KPI calculations.
- Replacing incorrectly summed row-level ratios with aggregate claims-to-premiums calculations.

## 📈 Key Performance Indicators

| KPI | Overall Result |
|---|---:|
| Total Policies | 10,000 |
| Total Premium Amount | ₹5.97M |
| Total Claim Amount | ₹16.90M |
| Recorded Claims | 5,646 |
| Claim Rate | 56.46% |
| Claims / Premiums Ratio | 282.96% |
| Average Premium per Policy | ₹597.41 |

### KPI Definitions

**Claim Rate (%)**

Recorded Claims ÷ Total Policies × 100

**Claims / Premiums (%)**

Total Claim Amount ÷ Total Premium Amount × 100

**Average Premium per Policy**

Total Premium Amount ÷ Total Policies

The measures recalculate according to the selected dashboard filters.

**Interpretation note:** The claims-to-premiums calculation includes amounts associated with pending claims in the supplied dataset. It is a portfolio comparison measure and should not be interpreted as a verified actuarial incurred-loss ratio or a real insurer's financial performance.

## 📊 Dashboard Visualizations

The dashboard includes:

1. **Monthly Premium** — Premium trends by calendar month.
2. **Status Distribution** — Policy record distribution by claim status.
3. **Policies by Type** — Policy counts across five insurance categories.
4. **Premium by Age** — Premium amount by age group.
5. **Policies by Age Group** — Customer policy distribution across age groups.
6. **Premium vs Claims** — Comparison of premium and claim amounts by policy type.
7. **Claims / Premiums %** — Aggregate ratio by policy type.
8. **Status by Gender** — Claim-status distribution across gender categories.
9. **Average Premium per Policy** — Average premium comparison by policy type.
10. **Recorded Claims by Type** — Records flagged as claims across policy categories.

## 🎛 Interactive Features

Five slicers allow users to filter the dashboard by:

- Gender
- Age Group
- Claim Status
- Policy Type
- Policy Year

The dashboard includes a dynamic **Portfolio Insights** section that displays:

- Top Policy Type
- Recorded Claims
- Highest Claims / Premiums Ratio

All three insights are linked to filtered PivotTable results and update when slicer selections change.

## 💡 Key Analytical Findings

**1. Travel insurance leads policy volume.**

Travel represents 4,145 policy records, accounting for 41.45% of the portfolio.

**2. Recorded claims account for 56.46% of policy records.**

A total of 5,646 records are flagged as claims out of 10,000 policy records.

**3. Claims exceed premium amounts in the dataset.**

The overall claims-to-premiums ratio is approximately 282.96%.

**4. Travel has the highest claims-to-premiums ratio among the five policy types.**

Its ratio is approximately 286.34% in the unfiltered data.

These findings describe patterns in the supplied dataset and do not establish causation or independently validated insurance risk.

## 🛠 Tools & Technical Skills

**Microsoft Excel | Excel Tables | Data Cleaning | PivotTables | PivotCharts | Power Pivot | DAX Measures | Slicers | GETPIVOTDATA | KPI Reporting | Business Intelligence | Data Visualization**

## 📂 Workbook Structure

**Data:** Source policy records and data fields.

**Analysis:** PivotTables, calculated measures, and supporting dashboard calculations.

**Dashboard:** Interactive KPI cards, charts, slicers, and dynamic portfolio insights.

## 🚀 Project Outcome

Developed an interactive Excel analytics dashboard that demonstrates the ability to:

- Organize and analyze structured business data.
- Build reusable analytical measures.
- Create interconnected PivotTables and PivotCharts.
- Calculate and interpret portfolio KPIs.
- Communicate business findings through interactive visualizations.


## 👤 Author

**Prakash Ananda Shelake**

Data Analyst | SQL | Python | Power BI | Tableau | Advanced Excel

GitHub: [Prakash1808](https://github.com/Prakash1808)
