# HR Turnover Analysis - Power BI
---
## Project Overview

This project leverages Power BI to conduct an in-depth analysis of HR turnover trends over multiple years. The analysis offers a comprehensive overview of employee numbers, identifying key patterns and conducting detailed comparisons across gender, age groups, and departments. By providing actionable insights into the underlying causes of turnover, this project supports data-driven decision-making aimed at optimizing hiring practices and minimizing employee attrition.

**Tool used:**
- Power BI

**Dataset**
- The project is based on a dataset imported from Kaggle [Human Resources Data Set](https://www.kaggle.com/datasets/rhuebner/human-resources-data-set).
- Data from .xlsm file with 312 rows from year 2011 to 2023
---
## Problem statement

### Problem/Question to be Solved: 

How can the company effectively reduce its employee turnover rate and ensure that critical positions are filled promptly to maintain productivity and morale?

This analysis seeks to identify the root causes of the increasing employee turnover and provide actionable recommendations to mitigate the risk of further staff losses. The goal is to develop a sustainable strategy that improves employee retention and ensures the company's workforce remains adequately staffed to meet operational demands.

---
## Main Steps in Report Creation

### 1. Data Import

- Downloaded `"HRDataset_v14.csv"` from Kaggle ([source](https://www.kaggle.com/datasets/rhuebner/human-resources-data-set)).
- Transformed the data and saved the file locally and renamed it to `"Employees.csv"`.

### 2. Data Cleaning and Transformation

**On the Datasource:**

To align the dataset with the Swiss context, several modifications were made:
- Removed irrelevant columns.
- Updated outdated dates for relevance.
- Added an `"Age"` column to calculate the age of each employee.
- Replaced U.S. states in the `"State"` column with Swiss cantons.

**On Power Query from Power BI:**

- Promoted the first row to "Headers".
- Changed Data types.
- Added two Conditional Columns (`Age Bins`, `Order Bins`).

### 3. Data Modeling

- Created a calendar table using DAX.
- Marked the calendar table as Date table.
- Established two innactive relashionships between the calendar table and the Employees table.

<img src="https://i.imgur.com/gRpIobl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

### 4. DAX Calculations

- Created a measures table to stores all measures.
- Created key measures to calculate the key metrics, such as:
    - *AVG AGE*
    - *AVG Yearly Salary*
    - *Headcounts*
    - *Hires*
    - *Leavers*
    - *Turnover Ratio*

### 5. Report Design

The analysis is based on the following two reports:
- HR Overview
- Turnover Analysis

---
## Report Visualization and Analysis

This analysis focuses on the HR data for the year 2023. For a more comprehensive review, including data from previous years, please refer to the .pbix file available in this project repository.

### Overall, Company Insights
<img src="https://i.imgur.com/LJmFJqG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

The insights analysis for this project begins with a general overview of the HR department:

- **Employees by department**
  
As showed on the above visual report, the company employed 208 people across six departments as of 2023. Notably, more than half of the workforce is concentrated in the Production department, which is the largest department by headcount. This is followed by the IT department, with the remaining employees distributed across other departments.

- **Gender Distribution**
  
The company's workforce is predominantly female, with women representing 55.77% of the total employees. This indicates a relatively balanced gender distribution, though slightly skewed towards female employees.

- **Age Distribution**
  
The age distribution of employees shows a significant concentration in the 30-40 year age group, with the average employee age being 38.6 years. This suggests that the company has a mature workforce, with a strong presence of mid-career professionals.

- **Recruitment Sources**
  
When analyzing recruitment sources for active employees in 2023, Indeed and LinkedIn emerge as the primary channels. The Treemap visualization highlights that Indeed was the most utilized source for new hires. However, it is important to note that the dominance of these recruitment sources can vary year over year, with LinkedIn sometimes taking the lead in previous years.

- **Salary Insights**
  
Although this analysis does not focus primarily on salary, it's worth mentioning that the average salary in 2023 was 70.57 KCHF per year. This provides a general context for the company's compensation levels.

**______________________________**
### HR Turnover Analysis <br />

<img src="https://i.imgur.com/jhZc16D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

This report dives deeper into employees turnover analysis, providing a more granular view with focus on the employees turnover for 2023, a critical metric for understanding the company's workforce stability: 

- **KPIs**
  
The data reveals that in 2023, 13 employees left the company, while only 2 new employees were hired, resulting in a turnover ratio of 6%. This indicates a significant gap between hires and leavers, which has implications for the company's operational effectiveness.

- **Hires and Leavers by Department**

The Production department is the most affected by turnover, with 10 employees leaving in 2023. Of these, only 2 were replaced. This imbalance could lead to potential productivity issues, as the department may struggle to maintain output with a reduced workforce.

- **Turnover Ratio by Gender**

The turnover data by gender shows that men represented nearly 60% of the leavers in 2023, a notable increase compared to previous years, where gender turnover was more balanced. This trend, which began in 2021, could indicate underlying issues specific to male employees that the company may need to address.

- **Reasons for Leaving**
  
In 2023, the primary reasons cited for leaving were seeking another position and the pursuit of higher pay. Over the years, these reasons, along with general dissatisfaction ("Unhappy"), have consistently been the top drivers for employee turnover. This suggests that the company might have challenges in both compensation and employee engagement that need to be addressed.


## Final Considerations and Recommendations
### Final Considerations

Analysis of the hires versus leavers trend from previous years shows a troubling pattern: while the company was able to replace most leavers up until 2020, the last three years have seen a decline in hiring, with many positions left unfilled. This widening gap could lead to significant challenges, such as:

**1. Productivity Issues:**
- *Insufficient staff to complete all tasks.*
- *Potential delays in production and other critical operations.*

**2. Increased Turnover:**
- *Remaining employees may become overburdened with extra responsibilities, leading to burnout and a higher likelihood of further resignations.*

### Recommendations
**1. Employee Retention Strategies:**

- *Enhance Compensation Packages: Regularly review and adjust salaries and benefits to remain competitive in the market.*
- *Career Development Opportunities: Implement clear career progression paths and offer training programs to increase job satisfaction and reduce turnover.*

**2. Recruitment and Replacement Efforts:**
- *Streamline Recruitment Processes: Invest in efficient recruitment technologies and strategies to fill vacant positions more quickly.*
- *Strengthen Employer Branding: Enhance the company’s reputation as an employer of choice to attract top talent, particularly in departments with high turnover.*
