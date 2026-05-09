# Excel Salary Dashboard

![1_Salary_Dashboard.png](/Images/1_Salary_Dashboard_Final_Dashboard.gif)

## Introduction

This Excel salary dashboard project was developed to analyze salary trends across data-related careers and provide interactive insights into compensation patterns, locations, and job roles.

The project was completed as part of an Excel Data Analytics course, where I applied Excel-based analytical and dashboarding techniques to work with real-world job market data.

The dataset includes detailed information related to salaries, job titles, countries, and required technical skills.

### Dashboard File
My completed dashboard project can be found here: [1_Salary_Dashboard.xlsx](1_Salary_Dashboard.xlsx).

### Excel Skills Used

The following Excel skills were applied throughout this project:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**

### Data Jobs Dataset

The dataset used for this dashboard contains real-world data analytics and data science job information from 2023. The dataset was provided through the Excel course and includes detailed insights into:

- **👨‍💼 Job Titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Technical Skills**

## Dashboard Build

### 📉 Charts

#### 📊 Data Job Salaries - Bar Chart

<img src="/Images/1_Salary_Dashboard_Chart1.png" width="850" height="550" alt="Salary Dashboard Chart1">

- 🛠️ **Excel Features:** Used Excel bar charts with customized formatting and salary labels for improved readability.
- 🎨 **Design Choice:** Implemented a horizontal bar chart to clearly compare salary ranges across job roles.
- 📉 **Data Organization:** Sorted salary values in descending order to highlight higher-paying positions.
- 💡 **Insights Gained:** The chart helps identify salary differences between analyst, engineer, and senior-level roles.

#### 🗺️ Country Median Salaries - Map Chart

![1_Salary_Dashboard_Chart2.png](/Images/1_Salary_Dashboard_Country_Map.gif)

- 🛠️ **Excel Features:** Utilized Excel's geographic map chart functionality to visualize salary trends globally.
- 🎨 **Design Choice:** Applied color-based mapping to distinguish salary levels across countries.
- 📊 **Data Representation:** Displayed median salary values for countries available within the dataset.
- 👁️ **Visual Enhancement:** Improved geographic salary comparison through visual mapping techniques.
- 💡 **Insights Gained:** Enabled quick analysis of salary distribution across different regions worldwide.

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

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

- 🔍 **Multi-Criteria Filtering:** Evaluates job title, country, schedule type, and excludes missing salary values.
- 📊 **Array Formula Usage:** Combines `MEDIAN()` with nested `IF()` conditions for dynamic calculations.
- 🎯 **Targeted Analysis:** Generates salary insights specific to selected job roles, countries, and work schedules.
- 🔢 **Formula Purpose:** This formula populates the salary analysis table displayed below.

🍽️ Background Table

![1_Salary_Dashboard_Screenshot1.png](/Images/1_Salary_Dashboard_Screenshot1.png)

📉 Dashboard Implementation

<img src="/Images/1_Salary_Dashboard_Job_Title.png" width="400" height="500" alt="Salary Dashboard Title">

#### ⏰ Count of Job Schedule Type

```excel
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 **Filtered List Creation:** The formula filters out unwanted values containing commas, "and", or blank entries.
- 🔢 **Formula Purpose:** Generates a clean and unique list of available job schedule types for dashboard interaction.

🍽️ Background Table

![1_Salary_Dashboard_Type.png](/Images/1_Salary_Dashboard_Screenshot2.png)

📉 Dashboard Implementation:

<img src="/Images/1_Salary_Dashboard_Type.png" width="350" height="500" alt="Salary Dashboard Type">

### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Applied filtered lists as data validation rules for the `Job Title`, `Country`, and `Type` fields to improve dashboard usability.
    - 🎯 Restricts user input to predefined values
    - 🚫 Prevents invalid or inconsistent entries
    - 👥 Improves dashboard interaction and user experience

<img src="/Images/1_Salary_Dashboard_Data_Validation.gif" width="425" height="400" alt="Salary Dashboard Data Validation">

## Conclusion

This dashboard project helped strengthen my Excel analytics and reporting skills through hands-on experience with charts, formulas, dashboards, and interactive filtering techniques.

By working with real-world salary datasets, I gained practical experience in creating business-focused Excel dashboards that provide meaningful insights into salary trends, locations, and job roles within the data analytics industry.
