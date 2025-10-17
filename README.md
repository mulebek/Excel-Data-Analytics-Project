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

  Dashboard Implementation

  <img width="1148" height="1214" alt="Job Title" src="https://github.com/user-attachments/assets/99f5ef48-ecb8-4b93-a2ed-a2dfad8573aa" />

  **Count of Job Schedule Type**

=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))


  - 🔍 Unique List Generation: This Excel formula below employs the FILTER() function to exclude entries containing "and" or commas, and omit zero values.
  - 🔢 Formula Purpose: This formula populates the table below, which gives us a list of unique job schedule types.

📉 Dashboard Implementation:  

<img width="942" height="1212" alt="Type_2" src="https://github.com/user-attachments/assets/c41fd8c2-fe78-4ca2-a425-092069a6135f" />

   ## Data Validation 
   
   🔍 Filtered List

- 🔒 Enhanced Data Validation: Implementing the filtered list as a data validation rule under the Job Title, Country, and Type option in the Data tab ensures:

     🎯 User input is restricted to predefined, validated schedule types

     🚫 Incorrect or inconsistent entries are prevented
  
     👥 Overall usability of the dashboard is enhanced


![Data Validation](https://github.com/user-attachments/assets/acd70963-8578-4118-ae0f-97213885c6bb)

## Conclusion  

I created this dashboard to showcase insights into salary trends across various data-related job titles. This dashboard allow users to make informed decision about their career paths. Exploring the functionality to how understand how location and job type influence salaries.


# Project 2 Analysis
# Introduction  

I have always been surprised by the lack of data exploring the most optimal jobs and skills in the data science market. I set out to understand what skills top employers request and how to land more pay.  

To understand the data science job market, I asked the following:

   Do more skills get you better pay?
   What’s the salary for data jobs in different regions?
   What are the top skills of data professionals?
   What’s the pay for the top 10 skills?

Excel Skills Used

The following Excel skills were utilized for analysis:

   📊 Pivot Tables  
   📈 Pivot Charts  
   🧮 DAX (Data Analysis Expressions)  
   🔍 Power Query  
   💪 Power Pivot  

   1️⃣ Do more skills get you better pay?  
🔍 Skill: Power Query (ETL)  
📥 Extract  

I first used Power Query to extract the original data (data_salary_all.xlsx) and create two queries:  
        🗃️ First one with all the data jobs information.  
        🔧 The second listing the skills for each job ID.  

📊 Analysis  
💡 Insights

📈 There is a positive correlation between the number of skills requested in job postings and the median salary, particularly in roles like Senior Data Engineer and Data Scientist.  

💼 Roles that require fewer skills, like Business Analyst, tend to offer lower salaries, suggesting that more specialized skill sets command higher market value.

![Checkout my work here](https://github.com/mulebek/Excel-Data-Analytics-Project/blob/main/Project_2.xlsx)
<img width="804" height="445" alt="Salary Analysis (2)" src="https://github.com/user-attachments/assets/60328a75-29f2-4a38-a316-4173e062b0f0" />  

This trend emphasizes the value of acquiring multiple relevant skills, particularly for individuals aiming for higher-paying roles.  

2️⃣ What’s the salary for data jobs in different regions?  
🧮 Skills: PivotTables & DAX  
📈Pivot Table  
🔢 I created a PivotTable using the Data Model I created with Power Pivot.  
📊 I moved the job_title_short to the rows area and salary_year_avg into the values area.  
🧮 Then I added new measure to calculate the median salary for United States jobs.  

=CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "United States")  

🧮 DAX  

To calculate the median year salary I used DAX.  

Median Salary := MEDIAN(data_jobs_all[salary_year_avg])  

📊 Analysis  
💡 Insights

💼 Job roles like Senior Data Engineer and Data Scientist command higher median salaries both in the US and internationally, showcasing the global demand for high-level data expertise.

💰 The salary disparity between US and Non-US roles is particularly notable in high-tech jobs, which might be influenced by the concentration of tech industries in the US.  

<img width="1776" height="738" alt="Country" src="https://github.com/user-attachments/assets/6481ae2c-33cd-4191-ba10-e5b2017b9ff5" />  

🤔 So What

   These salary insights are important for planning and salary negotiations, helping professionals and companies align their offers with market standards while considering geographical variations.  

 3️⃣ What are the top skills of data professionals?  
🔧 Skill: Power Pivot  
💪 Power Pivot

   🔗 I created a data model by integrating the data_jobs_all and data_jobs_skills tables into one model.
   🧹 Since I had already cleaned the data using Power Query; Power Pivot created a relationship between these two tables.  

 📊Analysis  
💡Insights

💻 SQL and Python dominate as top skills in data-related jobs, reflecting their foundational role in data processing and analysis.  

☁️ Emerging technologies like AWS and Azure also show significant presence, underlining the industry's shift towards cloud services and big data technologies.  

<img width="942" height="1212" alt="Top" src="https://github.com/user-attachments/assets/f82b0be2-f05c-4e23-834a-10bafdad5698" />  

🤔So What

   Understanding prevalent skills in the industry not only helps professionals stay competitive but also guides training and educational programs to focus on the most impactful technologies.  

 4️⃣ What’s the pay of the top 10 skills?  
📊 Skill: Advanced Charts (Pivot Chart)  
📈 PivotChart

   I created a combo PivotChart to plot median salary and skill likelihood (%) from my PivotTable.  
       🪙 Primary Axis: Median Salary (as a Clustered Column)  
       👍 Secondary Axis: Skill Likelihood (as a Line with Markers)  
    To customize the chart, I added a title axis title, removed the lines (skill likelihood), and changed the markers to diamonds.  

📊 Analysis  
💡Insights

💰 Higher median salaries are associated with skills like Python, Oracle, and SQL, suggesting their critical role in high-paying tech jobs.

📉 Skills like PowerPoint and Word have the lowest median salaries and likelihood, indicating less specialization and demand in high-salary sectors.  

<img width="862" height="452" alt="Skills" src="https://github.com/user-attachments/assets/759d6845-672a-4f6a-a95f-18e9abec4a11" />  

🤔So What  

  This chart highlights the importance of investing time in learning high-value skills like Python and SQL, which are evidently tied to higher paying roles, especially for those looking to maximize their salary in the tech industry.

Conclusion

As a data enthusiast and former job seeker, I embarked on this Excel-based project to uncover valuable insights about the data science job market. Using a dataset I've curated from real-world job postings, I analyzed job titles, salaries, locations, and essential skills. By leveraging Excel features like Power Query, PivotTables, DAX, and charts, I discovered key correlations between multiple skills and higher salaries, particularly in Python, SQL, and cloud technologies.

I hope this project serves as a practical guide for data professionals and provides an overview of the skills needed for higher-paying roles.

