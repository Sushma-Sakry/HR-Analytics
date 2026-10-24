# HR Analytics: Employee Attrition and Retention Analysis

## 1. Project Overview

This project analyzes employee attrition using Python, Pandas, Matplotlib, Seaborn, and Power BI. The aim is to understand employee turnover patterns and identify factors associated with employees leaving an organization.

The project includes data cleaning, exploratory data analysis (EDA), data visualization, and an interactive Power BI dashboard to support data-driven HR decisions.

## 2. Problem Statement

Employee attrition can affect organizational stability, recruitment costs, and productivity. This project explores employee data to identify patterns in attrition across departments, overtime status, age groups, and job roles.

The analysis aims to help HR teams identify areas that may require further investigation and develop employee retention strategies.

## 3. Project Objectives

- Clean and prepare the HR dataset for analysis.
- Explore employee characteristics and attrition patterns.
- Analyze attrition by department, overtime, age group, and job role.
- Examine correlations between numerical variables and attrition.
- Identify potential outliers in monthly income.
- Create visualizations and an interactive Power BI dashboard.
- Provide data-driven recommendations to support employee retention.

## 4. Dataset

**Dataset name:** HR Analytics Dataset

**Original file:** `HR_Analytics.csv`

**Cleaned file:** `HR_Analytics_Cleaned.csv`

The original dataset contains 1,480 rows and 38 columns, including employee demographics, department, job role, income, job satisfaction, overtime, work experience, and attrition status.

The cleaned dataset contains 1,473 rows and 35 columns.

**Dataset source:** Add the original dataset's verified source URL and licence here before submitting the project.

## 5. Tools and Technologies

- **Python:** Data analysis and cleaning
- **Pandas:** Data manipulation and preparation
- **NumPy:** Numerical operations
- **Matplotlib:** Data visualization
- **Seaborn:** Statistical visualization
- **Google Colab:** Python notebook environment
- **Power BI Desktop:** Interactive dashboard development
- **Git:** Version control
- **GitHub:** Project hosting and documentation

## 6. Data Cleaning and Preparation

The following cleaning steps were performed:

1. Inspected the dataset's dimensions, columns, data types, and missing values.
2. Identified and removed 7 exact duplicate rows.
3. Handled 57 missing values in `YearsWithCurrManager` by replacing them with the median.
4. Standardized the inconsistent `BusinessTravel` category `TravelRarely` to `Travel_Rarely`.
5. Removed three constant columns: `EmployeeCount`, `Over18`, and `StandardHours`.
6. Verified that the cleaned dataset contained no missing values or exact duplicate rows.

The cleaned dataset was retained separately from the original dataset.

## 7. Exploratory Data Analysis (EDA)

The analysis included:

- Descriptive statistics for numerical columns.
- Employee attrition counts and percentages.
- Attrition analysis by department.
- Attrition analysis by overtime status.
- Attrition analysis by age group.
- Attrition analysis by job role.
- Correlation analysis between numerical variables and attrition.
- Potential outlier detection in monthly income using the interquartile range (IQR) method.

A total of 114 potential monthly income outliers were identified using the IQR rule. These records were not automatically removed because an outlier is not necessarily an incorrect value.

## 8. Data Visualizations

Five charts were created using Python:

1. Employee Attrition Count
2. Attrition Rate by Department
3. Attrition Rate by Overtime
4. Attrition Rate by Age Group
5. Attrition Rate by Job Role

These visualizations help compare attrition patterns across different employee groups.

## 9. Power BI Dashboard

An interactive Power BI dashboard was created with two report pages.

### Page 1: HR Overview

- Total Employees KPI
- Employees Who Left KPI
- Attrition Rate KPI
- Employee Attrition by Department
- Employee Attrition by Overtime
- Department, Age Group, and Overtime slicers

### Page 2: Attrition Analysis

- Employee Attrition by Job Role
- Employee Attrition by Age Group

The dashboard enables users to explore employee attrition patterns through visual comparisons and interactive filters.

## 10. Key Insights

### Overall Attrition

- Total employees: 1,473
- Employees who left: 237
- Employees who stayed: 1,236
- Overall attrition rate: 16.09%

### Overtime

Employees working overtime had an attrition rate of 30.53%, compared with 10.41% among employees not working overtime.

### Department

- Sales: 20.58%
- Human Resources: 19.05%
- Research & Development: 13.81%

Sales had the highest department-level attrition rate.

### Age Group

Employees aged 18–25 had an attrition rate of approximately 35.77%, the highest among the age groups analyzed.

### Job Role

Sales Representatives had the highest job-role attrition rate at 39.29%, followed by Laboratory Technicians at 23.85%.

### Correlation

The strongest negative correlations with attrition included:

- TotalWorkingYears: -0.171
- JobLevel: -0.169
- YearsInCurrentRole: -0.160
- MonthlyIncome: -0.159
- Age: -0.159

These are weak associations and do not establish causation.

## 11. Recommendations

### 1. Review Overtime and Workload

Investigate overtime patterns, staffing levels, workload distribution, and employee feedback. Pilot workload improvements and monitor attrition rates to evaluate their effectiveness.

### 2. Improve Targeted Retention Efforts

Investigate the reasons for departures among Sales Representatives and younger employees. Consider structured onboarding, mentoring, career development, and regular employee feedback sessions.

## 12. Project Limitations

- The analysis identifies associations and patterns but does not establish causal relationships.
- The findings are based on the available dataset and may not represent every organization.
- Potential outliers require business context before any decision to remove them.
- Recommendations should be evaluated using additional data and future attrition trends.

## 13. Conclusion

This project demonstrates how Python and Power BI can be used to clean, analyze, visualize, and interpret HR data. The analysis identified differences in attrition across overtime status, departments, age groups, and job roles.

The findings provide a starting point for further investigation and targeted employee retention initiatives.

## 14. Project Structure

```text
HR-Analytics/
├── data/
│   └── HR_Analytics_Cleaned.csv
├── notebooks/
│   └── HR_Analytics.ipynb
├── charts/
│   ├── attrition_count.png
│   ├── department_attrition.png
│   ├── overtime_attrition.png
│   ├── age_group_attrition.png
│   └── job_role_attrition.png
├── dashboard/
│   └── HR_Analytics_Dashboard.pbix
├── reports/
│   └── Insights_and_Recommendations.md
├── presentation.pptx
└── README.md
```

