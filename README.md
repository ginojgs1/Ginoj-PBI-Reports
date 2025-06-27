
# HR Data Analysis-Dashboard

### Dashboard Link : https://app.powerbi.com/reportEmbed?reportId=8bd94727-21c6-48c9-b479-45304a26725d&autoAuth=true&ctid=7a95ad65-55ee-41e3-ba46-acbdf605ee3d

## Problem Statement

Market fluctuations andrapidly changing technology have affected the global market. Many published reports showed that around half of the employees wanted to change jobs. While some market researchers said that flexible working and job security were their primary factors, few admitted that a higher salary was their aim.Different regions saw an increase and a decrease in salariesover the years. While the increase was to retain top-level professional employees, the pay cuts were due to market fluctuations and were resorted after the market conditions improved. HR people across the globe are hiring new employees, trying to retain andunderstand the needs of employees who got separated (those who left the company).So,how does the HR department make these decisions in volatile market conditions? They rely on HR analytics to understand the existing situation and develop a new modern approach. For this requirement, you have been asked in your company to build a dashboard in Power BI considering the following challenges of HR people and provide an effective way to find the answers to their day-to-day questions.


### Task 

1.Use the HR dataset provided for this project andanalyze that to understand the data andterms.
2.Load data intothe Power BI Query Editor and perform the required actions.

3.Establish the required relationships (look at the hint section).

![Image](https://github.com/user-attachments/assets/6318f475-7287-47bd-991d-d3f4dc0384c0)

![Image](https://github.com/user-attachments/assets/6e34317e-0f93-4a3b-b4d6-5aecf2271c53)

        
4.Create the required DAX columns andmeasures to calculate the below things 

(look at the hint section).

▪Create the below-calculatedcolumn in the BUtable:

Region = mid([RegionSeq], 3,15)

![Image](https://github.com/user-attachments/assets/18d90fb2-df1a-4efb-9881-4dd10ae73009)

        
 ▪Create the below columns in the Employee table:

a.AgeGroupID = IF([Age]<30, 1, IF([Age]<50, 2, 3))

b.isNewHire = IF(YEAR([date]) = YEAR([HireDate]) && MONTH([date])=MONTH([HireDate]), 1)

c.TenureDays = IF([date]-[HireDate]<0,[HireDate]-[date],[date]-[HireDate])

▪Create a new measure table (separate table using Enter data) andplace all the measuresinto this table.

a.Create a new Measure EmpCount

Hint:EmpCount = CALCULATE(COUNT(Employee[EmplID]), FILTER(ALL('Date'[PeriodNumber]), 'Date'[PeriodNumber]= MAX('Date'[PeriodNumber])))

b.Create a Measure for Active Employees

Hint:Actives = CALCULATE([EmpCount], FILTER(Employee, ISBLANK(Employee[TermDate])))//total active employees

c.Create a Measure called New Hires, which will have the sum of the new NewHirein theEmployee table.

d.Create a Measure called Separations.
 
Hint:Separations = 

CALCULATE(COUNT(Employee[EmplID]), FILTER(Employee, NOT(ISBLANK(Employee[TermDate]))))

//separations/employees who left

e.Create a Measure called AVG Tenure Days which has an average column TenureDaysfromEmployeetable.

f.Create a Measure called AVG Tenure Months.

  Hint:AVG Tenure Months = ROUND([AVG Tenure Days]/30, 1)-1

g.Create a Measure called Female Emp Actives.

  Hint:Female Emp Actives = CALCULATE([Actives],Gender[Gender]=”Female”)

h.Create a Measure called Female New Hiresusing New Hires.

i.Create a Measure called Female Separationss

  Hint:Female Separationss = CALCULATE([Separations],Gender[Gender]="Female")

j.Create a Measure called Male Actives

  Hint:Male Actives = CALCULATE([Actives],Gender[Gender]="Male")//how many Active male employees

k.Create a Measure called Male New Hires

  Hint:Male New Hires = CALCULATE([New Hires],Gender[Gender]="Male")//how many new hire male employees

l.Create a Measure called Male Separations

  Hint:Male Separations = CALCULATE([Separations],Gender[Gender]="Male")// male employees who leftor separations
 
5.Based on the below design, create the report in Power BI. 

6.Implement row-level security based on the BU region.

7.After developing this, save your file as “FinalProject_YourName.pbix”.

8.Publish your report in my workspace using the demo PBI service account (provided during training) or your own account.

9.Create the dashboard in the Power BI workspace using the key visuals; identify the visuals thatshow key information and pin them on thedashboard.

10.Export the report to PowerPointand the dashboard to a PDFfile.

11.Submit the PowerPointreport, PDFdashboard,and.pbix file.
 
![Image](https://github.com/user-attachments/assets/02c7cfdf-37b8-430a-8336-f7dc8ad1ab20)

Note:You must considerthe above-mentioned requirements and give an appropriate solutionwith proper screenshots in a word/pdf file with the final .pbix file.

[FinalProject_Ginoj.pdf](https://github.com/user-attachments/files/20949910/FinalProject_Ginoj.pdf)
