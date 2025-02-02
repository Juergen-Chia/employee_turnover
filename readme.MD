# Employee Retention Analysis - Salifort Motors

## Project Overview
This notebook analyzes employee data to identify factors contributing to employee turnover at Salifort Motors. The analysis aims to help the company understand why employees leave and propose solutions to reduce turnover rates.

## Dataset Description
The analysis uses the HR_capstone_dataset.csv containing employee information with the following variables:

- `satisfaction_level`: Employee-reported job satisfaction [0-1]
- `last_evaluation`: Score of employee's last performance review [0-1]
- `number_project`: Number of projects employee contributes to
- `average_monthly_hours`: Average monthly working hours
- `time_spend_company`: Years at the company (tenure)
- `work_accident`: Whether they had a workplace accident
- `left`: Whether the employee left the company
- `promotion_last_5years`: Whether they were promoted in the last 5 years
- `department`: Employee's department
- `salary`: Salary level (low, medium, high)

## Analysis Steps

### 1. Data Preprocessing

- Loaded and cleaned the dataset containing 14,999 employee records
- Identified and removed 3,008 duplicate entries
- Standardized column names and data types
- Checked for missing values (none found)
- Examined outliers using IQR method

### 2. Exploratory Data Analysis

Key findings from initial analysis:

1. Turnover Rate:
   - 16.6% of employees left the company
   - This represents a significant turnover rate requiring attention

2. Satisfaction and Evaluation Patterns:
   - Clear clustering in satisfaction levels among departing employees
   - Identified group of high-performing but unsatisfied employees who left
   - Another cluster shows low satisfaction and low evaluation scores

3. Working Hours and Projects:
   - Employees who left often worked significantly more than average
   - Higher turnover rates among those with 6-7 projects
   - Evidence suggests overwork may be a contributing factor

4. Department and Salary Insights:
   - Certain departments show notably higher turnover
   - Lower salary levels correlate with higher turnover
   - Salary impact varies by department

5. Tenure Patterns:
   - Peak turnover at 3-4 years of tenure
   - Both very new and long-tenured employees show lower turnover rates
   - Satisfaction levels vary significantly with tenure

### 3. Model Development

Two models were developed to predict employee turnover:

#### Logistic Regression Results:
- Accuracy: 83%
- Precision: 50% for predicting departures
- Recall: 21% for identifying potential leavers
- Better at predicting who will stay than who will leave

#### Random Forest Results:
- Accuracy: 97.9%
- Precision: 94.6%
- Recall: 92.7%
- AUC Score: 0.958
- Significantly better performance across all metrics

### 4. Feature Importance

Most important factors in predicting turnover:
1. Last evaluation score
2. Number of projects
3. Tenure
4. Monthly hours
5. Satisfaction level

## Business Recommendations

### Immediate Actions
1. **Employee Feedback System**
   - Implement regular satisfaction surveys
   - Create structured feedback sessions
   - Establish clear communication channels

2. **Workload Management**
   - Review project allocation processes
   - Set guidelines for maximum concurrent projects
   - Monitor monthly working hours

3. **Career Development**
   - Develop clear progression paths
   - Create structured promotion cycles
   - Implement mentorship programs

### Policy Changes
1. **Work-Life Balance**
   - Set policies on maximum working hours
   - Implement flexible working arrangements
   - Create guidelines for project allocation

2. **Compensation and Benefits**
   - Review salary structures, especially in high-turnover departments
   - Implement regular market-rate adjustments
   - Develop performance-based incentives

3. **Department-Specific Initiatives**
   - Address department-specific turnover factors
   - Create targeted retention strategies
   - Review resource allocation across departments

### Long-term Strategic Recommendations
1. **Organizational Culture**
   - Foster positive work environment
   - Promote work-life balance
   - Encourage professional development

2. **Performance Management**
   - Revise evaluation systems
   - Create fair and transparent promotion criteria
   - Implement regular check-ins

## Model Implementation Strategy

1. **Early Warning System**
   - Use Random Forest model to identify at-risk employees
   - Monitor key indicators (workload, satisfaction, etc.)
   - Enable proactive intervention

2. **Regular Monitoring**
   - Track turnover metrics by department
   - Monitor effectiveness of implemented changes
   - Adjust strategies based on outcomes

## Expected Impact
- Reduced turnover rates
- Improved employee satisfaction
- Better resource allocation
- Reduced hiring and training costs
- Enhanced organizational stability