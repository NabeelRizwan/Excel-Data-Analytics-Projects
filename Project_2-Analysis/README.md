# SQL Data Exploration Project

![2_Project_Analysis.png](/Images/2_Project_Analysis.gif)

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

### 📑 Common Table Expressions (CTEs)

#### 🧮 Structured Query Analysis

<img src="/Images/2_Project_Analysis_CTE.png" width="850" height="500" alt="CTE Analysis">

```sql
WITH salary_data AS (
    SELECT
        job_title_short,
        AVG(salary_year_avg) AS avg_salary
    FROM job_postings_fact
    GROUP BY job_title_short
)

SELECT *
FROM salary_data
ORDER BY avg_salary DESC;
```

- 🔍 **Improved Readability:** Used CTEs to simplify complex analytical queries.
- ⚡ **Better Organization:** Broke larger SQL workflows into manageable sections.
- 📈 **Scalability:** Improved maintainability for future SQL analysis tasks.
- 💡 **Insights Gained:** Helped structure advanced analytical logic more efficiently.

### 📈 Window Functions

#### 🏆 Salary Ranking Analysis

<img src="/Images/2_Project_Analysis_Window_Function.png" width="850" height="500" alt="Window Function Analysis">

```sql
SELECT
    job_title_short,
    salary_year_avg,
    RANK() OVER(ORDER BY salary_year_avg DESC) AS salary_rank
FROM job_postings_fact;
```

- 🛠️ **SQL Features:** Utilized the `RANK()` window function for salary ranking.
- 🎨 **Design Choice:** Maintained row-level information while ranking salaries dynamically.
- 📊 **Data Representation:** Compared salaries across different job roles efficiently.
- 💡 **Insights Gained:** Helped identify the highest-paying opportunities within the dataset.

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
