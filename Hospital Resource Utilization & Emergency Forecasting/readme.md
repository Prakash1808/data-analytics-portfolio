# 🏥 Hospital Resource Utilization & Emergency Forecasting

## 📌 Project Overview
Hospitals operate in highly dynamic environments where sudden emergency cases, ICU bed shortages, long waiting times, and inefficient resource allocation can significantly impact patient care.

This project focuses on analyzing **hospital resource utilization** and **emergency patient demand** using a large-scale dataset. The goal is to extract meaningful insights that can help hospitals optimize resources, reduce waiting time, and improve emergency preparedness.

The project demonstrates an **end-to-end data analytics workflow** using Python and MySQL.

---

## 🎯 Business Problem
Healthcare facilities face several operational challenges:
- Unpredictable spikes in emergency cases  
- Inefficient ICU and bed allocation  
- Long patient waiting times  
- High operational and treatment costs  

**Objective:**  
To analyze hospital visit data and identify emergency trends, resource usage patterns, and key performance indicators (KPIs) that support data-driven hospital planning.

---

## 📂 Dataset Description
- **Records:** 1,000,000 (10 lakh rows)
- **Type:** Synthetic hospital visit data
- **Time Period:** Last 2 years
- **Format:** CSV
- **Target Variable:** `emergency_flag`

### Key Columns
| Column Name | Description |
|------------|------------|
| patient_id | Unique patient identifier |
| visit_date | Date of hospital visit |
| visit_time | Time of arrival |
| age | Patient age |
| gender | Patient gender |
| city | Patient city |
| department | Hospital department |
| diagnosis_type | Diagnosis category |
| triage_level | Severity level |
| wait_time_min | Waiting time (minutes) |
| treatment_time_min | Treatment duration |
| bed_required | Bed requirement (Yes/No) |
| bed_type | Bed type (ICU, General, Ventilator) |
| ambulance_used | Ambulance usage (Yes/No) |
| resource_cost_inr | Cost of treatment |
| emergency_flag | Emergency indicator (0/1) |

---

## 🔄 Data Pipeline
1. **Data Generation** using Python (Faker, NumPy)  
2. **Data Cleaning & Preprocessing**  
3. **Feature Engineering**  
4. **CSV Export**  
5. **Bulk Data Loading into MySQL**  
6. **SQL-Based KPI Analysis**  
7. **Visualization & Insights**

---

## 🛠 Tools & Technologies
- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, Faker, Matplotlib  
- **Database:** MySQL 8.0  
- **SQL Concepts:** DDL, Bulk Load, Indexing, Aggregations  
- **Environment:** Jupyter Notebook / VS Code  
- **Version Control:** Git & GitHub  

---

## 🧹 Data Cleaning & Feature Engineering
- Removed duplicate records  
- Converted date and time fields into proper formats  
- Handled categorical variables  
- Created additional features:
  - Visit hour  
  - Day of week  

---

## 📊 Key Performance Indicators (KPIs)
- Average waiting time by triage level  
- Emergency cases by department  
- ICU and bed utilization trends  
- Ambulance usage percentage  
- Department-wise resource cost  

---

## 📈 Key Insights
- Emergency department handles the highest patient inflow  
- Critical cases have the longest waiting and treatment times  
- ICU demand increases during weekends and evening hours  
- Accident-related cases show higher ambulance usage  
- High-severity cases contribute most to total hospital cost  

---

## ✅ Recommendations
- Increase ICU capacity during peak hours  
- Optimize doctor scheduling during evenings and weekends  
- Maintain buffer emergency beds  
- Improve ambulance availability in accident-prone zones  
- Use predictive analytics for emergency preparedness  

---
## 🏆 Key Learning Outcomes
- Handling large datasets (1M+ records)  
- End-to-end data analytics pipeline  
- SQL-based performance analysis  
- Healthcare domain analytics experience  

---

## 📌 Conclusion
This project demonstrates how data analytics can support hospitals in making informed decisions related to emergency pr
