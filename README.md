# Introduction
📊 Step into the world of data analytics! This project dives deep into data analyst roles, uncovering 💰 the highest-paying positions, 🔥 the most sought-after skills, and ✅ where lucrative salaries align with in-demand expertise.

🔍 Want to explore the SQL queries used? Find them here: [project_sql folder](/project_sql/).


# Background
As the demand for data professionals grows, companies are offering competitive salaries for skilled data analysts. This project analyzes real-world job posting data to uncover valuable insights into the current job market. By writing SQL queries on a structured dataset, I explored:

📍 The most in-demand skills for data analyst roles

💵 The top-paying data analyst jobs

🔁 How remote roles compare in terms of salary

📈 Where high salary and skill demand intersect

The goal was to help aspiring analysts and job seekers understand what skills to focus on and where the best opportunities lie.

### The questions I wanted to answer through my SQL queries   were:
   1. What are the top-paying data analyst jobs?

   2. What skills are required for these top-paying jobs?

   3. What skills are most in demand for data analysts?

   4. Which skills are associated with higher salaries?

   5. What are the most optimal skills to learn?
# Tools I Used
For my deep dive into the data analyst job market, I harnessed the power of several key tools:

- **SQL:** The backbone of my analysis, allowing me to query the database and unearth critical insights.  
- **PostgreSQL:** The chosen database management system, ideal for handling the job posting data.  
- **Visual Studio Code:** My go-to for database management and executing SQL queries.  
- **Git & GitHub:** Essential for version control and sharing my SQL scripts and analysis, ensuring collaboration and project tracking.

# The Analysis
Each query in this project targeted a specific aspect of the data analyst job market. Here's how I approached the first question:

### **Top Paying Data Analyst Jobs**
To identify the highest-paying roles, I filtered job postings by average yearly salary and location. This query helped highlight where the most lucrative opportunities are for data analysts.

```sql
SELECT 
    job_id,
    job_title,
    job_location,
    job_schedule_type,
    salary_year_avg,
    job_posted_date,
    name AS company_name
FROM
    job_postings_fact
LEFT JOIN company_dim ON job_postings_fact.company_id = company_dim.company_id
WHERE
    job_title_short = 'Data Analyst' AND
    job_location = 'Anywhere' AND
    salary_year_avg IS NOT NULL
ORDER BY salary_year_avg DESC
LIMIT 10
```
## 📊 Key Insights

Here’s the breakdown of the top data analyst jobs in 2023:

- **💸 Wide Salary Range:** Top 10 paying data analyst roles span from **$184,000 to $650,000**, indicating significant earning potential in the field.

- **🏢 Diverse Employers:** Companies like **SmartAsset, Meta, and AT&T** are offering high salaries, highlighting broad industry demand.

- **📌 Job Title Variety:** There's a wide range of titles — from *Data Analyst* to *Director of Analytics* — reflecting different specializations and career paths.

*simliary done for other queries*


# What I Learned


Throughout this adventure, I've turbocharged my SQL toolkit with some serious firepower:

- **🧩 Complex Query Crafting:** *Mastered the art of advanced SQL, merging tables like a pro and wielding `WITH` clauses for ninja-level temp table maneuvers.*

- **📊 Data Aggregation:** *Got cozy with `GROUP BY` and turned aggregate functions like `COUNT()` and `AVG()` into my data-summarizing sidekicks.*

- **💡 Analytical Wizardry:** *Leveled up my real-world puzzle-solving skills, turning questions into actionable, insightful SQL queries.*

# Conclusions
### 📊 Insights

From the analysis, several general insights emerged:

1. _**Top-Paying Data Analyst Jobs**_: The highest-paying jobs for data analysts that allow remote work offer a wide range of salaries, the highest at **$650,000**!

2. _**Skills for Top-Paying Jobs**_: High-paying data analyst jobs require advanced proficiency in SQL, suggesting it’s a critical skill for earning a top salary.

3. _**Most In-Demand Skills**_: SQL is also the most demanded skill in the data analyst job market, thus making it essential for job seekers.

4. _**Skills with Higher Salaries**_: Specialized skills, such as SVN and Solidity, are associated with the highest average salaries, indicating a premium on niche expertise.

5. _**Optimal Skills for Job Market Value**_: SQL leads in demand and offers a high average salary, positioning it as one of the most optimal skills for data analysts to learn to maximize their value.

### 🧠 Closing Thoughts

This project enhanced my _SQL skills_ and provided valuable insights into the _data analyst job market_.  
The findings from the analysis serve as a guide to prioritizing skill development and job search efforts.  

Aspiring data analysts can better position themselves in a competitive job market by focusing on _high-demand_, _high-salary skills_.  
This exploration highlights the importance of _continuous learning_ and _adaptation_ to emerging trends in the field of _data analytics_.