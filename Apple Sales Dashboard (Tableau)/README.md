# 🏥 Hospital Resource Utilization & Patient Flow Analytics

### Python & MySQL | Exploratory Data Analysis | Data Analytics Portfolio Project

## 🔍 Project Overview

**Hospital Resource Utilization & Patient Flow Analytics** is a Python-based data analytics project developed to analyze patient visits, departmental workloads, waiting times, treatment durations, and hospital resource costs.

The project analyzes **1,000,000 hospital visit records** retrieved from a MySQL database using Python, Pandas, NumPy, Matplotlib, and Seaborn.

After resource-cost outlier filtering, **999,358 records** were retained for exploratory analysis.

The analysis helps identify patterns in hospital operations, patient flow, and resource utilization, providing a foundation for data-driven healthcare planning.

## 🎯 Business Objectives

- Analyze patient visit patterns across hospital departments.
- Examine waiting times and treatment durations.
- Explore resource costs and their relationship with visit duration.
- Compare resource costs across patient age groups.
- Identify high-volume hospital departments.
- Examine monthly patient visit trends.
- Support exploratory, data-driven hospital resource planning.

## 📁 Dataset Overview

| Attribute | Details |
|---|---|
| Total Original Records | 1,000,000 |
| Records After Filtering | 999,358 |
| Records Removed | 642 |
| Date Range | February 2024 – February 2026 |
| Data Source | MySQL |
| Database Table | `hospital_resource` |
| Dataset Type | Synthetic hospital visit data (as described in project brief) |
| Main Dimensions | Department, Age, Gender, City, Diagnosis, Triage Level |
| Main Measures | Waiting Time, Treatment Time, Resource Cost, Total Time |

### Key Dataset Columns

| Column | Description |
|---|---|
| `patient_id` | Patient identifier |
| `visit_date` | Hospital visit date |
| `visit_time` | Patient arrival time |
| `age` | Patient age |
| `gender` | Patient gender |
| `city` | Patient city |
| `department` | Hospital department |
| `diagnosis_type` | Diagnosis category |
| `triage_level` | Patient severity category |
| `wait_time_min` | Waiting time in minutes |
| `treatment_time_min` | Treatment duration in minutes |
| `bed_required` | Bed requirement field |
| `bed_type` | ICU, General, Ventilator or no bed |
| `ambulance_used` | Ambulance usage indicator |
| `resource_cost_inr` | Resource cost in INR |
| `emergency_flag` | Emergency classification indicator |

## 🧹 Data Preparation & Validation

The analytical workflow included:

- Loading hospital records from MySQL using SQLAlchemy and Pandas.
- Converting `visit_date` into a datetime format.
- Checking missing values using `isna().sum()`.
- Identifying and filtering high resource-cost outliers using the Interquartile Range (IQR) method.
- Creating `total_time` from waiting and treatment durations.
- Creating patient age groups using `pd.cut()`.
- Mapping ambulance usage values from Yes/No to numeric indicators.
- Reviewing descriptive statistics and categorical distributions.

### Feature Engineering

**Total Time**

`total_time = wait_time_min + treatment_time_min`

**Age Groups**

| Age Group | Age Range |
|---|---|
| Child | 1–18 |
| Young | 19–35 |
| Adult | 36–60 |
| Senior | 61–120 |

The saved notebook output also includes `visit_month` and `visit_day`. Their creation code needs to be added to the notebook to reproduce the monthly analysis in a fresh session.

## 📊 Key Performance Indicators

The following values are based on saved outputs in the uploaded Jupyter notebook.

| KPI | Overall Result |
|---|---:|
| Total Original Records | 1,000,000 |
| Total Analyzed Records | 999,358 |
| Average Waiting Time | 61.52 minutes |
| Average Treatment Time | 1,049.99 minutes |
| Average Total Time | 1,111.50 minutes |
| Average Resource Cost | ₹170.96 |
| Emergency Department Records | 350,233 |
| Emergency Department Share | 35.05% |
| Most Frequent City | Bangalore |
| Most Frequent Diagnosis | Accident |

### KPI Definitions

**Average Waiting Time**

Total Waiting Time ÷ Total Analyzed Records

**Average Resource Cost**

Total Resource Cost ÷ Total Analyzed Records

**Average Total Time**

Total Combined Time ÷ Total Analyzed Records

**Department Visit Share (%)**

Department Visit Count ÷ Total Analyzed Records × 100

**Interpretation Note:** These results describe recorded values in the dataset. They should not be considered validated real-world healthcare benchmarks or evidence of clinical performance.

## 📈 Data Visualizations

The Jupyter notebook contains three exploratory visualizations.

**1. Total Time vs Resource Cost**

A scatter plot examining the relationship between combined waiting/treatment time and recorded hospital resource cost.

**2. Resource Cost by Age Group**

A box plot comparing resource-cost distributions among Child, Young, Adult, and Senior patients.

**3. Monthly Visit Trend**

A line chart displaying patient visit counts by calendar month.

The monthly visualization groups visits by month number across years rather than displaying a continuous year-month timeline.

## 💡 Key Analytical Findings

**1. Emergency is the highest-volume hospital department.**

The Emergency department accounts for **350,233 records**, approximately **35.05%** of the analyzed dataset.

**2. Average waiting time is approximately one hour.**

The overall average waiting time is **61.52 minutes**, providing a baseline for evaluating patient flow.

**3. Accident is the most frequent diagnosis category.**

Accident-related visits account for **221,205 records**, approximately **22.13%** of analyzed visits.

**4. Bangalore has the highest recorded city frequency.**

Bangalore accounts for **200,330 records**, approximately **20.05%** of the analyzed dataset.

**5. Average resource cost is ₹170.96.**

The notebook reports an average resource cost of ₹170.96 and explores variation across total visit time and patient age categories.

These findings are descriptive and do not establish causal relationships or independently validated hospital resource requirements.

## 🛠 Tools & Technologies

**Programming Language:** Python

**Database:** MySQL

**Python Libraries:** Pandas, NumPy, Matplotlib, Seaborn, SQLAlchemy, PyMySQL

**Development Environment:** Jupyter Notebook

**Analytical Techniques:** Data Cleaning, Outlier Detection, Feature Engineering, Descriptive Statistics, Exploratory Data Analysis, Data Visualization

## 🔄 Project Workflow

1. **Data Extraction** — Retrieve hospital records from MySQL.
2. **Data Validation** — Inspect field types and missing values.
3. **Data Cleaning** — Filter high resource-cost outliers.
4. **Feature Engineering** — Calculate total time and categorize patient ages.
5. **Exploratory Data Analysis** — Examine distributions and summary metrics.
6. **Data Visualization** — Create scatter, box, and line plots.
7. **Insight Generation** — Summarize descriptive operational patterns.

## ⚠️ Analytical Limitations & Future Scope

The notebook establishes a foundation for hospital resource analytics, but several areas require additional work:

- The notebook does not currently implement an emergency-demand forecasting model.
- The saved descriptive statistics show `emergency_flag` equal to zero for the retained records, requiring investigation before emergency prediction.
- Bed requirement and ambulance usage fields need validation before calculating utilization KPIs.
- Month and day feature-generation cells should be included for reproducibility.
- Year-month trends would provide a more useful view of changing patient demand.
- Reproducing the analysis requires access to the underlying MySQL data.

**Potential Enhancements**

- Department-wise waiting time analysis.
- Triage-level patient flow analysis.
- ICU and bed utilization KPIs after data validation.
- Emergency demand forecasting using properly validated historical data.
- An interactive hospital operations dashboard.

## 🚀 Project Outcome

Developed a Python and MySQL analytics project demonstrating the ability to:

- Work with large-scale structured datasets.
- Retrieve database records using Python.
- Perform data cleaning and outlier filtering.
- Engineer analytical variables.
- Calculate and interpret descriptive KPIs.
- Visualize hospital operational patterns.
- Communicate analytical findings and limitations.


## 📂 Project File

**Hospital Data Analysis .ipynb**

Contains Python code, saved analytical outputs, exploratory visualizations, and project discussion.

## 👤 Author

**Prakash Ananda Shelake**

Data Analyst | SQL | Python | Power BI | Tableau | Advanced Excel

GitHub: [Prakash1808](https://github.com/Prakash1808)
