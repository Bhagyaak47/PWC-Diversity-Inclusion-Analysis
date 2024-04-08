# PWC-Diversity-Inclusion-Analysis
PwC Power BI Virtual Case Experience Task 3- Hiring Diversity and Inclusion Analysis Dashboard
  
  
In this project create a dashboard in Power BI that reflects the Inclusion analysis and Hiring diversity for further decision making and strategies for future hiring.

- Define relevant KPIs in hiring, promotion, performance and turnover, and create a visualisation
- Write what you think some root causes of their slow progress might be

# Dataset :
The dataset used for this task was presented by https://www.theforage.com

# Data Cleaning/ Preparation:

- The data consists of over 500 rows and 32 columns.
- Changed the datatypes of some columns.
- Removed unnecessary columns.
- Replaced Y and N with yes and no respectively for better readability.
- Some columns are blank which can be kept blank and will not affect the analysis.
- Split 2 columns by Delimiter 1.Job Level after FY20 Promotion 2.Job Level after FY21 Promotion

# Dax Formulas :

- Total Employees = COUNT(Pharma[Employee ID])
- Total Male Employees = CALCULATE(DISTINCTCOUNT('Pharma'[Employee ID]),FILTER('Pharma','Pharma'[Gender]="Male"))
- Total Female Employee = CALCULATE(DISTINCTCOUNT(Pharma[Employee ID]),FILTER(Pharma,Pharma[Gender]="Female"))
- Avg Female Performance Rating FY19 = CALCULATE(AVERAGE(Pharma[FY19 Performance Rating]),Pharma[Gender]="Female")
- Avg Female Performance Rating FY20 = CALCULATE(AVERAGE(Pharma[FY20 Performance Rating]),Pharma[Gender]="Female")
- Avg Male Performance Rating FY19 = CALCULATE(AVERAGE(Pharma[FY19 Performance Rating]),Pharma[Gender]="Male")
- Avg Male Performance Rating FY20 = CALCULATE(AVERAGE(Pharma[FY20 Performance Rating]),Pharma[Gender]="Male")
- Employees left in FY20 = CALCULATE(COUNT(Pharma[FY20 leaver?]),Pharma[FY20 leaver?]="Yes")
- Hired in FY20 = CALCULATE(COUNT(Pharma[New hire FY20?]),Pharma[New hire FY20?]="Yes")
- Promoted in FY20 = CALCULATE(COUNT(Pharma[Promotion in FY20?]),Pharma[Promotion in FY20?]="Yes")
- Promoted in FY21 = CALCULATE(COUNT(Pharma[Promotion in FY21?]),Pharma[Promotion in FY21?]="Yes")
- Total Employees before FY21 Hiring = (CALCULATE(count(Pharma[FY20 leaver?]),Pharma[FY20 leaver?]="No")+[Hired in FY20])
- Turnover Rate % = DIVIDE([Employees left in FY20],[Total Employees])

# Questions to be answered:
- Total employees, Male and Female Employees.
- Filtering by department and gender.
- Employees by age group, gender regions etc.
- Hiring trend over the years etc
- Performance Ratings of FY19 and FY20.
- Other metrics like total hiring, turnover rate, total promotions etc.
- Job levels after promotions

![Pwc Diversity   Inclusion (1)_001](https://github.com/Bhagyaak47/PWC-Diversity-Inclusion-Analysis/assets/152842490/69c87dd8-66ac-4f61-98c9-5a57bac07065)
![Pwc Diversity   Inclusion (1)_002](https://github.com/Bhagyaak47/PWC-Diversity-Inclusion-Analysis/assets/152842490/d693987b-5a65-428e-9afd-46ba88ffda00)


# Insights :
- There are a total of 500 employees out of which 295 are male(59%) and 205 are female(41%) employees.
- From the age group, we can see that the age group 60-69 consists of only male employees whereas there is a mix of male and female employees in other age groups. The majority of employees are from the 20-29 age group.
- Most of the part-time workers are women in the company and full-time is dominated by males in the company.
- The company is most probably situated in Europe therefore majority of the employees are from Europe and Switzerland regions.
- The hiring trend took a boom after 2015 but dropped in 2019 due to some reasons and again increased in 2020.
- The turnover rate is 9.4%. the turnover rate for females is around 10% and that of males is 8%.
- The majority of the employees who left the company in FY20 were from the operations department but also most people were hired in operations.
- The FY19 performance rating for males is 2.58 whereas for females it is 2.56.
- All the departments except HR have male employees as its majority but in HR there are over 70% females and 30% males. Also, the performance rating of FY19 is the highest for the HR department for both males and females.
- We can see the FY20 performance rating dropped to 2.41 for males and 2.42 for females.
- 36 employees were promoted in FY20 and 51 employees were promoted in FY21 i.e. 41% more than the previous year.
- 47 employees left the company and 66 were hired by the company in FY20. There is no data for the FY21 hiring and up till then there are 519 employees.
- Out of 36 employees promoted(FY20) almost 78% were males and 22% of females received promotions. The sales and Marketing department received maximum promotions whereas there were no promotions from the HR department.
- Out of 51 employees promoted(FY21) almost 64% were males and 36% of females received promotions. Definitely, there was an increase in the promotions of female employees. The sales and Marketing department received the maximum promotions whereas there were low promotions from the Finance department.
- The job-level employee numbers also increased or decreased depending on the promotions. For eg, the number of executives (both male and female) increased in FY21 whereas female managers decreased in FY21.

# Recommendations:
- There are fewer employees from the 16-19 age groups. The company can hire interns to increase age diversity which can thereby increase the part-time jobs in the company.
- The company should hire employees from overseas countries who can do remote work.
- The decreased performance rating should be analysed as to why it decreased from the previous year.
- Various departments should be analysed as to why are the employees leaving and where hiring is needed.
- Encouraging healthy work-life balance and various factors can be implemented to reduce the turnover rate.
