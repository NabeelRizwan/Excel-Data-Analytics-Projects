# SQL Data Exploration Project

![2_Project_Analysis.png](/Images/2_Project_Analysis_Chart2.png)

## Introduction

This SQL data exploration project was completed as part of my data analytics learning journey to analyze real-world data job postings and gain insights into salaries, hiring trends, and in-demand technical skills.

The dataset used in this project comes from my SQL learning course, which helped me build a strong foundation in querying, analyzing, and exploring structured data using SQL. The data contains detailed information about job titles, salaries, locations, and technical skills that are explored throughout this project.

### Project Files

My completed SQL analysis files are included in this repository.

### SQL Skills Used

The following SQL skills and concepts were utilized throughout this project:

- **📊 Data Analysis**
- **🧮 Aggregate Functions**
- **🔗 Joins**
- **📑 Common Table Expressions (CTEs)**
- **📈 Window Functions**
- **🗂️ Filtering & Sorting**

### Data Jobs Dataset

The dataset used for this project contains real-world data job information from 2023. The dataset was provided through my SQL course and includes detailed information on:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

## SQL Analysis

### 📊 In-Demand Skills Analysis

#### 🔍 Top Skills by Job Demand

<img src="/Images/2_Project_Analysis_Chart1.png" width="850" height="500" alt="Top Skills Analysis">

```sql
SELECT 
    skills,
    COUNT(*) AS demand_count
FROM skills_job_dim
GROUP BY skills
ORDER BY demand_count DESC;
```

- 🛠️ **SQL Features:** Utilized `GROUP BY`, `COUNT()`, and `ORDER BY` for demand analysis.
- 🎨 **Design Choice:** Organized skills by descending demand for easier comparison.
- 📉 **Data Organization:** Grouped and ranked skills based on total job postings.
- 💡 **Insights Gained:** SQL, Python, and cloud-related technologies consistently ranked among the most requested skills.

### 📊 Analysis

#### 💡 Insights

- 💻 SQL and Python remained among the most dominant technical skills across data-related job postings, highlighting their importance in analytics, automation, and data processing workflows.
- ☁️ Cloud technologies such as AWS and Azure also appeared frequently, reflecting the growing demand for cloud computing and scalable data infrastructure skills in the industry.

![2_Project_Analysis_Chart3.png](/Images/2_Project_Analysis_Chart3.png)

#### 🤔 So What

- Understanding which technical skills are most commonly required helps aspiring data professionals focus on learning tools that are highly valued in the job market.
- These insights also help students and professionals prioritize skill development based on current industry trends and hiring demands.

## 4️⃣ What’s the pay of the top 10 skills?

### 📊 Skill: Advanced Charts (Pivot Chart)

#### 📈 PivotChart

- I created a combo PivotChart to visualize both median salary and skill likelihood (%) from my PivotTable.
    - 🪙 **Primary Axis:** Median Salary displayed as a Clustered Column Chart
    - 👍 **Secondary Axis:** Skill Likelihood displayed as a Line Chart with Markers
- To improve the visualization, I customized the chart by adding chart titles, adjusting axis labels, removing unnecessary gridlines, and changing marker styles for better readability.

### 📊 Analysis

#### 💡 Insights

- 💰 Higher median salaries were strongly associated with technical skills such as Python, Oracle, and SQL, showing their importance in higher-paying technology and analytics roles.
- 📉 Skills such as PowerPoint and Word showed lower salary ranges and lower demand percentages, indicating that general office skills are less connected to specialized high-paying positions.

![2_Project_Analysis_Chart4.png](/Images/2_Project_Analysis_Chart4.png)

### 🤔 So What

- Learning specialized technical skills can significantly improve earning potential in data and technology careers.
- This analysis highlights the value of investing time in high-demand technologies that align with industry needs and higher-paying job opportunities.

### 💰 Salary Analysis

#### 📉 Average Salary by Job Role

<img src="/Images/2_Project_Analysis_Chart2.png" width="850" height="500" alt="Salary Analysis">

```sql
SELECT
    job_title_short,
    AVG(salary_year_avg) AS avg_salary
FROM job_postings_fact
GROUP BY job_title_short
ORDER BY avg_salary DESC;
```

- 🛠️ **SQL Features:** Applied aggregate salary calculations using `AVG()`.
- 🎨 **Design Choice:** Grouped salaries by job titles for better role comparison.
- 📊 **Data Representation:** Compared compensation trends across multiple data-related careers.
- 💡 **Insights Gained:** Senior and engineering-focused positions generally offered higher salary ranges.


## Key Insights

### 📌 Findings from the Analysis

- SQL and Python were among the most in-demand technical skills.
- Remote and hybrid roles showed competitive salary ranges.
- Senior-level positions generally offered significantly higher compensation.
- Cloud and engineering-related skills were associated with higher-paying jobs.
- Salary trends varied across different job categories and geographic regions.

## Conclusion

I completed this SQL analysis project to strengthen my practical SQL and data analytics skills using real-world datasets. Through this project, I gained hands-on experience working with SQL queries, aggregations, filtering, joins, CTEs, and window functions.

This project also improved my ability to analyze industry trends, uncover salary insights, and extract meaningful information from structured datasets while building confidence in real-world data analysis workflows.
