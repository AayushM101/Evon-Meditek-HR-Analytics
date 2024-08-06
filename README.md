# HR Attrition Analysis for Evon Meditek Ltd.
## Problem statement

### Background:
Evon Meditek Ltd., a leading medical technology company, has been experiencing noticeable attrition rates among its employees. This trend is a concern for the company's management, as it can impact overall productivity, employee morale, and operational costs. Vipin Singh, the HR Manager, is keen to understand the underlying factors contributing to employee attrition and to gain insights into other relevant HR metrics.

### Objective:
The primary objective of this analysis is to investigate the reasons behind employee attrition at Evon Meditek Ltd. and to identify patterns and trends that can inform strategic decisions. Additionally, this analysis aims to provide a comprehensive overview of other key HR metrics that can offer a holistic understanding of the workforce dynamics.

### Key Questions to Address:

- What are the primary factors contributing to employee attrition at Evon Meditek Ltd.?
- Are there specific departments or job roles with higher attrition rates?
- What are the demographic characteristics (e.g., age, gender, tenure) of employees who are leaving the company?
- How do compensation, benefits, and work-life balance influence employee retention?
- What is the impact of employee engagement and job satisfaction on attrition rates?
- How do the attrition rates at Evon Meditek Ltd. compare to industry benchmarks?

#### Other HR Metrics to Analyze:

- Employee Demographics: Age, gender, education level, and tenure distribution.
- Performance Metrics: Employee performance ratings and their correlation with attrition.
- Employee Engagement: Levels of engagement and job satisfaction across different departments.
- Training and Development: Participation in training programs and their impact on retention.
- Work-Life Balance: Analysis of work hours, flexibility options, and employee feedback on work-life balance.


### Expected Outcome:
By analyzing these aspects, the goal is to develop actionable insights and recommendations that can help Evon Meditek Ltd. reduce attrition rates and improve overall employee satisfaction and retention. This analysis will also support the HR department in identifying potential areas for improvement and aligning HR strategies with the company's long-term objectives.

### Steps followed 

#### Step 1 : Extract, Transform & Load

- Launch Power Query Editor, 
following operations are performed:

  (a) Promote First column as headers.

  (b) Check for Duplicate and blank Data.
  
  (c) Rectifying data type.

  (d) Removing Junk column and data. 

  (e) Add a column for  Attrition count.

   conditional column 

    if attrition = yes output = 1
    else 0
  
#### Step 2 : Data Modelling 
  
  (a) Single dataset contains all data so Modelling is not required but simplify we can use pivot tables.

#### Step 3 : Metrics and DAX 
  

- 1 :Number of employee : 


      SUM('HR data'[Employee Count])

 
- 2 :Attrition:

     Sum('HR data'[Attrition Count])
        
- 3 : Attrition Rate :

      SUM('HR data'[Employee Count])/Sum('HR data'[Attrition Count])
  ![Screenshot 2024-08-06 185734](https://github.com/user-attachments/assets/e587f2a4-aa7e-471d-994f-7d10365f9578)

- 4 : Active Employee :

     SUM('HR data'[Employee Count])-Sum('HR data'[Attrition Count])

     ![Screenshot 2024-08-06 185701](https://github.com/user-attachments/assets/bfdc96d4-52b7-4734-944a-7858412498c5)

## Dashboard Designing 

- Add card for Number of Employee

- Add card for Attrition card 
  
- Add donut and Card chart for Attrition rate
- Add donut and card Active Employees vs department
- Add card for average age 
- Add bar chart for Attritioncount vs Department 
- Stacked bar and line chart - 
                X axis = Age band 
                y axis = Employee count 
                line = Attrition rate 
                legend = Gender 
  
*Change Under 25 to 18-25 to arrange the graph in order 

launch power query 
filter column for under 25 and replace value with 18-25
apply remove filter
sort axis age band in ascending order.

- Matrix - 
  (1) Job satisfaction
  (2) Job role 
  (3) Employee count 
  add cell elements and add highest to lowest gradient.

- Attrition count vs Education Field - stacked bar chart

- Attrition by Age band 
- Slicer - Education 

   ![Screenshot 2024-08-06 185714](https://github.com/user-attachments/assets/0922a3b3-f0ee-417a-ab04-26596b7d0c0a)
 
## Conclusion

In conclusion, the analysis of employee attrition at Evon Meditek Ltd. reveals critical insights:

- Attrition Rate Comparison: Evon Meditek Ltd. currently has an annual attrition rate of [16.12%]. Compared to the industry benchmark of 10% to 20%, this rate indicates [a higher average] level of employee turnover.

- Departmental Analysis: The highest attrition rate is observed in the [Sales department], with a rate of [20.63]%. This is significantly higher than the company average and suggests targeted interventions are necessary in this area.

- Demographic Insights: Employees aged [18-25] and those with tenure of [1-2 years] have the highest attrition rates, at [39.18]% and [28.66]% respectively. Addressing the needs and concerns of these demographic groups could significantly reduce overall attrition.

- Job Satisfaction and Engagement: Survey results indicate that employees with low engagement scores have an attrition rate of [22.46]%, versus [12.18]% for highly engaged employees. Improving engagement initiatives could thus reduce turnover.

- Comparative Metrics: The attrition rate for Evon Meditek Ltd. is [16.12]% higher/lower than the regional average for similar companies, which stands at [12]%.

## Dashboard 

![Screenshot 2024-08-06 185649](https://github.com/user-attachments/assets/1b9f8be0-eecb-45b9-9f8d-6d1c3cfcbe5b)
