# Excel_Project-Data_Analytics
Project demonstrating my Excel skills 
# 📊 Data Jobs Salary Dashboard (Excel)

## 📌 Project Overview
This project presents an **interactive Excel dashboard** analyzing global salary trends for data-related roles such as Data Analyst, Data Scientist, and Data Engineer. By exploring how job titles, geographic locations, and work schedule types influence compensation, this tool enables users to identify high-paying opportunities and regional salary patterns within the 2023 data industry.

## 🎯 Project Objective
The goal was to leverage Excel’s advanced analytical and visualization capabilities to transform raw market data into a functional business intelligence tool. This project demonstrates how data-driven insights can support strategic career decision-making.

---

## 🛠️ Tools & Excel Skills Used
-**📈 Data Visualization:** Designing interactive charts and map distributions.
-**🧮 Advanced Formulas:** Utilizing array formulas (MEDIAN, IF, FILTER) for dynamic data extraction.
-**❎ Data Validation:** Implementing dropdown filters to ensure clean, consistent user inputs.
-**🏗️ Dashboard Architecture:** Building a performance-optimized, professional layout.

---

## 📊 Dashboard Highlights
### **💰 Salary Comparison by Job Title**
A horizontal bar chart visualizes the median salary across various data roles, sorted in descending order for immediate readability.
**Key Insight:** Senior-level and engineering roles command significantly higher salary ranges compared to entry-level analyst positions.
### **🌍 Global Salary Distribution**
An interactive map chart displays median salaries by country to highlight regional disparities.
**Key Insight:** Significant variations exist globally, with regions like the USA and UK offering substantially higher compensation for data professionals.

---

## 🔎 Analytical Methodology
### **1. Dynamic Salary Calculation**
The dashboard utilizes a complex **array formula** with multiple filtering conditions to calculate median salaries based on user selections.
```excel
=MEDIAN(
  IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
  )
)
