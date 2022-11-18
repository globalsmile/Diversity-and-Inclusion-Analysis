# Pwc Switzerland Power BI virtual case experience - Diversity and Inclusion Analysis
<img align="right" alt="Diversity and Inclusion Analysis" width="1000" height = "400" src="https://www.pwc.ch/en/images/blog/virtual-case-experience/HC_Virtual%20Case%20Experience_1000x560_NWNS-Power%20BI.png">

---


# Table of Contents

- [Problem Statement](https://github.com/globalsmile/Diversity-and-Inclusion-Analysis#Problem-Statement)
- [Data Sourcing](https://github.com/globalsmile/Diversity-and-Inclusion-Analysis#Data-Sourcing)
- [Data Preparation](https://github.com/globalsmile/Diversity-and-Inclusion-Analysis#Data-Preparation)
- [Data Modeling](https://github.com/globalsmile/Diversity-and-Inclusion-Analysis#Data-Modeling)
- [Data Visualization](https://github.com/globalsmile/Diversity-and-Inclusion-Analysis#Data-Visualization)
- [Data Analysis](https://github.com/globalsmile/Diversity-and-Inclusion-Analysis#Data-Analysis)
- [Insights](https://github.com/globalsmile/Diversity-and-Inclusion-Analysis#Insights)
- [Shareable link](https://github.com/globalsmile/Diversity-and-Inclusion-Analysis#Shareable-Link)


---

# Problem Statement

INTRO :This project is the final project from the [Pwc Switzerland Power BI virtual case experience internship program](https://www.theforage.com/virtual-internships/prototype/a87GpgE6tiku7q3gu/PwC-Digital-Up-skilling-Virtual-Case-Experience) which I completed on Forage.

The purpose of this analysis is to: 
- Define proper KPIs in hiring, promotion, performance and turnover
- Create a visualisation for the HR manager that reflects all relevant Key Performance indicators(KPIs)
and metrics in the dataset.

The following measures could help to define proper KPIs:
- '#' of men
- '#' of women
- '#' of leavers
- % employees promoted (FY21)
- % of women promoted
- % of hires men
- % turnover
- Average performance rating: men
- Average performance rating: women

---

# Data Sourcing

The Dataset used for this analysis was presented by [Pwc Switzerland](https://www.pwc.ch/en/careers-with-pwc/students/virtual-case-experience.html) and available at:

- [Diversity Inclusion Dataset](https://github.com/globalsmile/Diversity-and-Inclusion-Analysis/blob/main/03%20Diversity-Inclusion-Dataset.xlsx)


---

# Data Preparation

Data transformation was done in Power Query and the dataset was loaded into Microsoft Power BI Desktop for modeling.

The diversity and inclusion dataset is given by a table named:

- `HR Manager` which has `32 columns and 500 rows` of observation


The tabulation below shows the `HR Manager` table with its column names and their description:
| Column Name | Description |
| ----------- | ----------- |
| Employee ID |   Represents the unique number of the employee in the dataset |
| Gender |  Describes the gender of the employee |
| Job Level after FY20 promotions |  Describes the job level of the employee after being promoted in FY20 |
| New hire FY20? |  Describes if the employee is a new hire in FY20 |
| FY20 Performance Rating |  Represents the performance rating of the  employee  in FY20 |
| Promotion in FY21? |  Describes if the employee is being promoted in FY21 |
| In base group for Promotion FY21 |  Describes if the employee is being selected for promoted in FY21 |
| Target hire balance |  Describes the target hire balance of the employee |
| FY20 leaver? |  Describes if the employee is a leaver in FY20 |
| In base group for turnover FY20 |  Describes if the employee is in a group for turnover in FY20 |
| Department @01.07.2020  |  Describes the department each employee belongs to as at January 7, 2020 |
| Leaver FY |  Describes if the employee is a leaver in a FY |
| Job Level after FY21 promotions |  Describes the job level of the employee after being promoted in FY21 |
| Last Department in FY20 |  Describes the last department each employee belongs in FY20 |
| FTE group |  Describes if the employee belongs to a FTE group |
| Time type |  Describes the contract type employee |
| Department & JL group PRA status |  Describes the department and JL group PRA status of the employee |
| Department & JL group for PRA |  Describes the department and JL group PRA  of the employee |
| Job Level group PRA status |  Describes the job level group PRA status of the employee |
| Job Level group for PRA |  Describes the job level group PRA of the employee |
| Time in Job Level @01.07.2020  |  Describes the time in job level of the employee |
| Job Level before FY20 promotions |  Describes the job level employee before being promoted in FY20 |
| Promotion in FY20? |  Describes if the employee is being promoted in FY20 |
| FY19 Performance Rating |  Describes the performance rating of the employee in FY19 |
| Age group |  Describes the age group of the employee |
| Age @01.07.2020 |  Represents the age of the employee as at January 07, 2020 |
| Nationality 1 |  Describes the nationality of the employee in state level |
| Region group: nationality 1 |  Describes the nationality of the employee in country level|
| Broad region group: nationality 1 |  Describes the nationality of the employee in regional level|
| Last hire date |  Describes the last hire date of the employee |
| Years since last hire |  Represents the number of years since last hire of the employee |
| Rand | generates random number for each entry in the dataset |


Data Cleaning for the dataset was done in power query as follows:

- Unnecessary columns were removed
- Unnecessary rows were filtered 
- Each of the columns in the table were validated to have the correct data type 

---

# Data Modeling

After the dataset was cleaned and transformed, it was ready to be modeled(using Power BI Desktop).

- The fact and dimension have been combined into one table and is shown in the data model below

<img align="right" alt="Data Model" width="1000" height = "400" src="https://user-images.githubusercontent.com/106287208/194948691-bbb923e4-1805-4ff4-a9f7-0fb3e1b9f902.JPG">



---


# Data Visualization

Data visualization for the dataset was done in 2 folds using Microsoft Power BI Desktop:

-  The `HR Manger (1/2)` Page: Shows the hiring KPI, promotion KPI, Turnover Rate (FY20 leavers) KPI, e.t.c
-  The `HR Manger (2/2)` Page: Shows the Performance rating KPI, Executive Gender Balance KPI, Age Group KPI, e.t.c

Figure 1 shows visualizations from `HR Manger (1/2)` page

| Figure 1 |
| ----------- |
| ![image](https://user-images.githubusercontent.com/106287208/194949076-adf39e10-97a7-46f1-a28f-8435fb9cf796.png) |


Figure 2 shows visualizations from `HR Manger (2/2)` page

| Figure 2 |
| ----------- |
| ![image](https://user-images.githubusercontent.com/106287208/194949761-9e6634ed-b5ea-409b-98bb-01e99d21b2d3.png) |


---

# Data Analysis

Measures used in visualization are:

- '#' of leavers = 
` CALCULATE(COUNTA('HR Manager'[Employee ID]), 'HR Manager'[Leaver FY] IN { "FY20" })`


- '#' of men = ` Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[Gender]="Male"))`


- '#' of women = ` Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[Gender]="Female"))`


- % employees promoted (FY21) = `Divide(Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[Promotion in FY21?]="Yes")),Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[In base group for Promotion FY21]="Yes")))`


- % of hires men = `Divide('HR Manager'[# of men],('HR Manager'[# of men]+'HR Manager'[# of women]))`


- % of hires women = ` Divide('HR Manager'[# of women],('HR Manager'[# of women]+'HR Manager'[# of men]))`


- % Promotees who were men = `Divide(Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[Gender]="Male")),distinctcount('HR Manager'[Employee ID]))`


- % Promotees who were women = `Divide(Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[Gender]="Female")),distinctcount('HR Manager'[Employee ID]))`


- % Turnover = `Divide(Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[FY20 leaver?]="Yes")),Divide(Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager','HR Manager'[In base group for turnover FY20]="Y"))+Calculate(distinctcount('HR Manager'[Employee ID]),Filter('HR Manager',NOT('HR Manager'[Department @01.07.2020]=BLANK()))),2))`


- Avg Rating Men = `Calculate(Average('HR Manager'[FY20 Performance Rating]),Filter('HR Manager','HR Manager'[Gender]="Male"))`


- Avg Rating Women = `Calculate(Average('HR Manager'[FY20 Performance Rating]),Filter('HR Manager','HR Manager'[Gender]="Female"))`



As shown from [Data Visualization](https://github.com/globalsmile/Diversity-and-Inclusion-Analysis#Data-Visualization), It can be deduced that:

- `41%` of hires were female
- `59%` of hires were male
- `53.8%` of promotees were women in the Junior Officer category, the highest for the year

---

# Insights

As shown by [Data Visualization](https://github.com/globalsmile/Diversity-and-Inclusion-Analysis#Data-Visualization), It can be deduced that:

- Avg Rating women `2.42%`
- Avg Rating women `2.41%`
- The most common age group  is `20-29` having `215` employees fall in this category


---


# Shareable Link

You can interact with the report here: 

[View Report](https://app.powerbi.com/view?r=eyJrIjoiOTQ1YTc3ZDUtNzZhNS00NzQwLTk1ZjgtNzgxNTMyYWU1OWE1IiwidCI6IjQ5ODY4YWYzLWNjNWYtNDIxNC04YjdmLTQwZjM3NDY0OWEwOSJ9)
