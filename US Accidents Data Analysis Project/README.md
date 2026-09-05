# 🚗 "US Accidents Data Analysis (2016-2023):EDA & Weather Impact"

## 📌 Project Overview
This project performs an end-to-end data analysis on the **US Accidents (March 2023)** dataset.
The workflow includes **ETL (Extract, Transform, Load)** steps, followed by **Exploratory Data Analysis (EDA)** and **Weather Impact Analysis**.

The goal is to identify patterns in accident severity based on **time, location, and weather conditions**.

---

## 📂 Dataset
- **File Name:** US_Accidents_March23.csv  
- **Type:** CSV  
- **Size:** ~3GB  
- **Data Includes:**
  - Severity
  - Time features (Start_Time, End_Time)
  - Location details (State, City, Street)
  - Weather information (Temperature, Humidity, Visibility, Weather_Condition)

---

## ⚙️ Tools & Libraries Used
- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn

---

## ✅ Workflow (ETL + EDA)
### 1. Extract
- Loaded the dataset from a CSV file using Pandas.

### 2. Data Understanding
- Checked data types, columns, and summary statistics using:
  - `df.info()`
  - `df.describe()`

### 3. Data Exploration
- Analyzed missing values and duplicates.
- Checked severity distribution and categorical feature counts.

### 4. Transform
#### Data Cleaning
- Converted time columns into datetime format.
- Removed missing `Start_Time` values.
- Removed duplicate rows.
- Filled missing numeric values with **median**.
- Filled missing categorical values with **"Unknown"**.
- Dropped unimportant columns like `End_Lat` and `End_Lng`.

#### Feature Engineering
- Created:
  - Year, Month, Day, Hour, DayOfWeek
  - Accident Duration (in minutes)
  - Weekend and Night indicators

#### Outlier Detection
- Used **IQR method** to detect outliers:
  - IQR = Q3 - Q1
  - LowerBound = Q1 - 1.5 × IQR
  - UpperBound = Q3 + 1.5 × IQR
- Visualized using Box/Whisker plots.
- Capped outliers for stability.

### 5. Load
- Saved cleaned dataset to:
  - `US_Accidents_Cleaned.csv`

### 6. Analysis & Visualization
- Performed EDA using plots:
  - Severity distribution
  - Top 10 States and Cities
  - Accidents by Hour / Day of Week / Month
  - Accident Duration distribution
- Weather Impact analysis:
  - Weather_Condition vs Severity (countplot + heatmap)

---

## 📊 Key Insights
- Accidents occur more frequently during rush hours (morning & evening).
- A few states/cities contribute to a high percentage of total accidents.
- Weather conditions such as Rain, Fog, and Snow can show a higher percentage of severe accidents.
- Outliers exist in distance, duration, precipitation, and were handled using IQR method.

---

## 📁 Project Files
- `Us Accident Project.ipynb` → Full analysis notebook  
- `US_Accidents_Cleaned.csv` → Cleaned dataset output  
- `README.md` → Project documentation  



## 👨‍💻 Author
Data Analysis Project by **Prakash**
