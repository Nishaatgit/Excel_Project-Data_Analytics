# 📊 Data Science Job Market Analysis (Excel)
## 📌 Project Overview

As a job seeker, I noticed a significant lack of centralized data exploring the most optimal roles and skills in the modern data science market. This project aims to uncover valuable insights into how skills impact pay, regional salary disparities, and the specific technical requirements of top employers.

---

## 📑 Table of Contents

* 📌 Project Overview](#-project-overview)
* Questions to Analyze](#-questions-to-analyze)
* 🛠️ Tech Stack \& Skills](#-tech-stack--skills)
* 📊 Data Pipeline (ETL)](#-data-pipeline-etl)
* 🏗️ Data Modeling \& DAX](#-data-modeling--dax)
* 📈 Key Insights](#-key-insights)
* 📝 Conclusion](#-conclusion)

---

## ❓ Questions to Analyze

To understand the data science job market, the analysis focuses on four core areas:

1.  **Skill-Pay Correlation:** Determining if a higher number of specialized skills leads to better compensation.

2.  **Regional Variation:** Benchmarking median salaries across different geographic regions.

3.  **In-Demand Tools:** Identifying the top technical skills requested by employers today.

4.  **Top Skill Compensation:** Calculating the specific pay associated with the top 10 industry skills.

---

## 🛠️ Tech Stack & Skills

* **Power Query:** Used for end-to-end ETL (Extract, Transform, Load) processes.

* **Power Pivot:** For building relational data models between disparate datasets.

* **DAX (Data Analysis Expressions):** To create custom measures for complex median salary calculations.

* **PivotTables & Charts:** For interactive data exploration and trend visualization.

---

## 📊 Data Pipeline (ETL)

The data preparation was handled entirely within **Power Query** to ensure a clean foundation for analysis.

* **Extraction:** Raw data was pulled from `data_salary_all.xlsx` into two primary queries: `data_jobs_all` and `data_job_skills`.

* **Transformation:** Key steps included trimming excess whitespace, capitalizing skill text for uniformity, and removing unnecessary columns to optimize performance.

---

## 🏗️ Data Modeling & DAX

A relational schema was established using **Power Pivot** to connect job attributes with specific skill requirements.

* **Data Model:** Created a 1-to-many relationship using the `job_id` column as the primary key.

* **DAX Measures:** Developed measures to calculate median year salaries, allowing for dynamic filtering by country and role.



**dax**
-- DAX Measure for Median Salary

Median Salary := ```MEDIAN(data_jobs_all[salary_year_avg])```

---

## 📈 Key Insights

* **Positive Correlation:** There is a direct link between the number of skills in a job posting and the offered salary, particularly for Senior Data Engineers and Data Scientists.

* **Market Value:** High-tech hubs in the US continue to command significantly higher median salaries compared to international roles.

* **High-Value Skills:** Mastery of Python and SQL remains the most reliable pathway to maximizing salary outcomes in the tech sector.



## 📝 Conclusion

This project serves as a practical guide for data professionals to align their expertise with current market standards. By utilizing advanced Excel features, the analysis proves that specialized skill sets—particularly in cloud technologies and core programming—command the highest market value.


