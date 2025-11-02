# 💼 Job Market Analysis SQL and Power BI Project

This project presents a comprehensive **Job Market Analysis Dashboard** built using **Microsoft Power BI**.  
The dashboard provides insights into job availability, salary distribution, employment types, and hiring trends across different platforms.

---

## 📊 Dashboard Overview

![Job Market Analysis Dashboard](../Project%20Job%20analysis.jpg)

### 🔍 Key Insights
- **Job Applications by Platform:**  
  Visual comparison of job postings from Indeed, LinkedIn, and Glassdoor.
- **Day-wise Job Trends:**  
  Tracks how many jobs were posted each day, revealing hiring spikes and drops.
- **Commute Time vs Job Type:**  
  Average salary comparison across Contract, Full-time, and Part-time schedules with work-from-home variations.
- **Salary Tier Distribution:**  
  Displays the proportion of jobs across Low, Medium, and High salary categories.
- **Top Salary Titles and Companies:**  
  Highlights highest-paying job titles such as *Cloud Security Architect* and companies like *SecureCloud Designs*.
- **Salary Rate Comparison:**  
  Average salary by payment rate (hourly vs yearly).

---

## 🧠 Skills & Tools Used

| Category | Details |
|-----------|----------|
| **Data Source** | SQL database|
| **Tools** | Power BI Desktop, DAX, Power Query |
| **Techniques** | Data Cleaning, Modeling, DAX Measures, Visualization |
| **Visualization Types** | Bar Chart, Line Chart, Donut Chart, Table, KPI Cards |

---
## 📊 Dashboard Preview
![Job Market Analysis Dashboard](https://github.com/DinakarShetty/Job-Market-Analysis/blob/main/Project%20Job%20analysis.jpg)

## ⚙️ Data Modeling & DAX Examples

### Power Query Transformations
- Removed null values and duplicates.  
- Standardized salary fields into a single column `salary_standardized`.  
- Added calculated columns for `SalaryTier` (Low, Medium, High).

### DAX Measures
DAX
Average Salary = AVERAGE(JOBS_DATA[salary_standardized])

High Salary % =
DIVIDE(
    CALCULATE(COUNTROWS(JOBS_DATA), JOBS_DATA[SalaryTier] = "HIGH"),
    COUNTROWS(JOBS_DATA)
)

Average Salary by Rate =
CALCULATE(
    AVERAGE(JOBS_DATA[salary_standardized]),
    ALLEXCEPT(JOBS_DATA, JOBS_DATA[salary_rate])
)


🧑‍💻 Author

Dinakar Shetty
Business & Data Analyst | Power BI | SQL | Excel | Python
📧 Email: dinakar.shetty2@gmail.com

