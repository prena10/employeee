CREATE EXTERNAL TABLE employee
(
Age int,
Attrition boolean,
BusinessTravel string,
DailyRate int,
Department string,
DistanceFromHome int,
Education int,
EducationField string,
EmployeeCount int,
EmployeeNumber int,
EnvironmentSatisfaction int,
Gender string,
HourlyRate int,
JobInvolvement int,
JobLevel int,
JobRole string,
JobSatisfaction int,
MaritalStatus string,
MonthlyIncome int,
MonthlyRate int,
NumCompaniesWorked int,
Over18 string,
OverTime boolean,
PercentSalaryHike int,
PerformanceRating int,
RelationshipSatisfaction int,
StandardHours int,
StockOptionLevel int,
TotalWorkingYears int,
TrainingTimesLastYear int,
WorkLifeBalance int,
YearsAtCompany int,
YearsInCurrentRole int,
YearsSinceLastPromotion int,
YearsWithCurrManager int
)
ROW FORMAT DELIMITED FIELDS TERMINATED BY ','
LINES TERMINATED BY '\n'
STORED AS TEXTFILE LOCATION '/Employee'
TBLPROPERTIES("skip.header.line.count"="1");
CREATE TABLE employee_sales AS
SELECT *
FROM employee;
SELECT Attrition, Department, JobSatisfaction, ROUND(MonthlyIncome, -3) AS Rounded_MonthlyIncome
FROM employee_sales;

SELECT Attrition, Department, JobSatisfaction, ROUND(MonthlyIncome, -3) AS Rounded_MonthlyIncome
FROM employee_sales
SELECT Attrition, Department, JobSatisfaction, ROUND(MonthlyIncome, -3) AS Rounded_MonthlyIncome
FROM employee_sales
WHERE Department = 'Sales Department

SELECT Attrition, Department, JobSatisfaction, ROUND(MonthlyIncome, -3) AS Rounded_MonthlyIncome
FROM employee_sales
WHERE Department = 'Sales Department'
ORDER BY JobSatisfaction DESC;
