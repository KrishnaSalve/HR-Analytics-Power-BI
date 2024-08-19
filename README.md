# HR Analytics Dashboard


## Problem Statement

This dashboard helps the HR Personels and gives better understanding of the reasons behind Employees Attrition. Employee attrition poses a significant challenge for organizations, affecting productivity, morale, and business continuity. High attrition rates lead to increased recruitment and training costs, loss of organizational knowledge, and potential disruptions in team dynamics. Despite regular efforts to improve employee retention, the current attrition rate is above the industry's average, indicating a need for a more systematic approach to understand and address the root causes.

The primary objective of this HR analytics project is to analyze attrition patterns within the organization, identify key factors contributing to employee turnover, and develop predictive models to proactively manage and mitigate attrition risk. The project will involve gathering and analyzing data related to employee Salary, Age, Education, Years of work at company, Job Roles, Job Satisfaction.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.

- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.

- Step 3 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".

- Step 4 : Promote first row of the data as the Headers which are nothing but the column names, by going through Transform tab under Table section select "Use first row as headers".

- Step 5 : Change the types of column based on their respective data types, by clicking on "Detect Data Type" under Any Column section in Transform tab, which will automatically detect the data types of columns.

- Step 6 : Removing column such as 'YearsWithCurrManager' which doesn't provide any better Insights about the Employee.

- Step 7 : Removing duplicate values from "EmpID" column.

- Step 8 : Replacing the values from "BusinessTravel" column such as 'TravelRarely' to 'Travel_Rarely' which have same meaning, by selecting option as Replace values from "Replace value" button under Any Column section in Transform tab.

- Step 9 : Add New Column named as 'Attrition_Count' by going into Add Column tab under General section select "Add Conditional Column" which specifies that if Attrition column value is 'Yes' then take Attrition_Count value as 1 else 0.

- Step 10 : After all the changes made goto Home tab under Close section click on "Close & Apply" to save the Transformed Data.

- Step 11 : After Transformation of Data we have created the Dashboard by considering all the Informative Insights about Attrition of Employees.

- Step 12 : First we have created 6 Cards to showcase the primary info such as,

   (a) "Count of Employees" - By doing summation of EmpID values from data.
   
    A card visual was used to represent Count of Employees.

  ![Screenshot_20240817_194312](https://github.com/user-attachments/assets/87ac0780-848e-46ca-9562-2548e102a380)


   (b) "Attrition" - Sum of values from Attrition_Count column.
    
    A card visual was used to represent Count of Attrition.

  ![Screenshot_20240817_194438](https://github.com/user-attachments/assets/90d67082-7dce-427f-9511-f352ed8cd19a)


   (c) "AttritionRate" - which shows the percent of employees with Attrition. 

  
    
      for creating Attrition Rate new measure was written; 
    
      AttritionRate = SUM(HR_Analytics[Attrition_Count]) / SUM(HR_Analytics[EmployeeCount])


    A card visual was used to represent Percent of Attrition Rate.

  ![Screenshot_20240817_194543](https://github.com/user-attachments/assets/02c86e79-2726-496c-a86a-5563fb6ac3ca)


   (d) "Avg. Salary" - Avg. monthly salary of employees.

   A card visual was used to represent Average Salary.

  ![Screenshot_20240817_194648](https://github.com/user-attachments/assets/e20a0886-7a80-4d55-801f-c68e235779b5)


   (e) "Avg. Years" - Avg. years of work at a company.

   A card visual was used to represent Employees Average years of work at company.

  ![Screenshot_20240817_194752](https://github.com/user-attachments/assets/a3b8320c-8a98-4347-90a8-34bc2e25dd21)


   (f) "Avg. Age" - Avg. Age of Employees

   A card visual was used to represent Average age of Employees with Attrition.

  ![Screenshot_20240817_194902](https://github.com/user-attachments/assets/41f2de06-01b2-4e2d-a7f3-87da56f22ec9)

       Using visual level filter from the filters pane, basic filtering was used & 
       Although, while Transforming the Data we have eliminated all the Null values and 
       blank values None of them were taken into consideration for average calculations.
           
       Although, by default, while calculating average, blank values are ignored.
- Step 13 : A Treemap chart was also added to the report design area representing the number of Male and Female w.r.t Attrition. While Blue color represent the count of Male and pink color represent count of Female for Attrition. 

  ![Screenshot_20240817_210923](https://github.com/user-attachments/assets/3d9916d9-7f7b-4ba2-a41d-33c6cc7d4c40)

- Step 14 : A donut chart is created representing Education field of Employees with Attrition and legend representing Education field and values as sum of Attrition count.

  ![Screenshot_20240817_211253](https://github.com/user-attachments/assets/39ac3875-3954-4f7b-9c70-36918e916681)

  i) 38 % of Employees with Education field as Life Sciences.

  ii) 27 % of Employees with Education field as Medical.

  iii) 15 % of Employees with Education field as Marketing.

  iv) 14 % of Employees with Education field as Technical Degree.

  v) 4.6 % and 2.9 % with Education field as Others and Human Resources respectively.


- Step 15 : A Stacked Column Chart was added to report to showcase a Age of Employees with Attrition where Age Group gap is taken of 10 years with 18 as minimum age of employee and 55+ is maximum from our data. Also, X-axis represents Age Group and Y-axis represents Attrition Count of Employees.

  ![Screenshot_20240817_214310](https://github.com/user-attachments/assets/4ea26b51-f9ad-464c-8364-c2c11a72847b)

  i) 116 Employees with Attrition comes from Age Group of 26 to 35.

  ii) 44 Employees with Attrition comes from Age Group of 18 to 25.

  iii) 43 Employees with Attrition comes from Age Group of 36 to 45.

  iv) 26 Employees with Attrition comes from Age Group of 46 to 55.

  v) 8 Employees with Attrition comes from Age Group of 55+

- Step 16 : A Stacked bar chart for Count of Employees with Attrition and Salary Slab they lie in. X-axis represents Count of Employees with Attrition and Y-axis represents Salary Slab.

  ![Screenshot_20240817_222534](https://github.com/user-attachments/assets/282441f1-df2e-45ee-8e89-9e06d9c398e0)

  i) 163 Employees with Attrition has salary upto 5k

  ii) 49 Employees with Attrition has salary between 5k to 10k

  iii) 20 Employees with Attrition has salary between 10k to 15k

  iv) 5 Employees with Attrition has salary above 15k 


- Step 17 : We have also added Area chart which represents Employees with their years of work at company, where X-axis gives us Years at Company and Y-axis gives us Count of Employees with Attrition. We have used visuals like solid line as line style and Shade area with transparency of 67%.

  ![Screenshot_20240817_223525](https://github.com/user-attachments/assets/aee9f483-8ec4-4fc0-94f6-4cbe51180bc2)

  i) 16 Employees with Attrition has been working with company for less 1 year 

  ii) 59 Employees with Attrition have been working with company for 1 year or above

  iii) 27 Employees with Attrition who have worked with company for 2 years or above

  iv) 20 Employees with Attrition who have worked with company for 3 years or above

  v) 19 Employees with Attrition who have worked with company for 4 years or above

  vi) 21 Employees with Attrition who have worked with company for 5 years or above

  vii) 9 Employees with Attrition who have worked with company for 6 years or above

  viii) 11 Employees with Attrition who have worked with company for 7 years or above

  ix) 9 Employees with Attrition who have worked with company for 8 years or above

  x) 8 Employees with Attrition who have worked with company for 9 years or above

  xi) 18 Employees with Attrition who have worked with company for 10 years or above

  xii) 2 Employees with Attrition who have worked with company for more than 10 years.


- Step 18 - To represent Count of Employees with Attrition and their respective Job Roles we have added Stacked Column Chart to our report with X-axis as Count of Employees and Y-axis as Job Roles.

  ![Screenshot_20240817_231416](https://github.com/user-attachments/assets/d578527c-6653-49b8-b078-dca9e3628dc2)

  i) 62 Employees with Attrition are from Laboratory Technician job role

  ii) 57 Employees with Attrition are from Sales Executive job role 

  iii) 47 Employees with Attrition are from Research Scientist job role

  iv) 33 Employees with Attrition are from Sales Representative job role

        
- Step 19 : A Matrix view was created in report with Rows as "Job Role", Columns as "Job Satisfaction" to gives Total values of Count of Employees with Attrition in their respective job roles and their job satisfaction rating between 1 to 4 where 1 represents low job satisfaction and 4 represents High job satisfaction.
     Also, we have applied Subtotal label for column which gives count of employees with Attrition for each job satisfaction rating, we have also applied Row subtotals which give count of employees with Attrition from respective Job Roles.
  
  In Matrix view, cell element's font color with Highest count is shown by dark blue color and tranparency gets reducing with count and lower count font color is represented by white color.

  ![Screenshot_20240818_103643](https://github.com/user-attachments/assets/8f558d95-40dd-482e-b58e-caf666e322f3)



 
 # Report Snapshot (Power BI DESKTOP)

 
![Screenshot_20240818_105632](https://github.com/user-attachments/assets/f44932f7-254a-4e25-8629-8b3efd8d4ba2)


# Transform Data Snapshot (Power BI Power Query)
![Screenshot_20240818_110242](https://github.com/user-attachments/assets/ef331731-9be5-4c32-be74-b60f012e5026)




# Insights

A single page report was created on Power BI Desktop & and Data was Transformed in Power BI Query.

Following inferences can be drawn from the dashboard;

### [1] Attrition Rate 

   Total Number of Employees 1470 out of which 237 opted 'Yes' for Attrition, whereas remaining opted 'No' for Attrition.

   i) 237 Employees opted for Attrition which is 16.1 % of Total Count of Employees.

   ii) Remaining which do not opted for Attrition makes upto 83.9 % of Total Count of Employees.


        thus, from above calculations we can come to conclusion that Most of the Employees like their jobs, 
        which is good for company.
        It indicates that the organization is able to provide a positive working environment, 
        meet employee needs, and foster job satisfaction.
           
### [2] Attrition by Education

        It's been noticed that most of Employees with Attrition come from Education Field 
        such as Life Science(38%), Medical(27%), Marketing(15%), Technical Degree(14%) 
        while 4% comes from Other Education field and 2% from Human Resources.
  
  while calculating average rating, null values have been ignored as they were not relevant for some customers. 
    
  
  ### [3] Attrition by Age  
  
      It's seen that most of Employees whose Age lies in Age Group of 26-35 have opted more for Attrition compare to other Age Groups.
      Out of 237 Employees with Attrition, 116 Employees age between 26-35, 44 Employees age between 18-26, 
      43 Employees age between 36-45, 26 employees age between 46-55 and 8 Employees age above 55 years. 
We can come to conclusion that, most of the young employees or work force with Attrition is not satisfied with their job or not comfortable with working environment.


### [4] Attrition by Salary 
  
      163 Employees out of total employees with Attrition have salary upto 5k, 
      49 employees salary lies in between 5k-10k, 20 employees salary lies between 10k-15k 
      and 5 employees salary is above 15k.
from above data, it is seen that most of the employees are unsatisfied with their job due to low wages or are under paid.
This could be one of the major reasons why employees are Resigninig or leaving the company.


### [5] Attrition by years at company
  
      It's seen that, most of the employees with Attrition have worked with 
      company for 1 year or above. Count of 59 employees who have worked for 
      1 year or above at company have left the company due to unsatisfaction. 
      16 employees have worked at company for less than 1 year.
We can come to conclusion that, most of the employees leave company at very early stage due poor job fit, lack of training, or insufficient support.


### [6] Attrition by Job Roles
  
      62 employees out of 237 employees with Attrition come from Laboratory Technician Department, 
      while 57 employees with Attrition come from Sales Executive job role, 
      47 employees are from Research Scientist Department, and 33 employees come from Sales Representative Department
Job Roles like Laboratory Technician, Sales Executive, Research Scientist, and Sales Representative are some of the Job Roles which have Highest Attrition Rate among the other 9 Job Roles.

 ### [7] Some other insights
 
 ### Business Travel
 
 1.1) 70 % of Employees travel Rarely.
 
 1.2) 18 %  of Employees travel Frequently.
 
 1.3) 10 % of Employees comes under Non-Travel Category.
 
         thus, maximum Employees travel Rarely due to work.
 
 ### Gender
 
 2.1)  60 % of Employees are Male which make upto 882 Employees out of 1470 total employees, 
 among which 140 Employees opted for Attrition.
 
 2.2)  40 %  of Employees are Femalewhich make upto 588 out of 1470 total employees, among which 79 employees opted for Attrition.


