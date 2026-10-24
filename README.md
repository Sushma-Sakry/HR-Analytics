HR Analytics: Employee Attrition and Retention Analysis
InternNova Internship --- Week 6 Final Data Analytics Project

1. Project Overview
This project analyzes employee attrition patterns using Python and Power BI. It covers data preparation, exploratory data analysis (EDA),
visualization, and an interactive dashboard to help identify employee groups that may need further retention-focused investigation.

The analysis describes patterns and associations in the available dataset. It does not establish that any individual factor causes employees to leave.

2. Problem Statement
Employee attrition can affect organizational stability, recruitment costs, and productivity. HR teams need a clear view of how attrition varies across employee groups and workplace characteristics. This project examines attrition by department, overtime status, age group, and job role, then presents the findings through charts and a Power BI dashboard.

3. Project Objectives
- Inspect, clean, and validate the HR dataset.
- Summarize employee characteristics and attrition.
- Compare attrition across departments, overtime status, age groups, and job roles.
- Examine correlations between numerical variables and attrition.
- Identify potential monthly-income outliers using the interquartile range (IQR) method.
- Create five visualizations and an interactive Power BI dashboard.
- Communicate findings and propose data-informed retention recommendations.
- Use Git and GitHub for version control and project documentation.

4. Dataset
- Original file: HR_Analytics.csv
- Cleaned file: HR_Analytics_Cleaned.csv
- Original dimensions: 1,480 rows × 38 columns
- Cleaned dimensions: 1,473 rows × 35 columns
The dataset contains employee-level information such as demographics, department, job role, income, satisfaction, overtime, work experience and attrition status.

5. Tools and Technologies
- Python --- data preparation and analysis
- Pandas --- data manipulation and cleaning
- NumPy --- numerical operations
- Matplotlib and Seaborn --- visualizations
- Google Colab --- notebook environment
- Power BI Desktop --- interactive dashboard
- Git and GitHub --- version control and project hosting

6. Data Cleaning and Preparation
The following steps were performed:
1. Inspected the dataset dimensions, columns, data types, and missing values.
2. Removed 7 exact duplicate rows.
3. Filled 57 missing values in YearsWithCurrManager with the median calculated after removing duplicates.
4. Standardized the BusinessTravel category TravelRarely to Travel_Rarely.
5. Removed three constant columns: EmployeeCount, Over18, and StandardHours.
6. Validated the cleaned data to confirm that no missing values or exact duplicate rows remained.
The original dataset was retained separately from the cleaned dataset.
7. Exploratory Data Analysis (EDA)
The analysis included:
- Descriptive statistics for numerical columns.
- Employee attrition counts and percentages.
- Attrition comparisons by department and overtime status.
- Attrition comparisons by age group and job role.
- Correlation analysis between numerical variables and an attrition
  indicator.
- Potential monthly-income outlier detection using the IQR method.
The IQR rule identified 114 potential monthly-income outliers. These records were not automatically removed because a statistical outlier is not necessarily an incorrect value.

8. Visualizations
Five charts were created during the analysis:
1. Employee Attrition Count
2. Attrition Rate by Department
3. Attrition Rate by Overtime
4. Attrition Rate by Age Group
5. Attrition Rate by Job Role

9. Power BI Dashboard
The Power BI report contains two pages.
Page 1: HR Overview
- Total Employees KPI
- Employees Who Left KPI
- Attrition Rate KPI
- Employee Attrition by Department
- Employee Attrition by Overtime
- Department, Age Group, and Overtime slicers

Page 2: Attrition Analysis
- Employee Attrition by Job Role
- Employee Attrition by Age Group
The dashboard is intended to let viewers compare employee attrition patterns through visualizations and interactive filters.

10. Key Findings
Overall attrition
- Total employees in the cleaned dataset: 1,473
- Employees who left: 237
- Employees who stayed: 1,236
- Overall attrition rate: 16.09%

Overtime
Employees who worked overtime had an attrition rate of 30.53%, compared with 10.41% among employees who did not work overtime.

Department
- Sales: 20.58%
- Human Resources: 19.05%
- Research & Development: 13.81%
Sales had the highest department-level attrition rate among the three departments.

Age group
Employees aged 18--25 had an attrition rate of approximately 35.77% (44 departures among 123 employees), the highest among the age groups
analyzed.

Job role
Sales Representatives had the highest job-role attrition rate at 39.29% (33 departures among 84 employees). Laboratory Technicians had a rate of 23.85%, while Research Directors had a rate of 2.50%.

Correlation
The strongest negative correlations with the attrition indicator included:
- TotalWorkingYears: −0.171
- JobLevel: −0.169
- YearsInCurrentRole: −0.160
- MonthlyIncome: −0.159
- Age: −0.159
These are weak associations and do not establish causation.

11. Recommendations

1. Review overtime and workload
Investigate overtime patterns, staffing levels, workload distribution, and employee feedback. Consider piloting workload adjustments and
monitoring attrition rates over time to evaluate whether outcomes
change.

2. Improve targeted retention efforts
Investigate departure reasons among Sales Representatives and younger employees. Consider structured onboarding, mentoring, career development, regular manager check-ins, and employee feedback sessions.
Evaluate the impact of these initiatives using future attrition trends.

12. Limitations
- The analysis identifies patterns and associations but does not establish causal relationships.
- Findings reflect the available dataset and may not represent every organization.
- Potential outliers require business context before deciding whether to remove them.
- Recommendations should be tested and evaluated with additional evidence and future attrition data.
- The dataset source and redistribution licence must be verified and documented before public distribution.

13. Conclusion
This project demonstrates how Python and Power BI can be used to clean, analyze, visualize, and interpret HR data. The analysis identified differences in attrition across overtime status, departments, age groups, and job roles. These findings provide a starting point for further investigation and targeted employee-retention initiatives.

## 14. Project Structure

```text
HR-Analytics/
├── .gitignore
├── README.md
├── Insights_and_Recommendations.md
├── HR Analytics dashboard.pbix
├── Presentation HR Analytics.pptx
├── code/
│   ├── Week_6_Assignment.ipynb
│   └── week_6_assignment.py
├── charts/
│   ├── attrition by age group.png
│   ├── attrition by emp dept.png
│   ├── attrition rate by job role.png
│   ├── attrition rate by overtime.png
│   └── emp attrition count.png
└── data/
    ├── HR_Analytics.csv
    └── HR_Analytics_Cleaned.csv
```
