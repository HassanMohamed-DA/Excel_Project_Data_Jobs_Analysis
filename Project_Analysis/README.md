# Job Skills Analysis


##  Introduction

This Excel-based analysis explores how technical skills shape compensation in the data science field. It reveals strong correlations between multiple skills and higher salaries—particularly among professionals skilled in **Python**, **SQL**, and **cloud technologies** like **AWS** and **TensorFlow**. Using advanced Excel tools, the project breaks down salary trends across job titles and highlights which skills truly make a difference.

The dataset includes real-world, detailed information on job titles, salaries, locations, and essential skills.

The project also reflects my Excel skills in action.

---

###  Questions to Analyze

**To guide the analysis, I focused on the following key questions:**

- Do more skills get you better pay?  
- What’s the salary for data jobs in different regions?  
- What are the top skills of data professionals?  
- What’s the pay for the top 10 skills?

  ```
  
### 🛠️ Skills demonstrated

- 📊 **Pivot Tables** – for dynamic data summarization  
- 📈 **Pivot Charts** – to visualize salary trends and patterns  
- 🔍 **Power Query** – for efficient data cleaning and transformation  
- 🧠 **Power Pivot** – to build and manage complex data models  
- 🧮 **DAX (Data Analysis Expressions)** – for creating calculated fields and measures
 ---


##  Project Analysis File
My final Analysis is in [Project_Analysis](Project_Analysis.xlsx)



---
  
## 1️⃣ Do More Skills Lead to Higher Pay?

## Skill Highlight: Power Query (ETL Process)

- ## Extract

Using **Power Query**, I imported the dataset and created two queries:

- One with complete details for each data-related job posting
- Another that connects each job ID to the skills listed for that role

---
- ##  Transform

- Then, I transformed each query by changing column types, removing unnecessary columns, cleaning text to eliminate specific words, and trimming excess whitespace.
    - 📊 data_jobs_all

    ![image](https://github.com/user-attachments/assets/3e632b64-c30e-4101-8687-f96d0d1990f8)

    - 🛠️ data_job_skills

    ![image](https://github.com/user-attachments/assets/0e44f179-2d81-431c-824e-775b0eb114f8)

---
- ##  Load

- I then loaded both cleaned queries into the workbook, getting everything ready for the analysis.

📊 data_jobs_all

![2_Project_Analysis_Screenshot3](https://github.com/user-attachments/assets/1a427a81-3f79-4566-91db-733a2f09d9f4)

🛠️ data_job_skills

![2_Project_Analysis_Screenshot3](https://github.com/user-attachments/assets/269ccda7-47e3-4e76-ac97-dd2b768d0155)

---

## Analysis

### 💡Insights

Jobs that list more required skills tend to offer higher salaries — especially in roles like Senior Data Engineer and Data Scientist.

On the other hand, positions that ask for fewer skills, such as Business Analyst, usually come with lower pay. This suggests that specialized skill sets are valued more in the job market.

![image](https://github.com/user-attachments/assets/10897ec3-7eb7-4e45-8824-ce7dfb8e9a38)

**These findings suggest that developing a broader set of in-demand skills can significantly boost your chances of landing higher-paying roles in data science.**

---

## 2️⃣ What’s the salary for data jobs in different regions?

## Skill Highlight: PivotTables & DAX

## Pivot Table


- I created a PivotTable using the data model built with Power Pivot.  
- In the layout, `job_title_short` was placed in the Rows area, and `salary_year_avg` in the Values area.  
- I then added a measure to calculate the median salary for jobs :

  ```
  =CALCULATE(
      MEDIAN(data_jobs_all[salary_year_avg]),
      data_jobs_all[job_country] = "United States")

##  DAX

To calculate the median yearly salary across all job listings, I used a DAX measure. The median is a better representation of central tendency than the average, especially in datasets with outliers or skewed salary distributions.
```

Median Salary := MEDIAN(data_jobs_all[salary_year_avg])      
```

## 💡 Insights

Job roles such as Senior Data Scientist and Senior Data Engineer offer the highest median salaries, reflecting the demand for advanced skills. 
Business Analyst and Data Analyst roles pay less, likely due to fewer technical requirements.

The salary gap between U.S. and non-U.S. roles is especially noticeable in high-tech positions, likely influenced by the concentration of tech industries in the United States.

![Animation5](https://github.com/user-attachments/assets/95c77662-82b9-42e8-ba90-44feb8b0f91f)

**These insights are valuable for both career planning and salary negotiations. They help professionals understand their market value and guide employers in offering competitive compensation, while also accounting for regional differences.**

---

## 3️⃣ What are the top skills of data professionals?

## Skill Highlight: Power Pivot

### Power Pivot

To support deeper analysis, I used Power Pivot to create a data model by combining the `data_jobs_all` and `data_jobs_skills` tables. Since the data had already been cleaned using Power Query, Power Pivot was able to automatically establish a relationship between the two tables.

---

### Power Pivot Menu

The Power Pivot menu was used to refine the data model and made it easy to create custom measures for further analysis.

![image](https://github.com/user-attachments/assets/c9054094-d594-4608-a01e-ff703b8426de)

 ---
 
### Data Model Structure

A relationship between the two tables was created using the `job_id` column, which served as a common key. This allowed for cross-table analysis, making it possible to link job titles with their related skill sets and salary data.

![image](https://github.com/user-attachments/assets/d1939ecd-8f1a-4333-b174-d7b531d7d631)

---

## 💡 Insights

SQL and Python consistently appear as the most in-demand skills for data-related roles, highlighting their essential role in data processing and analysis.  
Cloud platforms like AWS and Azure are also becoming increasingly common in job postings, reflecting the industry's growing focus on cloud services and big data technologies.

![image](https://github.com/user-attachments/assets/e965460a-f27f-46c2-a02a-be81719da315)

---

## PivotChart

I created a combination PivotChart to visualize both the median salary and the likelihood of specific skills appearing in job postings.  
- The **primary axis** displays median salary using clustered columns.  
- The **secondary axis** shows skill likelihood (%) as a line with markers.

-The PivotTable shows key skills like Python, SQL, Excel, and Tableau, along with their median salaries and how often they appear in job listings. High-demand skills like Python and SQL are linked to higher salaries, while less common tools like Word and PowerPoint tend to offer lower pay.  

-I also added a slicer to the chart, allowing users to filter the data by country for more targeted insights.


![image](https://github.com/user-attachments/assets/ddb8512e-ed8b-4398-ad40-a139d3b8c120) ![image](https://github.com/user-attachments/assets/ab6633eb-d012-48e5-aab6-3fc8e84a1107)

---
## 💡 Insights
Higher median salaries are linked to skills like Python, Oracle, and SQL, suggesting their crucial role in well-paying tech jobs.  
On the other hand, skills like PowerPoint and Word show the lowest median salaries and appear less frequently, indicating lower specialization and demand in high-salary roles.

**This chart highlights the importance of focusing on high-value skills like Python and SQL, which are clearly connected to higher-paying opportunities—especially for those aiming to increase their earning potential in the tech industry.**

![Animation4](https://github.com/user-attachments/assets/40241eb1-8bff-4bb3-acb5-02fcf52f0acb)

---
## 📌 Conclusion

This project highlights how technical skills directly influence compensation in the data science field. By combining Excel's powerful tools—Power Query, Power Pivot, PivotTables, DAX, and PivotCharts—I was able to explore patterns between job roles, salary levels, and the most in-demand skills across different regions.

The analysis clearly shows that roles requiring advanced skills like Python, SQL, and cloud technologies not only appear more frequently in job listings but also command significantly higher median salaries. In contrast, roles demanding fewer or more general skills tend to offer lower compensation.

For professionals aiming to grow in the data field, this underscores the value of investing in high-demand skills. For employers and recruiters, it provides insight into the evolving expectations and compensation benchmarks of the data workforce.

This project reflects both analytical thinking and technical capability, demonstrating how Excel can be used to gain valuable, actionable insights from real-world job market data.

Feel free to explore the analysis file to see the full details, Excel techniques, and insights applied throughout the project. <3
