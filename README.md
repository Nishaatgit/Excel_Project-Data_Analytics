# Excel_Project-Data_Analytics
Project demonstrating my Excel skills 
# 📊 Data Jobs Salary Dashboard (Excel)
[Checkout_my_work_here](Salary_Dashboard_project1.xlsx)

## 📌 Project Overview
This project presents an **interactive Excel dashboard** analyzing global salary trends for data-related roles such as Data Analyst, Data Scientist, and Data Engineer. By exploring how job titles, geographic locations, and work schedule types influence compensation, this tool enables users to identify high-paying opportunities and regional salary patterns within the 2023 data industry.
![Final_Salary_Dashboard](https://github.com/user-attachments/assets/448e488d-3a2a-4df9-8a9e-2a18040c695b)


## 🎯 Project Objective
The goal was to leverage Excel’s advanced analytical and visualization capabilities to transform raw market data into a functional business intelligence tool. This project demonstrates how data-driven insights can support strategic career decision-making.

---

## 🛠️ Tools & Excel Skills Used
- **📈 Data Visualization:** Designing interactive charts and map distributions using Pivot charts.
- **🧮 Advanced Formulas and Functions:** Utilizing array formulas (MEDIAN, IF, FILTER) for dynamic data extraction.
- **❎ Data Validation:** Implementing dropdown filters to ensure clean, consistent user inputs.
- **🏗️ Dashboard Architecture:** Building a performance-optimized, professional layout.
- ** Git & GitHub:** For version control and sharing my analysis.

---

## 📊 Dashboard Build & Highlights
### **💰 Salary Comparison by Job Title**
A horizontal bar chart visualizes the median salary across various data roles, sorted in descending order for immediate readability.
**Key Insight:** Senior-level and engineering roles command significantly higher salary ranges compared to entry-level analyst positions.
![Median_Salary_by_Job_Title](https://github.com/user-attachments/assets/52bd6892-1bfd-410b-b197-28bf64da470e)


### **🌍 Global Salary Distribution**
An interactive map chart displays median salaries by country to highlight regional disparities.
**Key Insight:** Significant variations exist globally, with regions like the USA and UK offering substantially higher compensation for data professionals.
![Median_Salary_by_Country](https://github.com/user-attachments/assets/a67ad8ce-21e4-4fc9-9946-72e9f9fafda5)


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
```

![Median_Salary_of_Job_Titles_Calculated](https://github.com/user-attachments/assets/efacf19e-4e96-4aae-a192-a40c697872e3)

**📊 Dashboard Implemented**

![Dashboard_Implemented_of_Calculated_Median_Salary](https://github.com/user-attachments/assets/af21b946-1c66-406d-8878-22f3fd6ca303)

### **2. Count of Job Schedule Type**
This Excel formula below employs the FILTER() function to exclude entries containing "and" or "," and omit zero values.
```excel
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

---

## 🧮 Conclusion
This Data Jobs Salary Dashboard demonstrates the power of Excel as a comprehensive business intelligence tool for converting raw, unstructured market data into a high-level strategic resource. By integrating advanced array formulas and dynamic filtering, this project successfully bridges the gap between complex data processing and an intuitive user experience. It showcases my technical mastery of multi-criteria logic, ensuring that median salary calculations remain accurate across diverse global parameters while providing immediate, evidence-based value for career planning and market analysis. Ultimately, this project serves as a testament to my ability to manage the full data lifecycle—from initial cleaning and transformation to the final presentation of impactful insights. I created this dashboard to showcase insights into salary trends across various data related job titles.

---

## 📂 Dataset Details
**Source:** 2023 Global Data Jobs dataset.
**Key Attributes:** Job Title, Salary (Yearly/Hourly Avg), Job Location, Schedule Type, and Required Skills.

---

## 👤 Author
- **Nisha Autade** Aspiring Data Analyst
- **Skills:** Python • SQL • Excel • PowerBI • Tableau • Data Visualization
