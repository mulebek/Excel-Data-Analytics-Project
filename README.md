# Excel Data Analytics Project  
## Salary Dashboard  
This data jobs salary dashboard was created to help job seekers investigate saalries for desired jobs and ensure they are being adequately compensated.  
![Checkout my work here](https://github.com/mulebek/Excel-Data-Analytics-Project/blob/main/Project_1.xlsx)  
<img width="1876" height="804" alt="Project 1-Dashboard" src="https://github.com/user-attachments/assets/d6118a0a-99de-4a46-92da-9e93088e7fb7" />  
# Introduction  
An interactive Excel dashboard analyzing data science and analytics salaries across different roles, experience levels, and job types. This project provides insights into compensation trends in the data industry.  
## Excel Skills Used  
The following excel skills were utilized for analysis:  

 - 📉 Charts
 - 🧮 Formulas and Functions
 - ❎ Data Validation
  
# Data Jobs Dataset  
The dataset used for this project contains real-world data science job information from 2023, which provide a foundation for analyzing data using excel. It includes detailed information on:  

  - 👨‍💼 Job titles
  - 💰 Salaries
  - 📍 Locations
  - 🛠️ Skills
  
## Dashboard Build  
📉 Charts
📊 Data Science Job Salaries - Bar Chart  
<img width="1336" height="867" alt="Bar Chart" src="https://github.com/user-attachments/assets/348058ff-4b96-481e-b864-89c013936f16" />

  - 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
  - 🎨 Design Choice: Horizontal bar chart for visual comparison of median salaries.
  - 📉 Data Organization: Sorted job titles by descending salary for improved readability.
  - 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

  
  🗺️ Country Median Salaries - Map Chart
  
  <img width="564" height="395" alt="Map Chart" src="https://github.com/user-attachments/assets/df942f50-707e-4d68-a317-474c16aafa8c" />

  - 🛠️ Excel Features: Utilized Excel's map chart feature to plot median salaries globally.
  - 🎨 Design Choice: Color-coded map to visually differentiate salary levels across regions.
  - 📊 Data Representation: Plotted median salary for each country with available data.
  - 👁️ Visual Enhancement: Improved readability and immediate understanding of geographic salary trends.
  - 💡 Insights Gained: Enables quick grasp of global salary disparities and highlights high/low salary regions.


🧮 Formulas and Functions
💰 Median Salary by Job Titles

    =MEDIAN(
  IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
  )
 )


  - 🔍 Multi-Criteria Filtering: Checks job title, country, schedule type, and excludes blank salaries.
  - 📊 Array Formula: Utilizes MEDIAN() function with nested IF() statement to analyze an array.
  - 🎯 Tailored Insights: Provides specific salary information for job titles, regions, and schedule types.
  - 🔢 Formula Purpose: This formula populates the table below, returning the median salary based on job title, country, and type specified.


  Background Table

  <img width="265" height="220" alt="Background" src="https://github.com/user-attachments/assets/f76f6fc7-f6f0-48cc-989e-679eae05a43f" />

  Dashboard Implementation

  <img width="1148" height="1214" alt="Job Title" src="https://github.com/user-attachments/assets/99f5ef48-ecb8-4b93-a2ed-a2dfad8573aa" />

  **Count of Job Schedule Type**

=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))


  - 🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
  - 🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table

<img width="195" height="119" alt="Type" src="https://github.com/user-attachments/assets/da074947-2df1-4608-bac0-48da448ff8b1" />

📉 Dashboard Implementation:  

<img width="942" height="1212" alt="Type_2" src="https://github.com/user-attachments/assets/c41fd8c2-fe78-4ca2-a425-092069a6135f" />

   ## Data Validation  
   
   🔍 Filtered List

🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:
      🎯 User input is restricted to predefined, validated schedule types
      🚫 Incorrect or inconsistent entries are prevented
      👥 Overall usability of the dashboard is enhanced

  
![Data Validation](https://github.com/user-attachments/assets/acd70963-8578-4118-ae0f-97213885c6bb)

## Conclusion  

I created this dashboard to showcase insights into salary trends across various data-related job titles. This dashboard allow users to make informed decision about their career paths. Exploring the functionality to how understand how location and job type influence salaries.


## Salary Analysis  
I have always been surprised by the lack of data exploring the most optimal jobs and skills in the data science market. I set out to understand what skills top employers request and how to land more pay.  
![Checkout my work here](https://github.com/mulebek/Excel-Data-Analytics-Project/blob/main/Project_2.xlsx)
<img width="804" height="445" alt="Salary Analysis (2)" src="https://github.com/user-attachments/assets/60328a75-29f2-4a38-a316-4173e062b0f0" />  


