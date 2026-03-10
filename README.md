# Excel_Project-Data_Analytics
Project demonstrating my Excel skills 
# 📊 Data Jobs Salary Dashboard (Excel)

## 📌 Project Overview
[cite_start]This project presents an **interactive Excel dashboard** analyzing global salary trends for data-related roles such as Data Analyst, Data Scientist, and Data Engineer[cite: 1, 3]. [cite_start]By exploring how job titles, geographic locations, and work schedule types influence compensation, this tool enables users to identify high-paying opportunities and regional salary patterns within the 2023 data industry[cite: 4, 5].

## 🎯 Project Objective
[cite_start]The goal was to leverage Excel’s advanced analytical and visualization capabilities to transform raw market data into a functional business intelligence tool[cite: 7]. [cite_start]This project demonstrates how data-driven insights can support strategic career decision-making[cite: 75].

---

## 🛠️ Tools & Excel Skills Used
* [cite_start]**📈 Data Visualization:** Designing interactive charts and map distributions[cite: 29].
* [cite_start]**🧮 Advanced Formulas:** Utilizing array formulas (MEDIAN, IF, FILTER) for dynamic data extraction[cite: 30, 46].
* [cite_start]**❎ Data Validation:** Implementing dropdown filters to ensure clean, consistent user inputs[cite: 31, 63].
* [cite_start]**🏗️ Dashboard Architecture:** Building a performance-optimized, professional layout[cite: 32].

---

## 📊 Dashboard Highlights
### **💰 Salary Comparison by Job Title**
[cite_start]A horizontal bar chart visualizes the median salary across various data roles, sorted in descending order for immediate readability[cite: 35, 38].
* [cite_start]**Key Insight:** Senior-level and engineering roles command significantly higher salary ranges compared to entry-level analyst positions[cite: 37, 72].

### **🌍 Global Salary Distribution**
[cite_start]An interactive map chart displays median salaries by country to highlight regional disparities[cite: 40].
* [cite_start]**Key Insight:** Significant variations exist globally, with regions like the USA and UK offering substantially higher compensation for data professionals[cite: 42, 43].

---

## 🔎 Analytical Methodology
### **1. Dynamic Salary Calculation**
[cite_start]The dashboard utilizes a complex **array formula** with multiple filtering conditions to calculate median salaries based on user selections[cite: 46, 57].

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
