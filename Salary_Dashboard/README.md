#  Salary Dashboard
![1_Salary_Dashboard_Final_Dashboard (2)](https://github.com/user-attachments/assets/cd7babf9-28f7-4d21-9ecf-de9c4a76c7d5)

##  Introduction
This **Data Jobs Salary Dashboard** helps job seekers investigate salaries for their desired roles and ensure they are being adequately compensated.  

The dataset includes real-world, detailed information on job titles, salaries, locations, and essential skills — all presented visually and interactively in the dashboard. It provides a strong foundation for analysis using Excel 

The project also reflects my Excel skills in action. 

🛠️Skills Demonstrated

- 🧮Advanced Excel formulas and functions  
- 📊Pivot tables and data validation  
- 🎨Conditional formatting and dynamic charts  
- 🧹Data cleaning, sorting, filtering, and structuring  
- 🧱Dashboard design for clarity and usability
---


##  Dashboard File
My final dashboard is in [Salary_Dashboard](Salary_Dashboard.xlsx)



---

##   Dashboard Build Details

###  📊Data Science Job Salaries - Bar Chart
![image](https://github.com/user-attachments/assets/a2236da2-c650-42ea-9ab4-ef1f2c6f8b62)


**I created a horizontal bar chart to visually compare median salaries across different job titles using the formula:** 

**The chart clearly shows that Senior roles and Engineers typically earn higher salaries, with the Senior Data Scientist and Machine Learning Engineer leading the pack. In contrast, the Data Analyst role has the lowest median salary, making it easy to identify salary trends at a glance.**

**Formula used**
```
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
**Calculation Table**

![image](https://github.com/user-attachments/assets/3e4c9abe-103b-41d6-b30b-9611ee6d8780)

---
##  🗺️Country Median Salaries - Map Chart
![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/963f9800-27c3-4e5b-ac70-583a69866e97)

**I used Excel's map chart feature to plot global median salaries, creating a color-coded map that highlights salary levels by region. This visualization reveals global salary disparities and helps those considering remote work identify countries that pay more for data jobs.**

---

##  #️⃣Count of Job Schedule Type
![image](https://github.com/user-attachments/assets/301ade2b-b4fc-4ba4-8735-be034f475258)

**I used the following Excel formula to generate a refined list of job schedule types by excluding unwanted entries:**

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```
**This formula removes entries that contain the word "and", commas, or zeros. It returns a clean list of valid, individual job schedule types, which I used to support accurate analysis and improve data validation in the dashboard.**

---

### ✅  Data Validation with Filtered List
![image](https://github.com/user-attachments/assets/af22dfe2-79f1-4796-867f-4e889845a183)


**To enhance data accuracy and user experience, I applied a filtered list as a data validation rule to the Job Title, Country, and Type fields in the Data tab. This setup:**

**Ensures user input is restricted to validated, predefined options**

**Prevents incorrect or inconsistent entries**

**Improves the overall functionality and reliability of the dashboard.**

---

## 📝Conclusion
This dashboard was developed to present insights into salary trends across a range of data-related job titles.The dashboard highlights how factors like location and job type impact salary levels, helping users make informed career decisions.

Feel free to navigate through the dashboard file to explore all the details, features, and Excel skills applied throughout the project. <3
