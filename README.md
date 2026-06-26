# Pipelines-Nyc-Pay-roll-Data-Analytics

1. Azure SQL Database – Create Payroll Transaction Table

CREATE TABLE [dbo].[NYC_Payroll_Data](
    [FiscalYear] [int] NULL,
    [PayrollNumber] [int] NULL,
    [AgencyID] [varchar](10) NULL,
    [AgencyName] [varchar](50) NULL,
    [EmployeeID] [varchar](10) NULL,
    [LastName] [varchar](20) NULL,
    [FirstName] [varchar](20) NULL,
    [AgencyStartDate] [date] NULL,
    [WorkLocationBorough] [varchar](50) NULL,
    [TitleCode] [varchar](10) NULL,
    [TitleDescription] [varchar](100) NULL,
    [LeaveStatusasofJune30] [varchar](50) NULL,
    [BaseSalary] [float] NULL,
    [PayBasis] [varchar](50) NULL,
    [RegularHours] [float] NULL,
    [RegularGrossPaid] [float] NULL,
    [OTHours] [float] NULL,
    [TotalOTPaid] [float] NULL,
    [TotalOtherPay] [float] NULL
);
3. Synapse – Employee Master Table

CREATE TABLE [dbo].[NYC_Payroll_EMP_MD](
    [EmployeeID] [varchar](10) NULL,
    [LastName] [varchar](20) NULL,
    [FirstName] [varchar](20) NULL
);
4. Synapse – Title Master Table

CREATE TABLE [dbo].[NYC_Payroll_TITLE_MD](
    [TitleCode] [varchar](10) NULL,
    [TitleDescription] [varchar](100) NULL
);
5. Synapse – Agency Master Table

CREATE TABLE [dbo].[NYC_Payroll_AGENCY_MD](
    [AgencyID] [varchar](10) NULL,
    [AgencyName] [varchar](50) NULL
);
6. Synapse – Payroll Transaction Table

CREATE TABLE [dbo].[NYC_Payroll_Data](
    [FiscalYear] [int] NULL,
    [PayrollNumber] [int] NULL,
    [AgencyID] [varchar](10) NULL,
    [AgencyName] [varchar](50) NULL,
    [EmployeeID] [varchar](10) NULL,
    [LastName] [varchar](20) NULL,
    [FirstName] [varchar](20) NULL,
    [AgencyStartDate] [date] NULL,
    [WorkLocationBorough] [varchar](50) NULL,
    [TitleCode] [varchar](10) NULL,
    [TitleDescription] [varchar](100) NULL,
    [LeaveStatusasofJune30] [varchar](50) NULL,
    [BaseSalary] [float] NULL,
    [PayBasis] [varchar](50) NULL,
    [RegularHours] [float] NULL,
    [RegularGrossPaid] [float] NULL,
    [OTHours] [float] NULL,
    [TotalOTPaid] [float] NULL,
    [TotalOtherPay] [float] NULL
);
7. Synapse – Payroll Summary Table

CREATE TABLE [dbo].[NYC_Payroll_Summary](
    [FiscalYear] [int] NULL,
    [AgencyName] [varchar](50) NULL,
    [TotalPaid] [float] NULL
);

8. Verify Data in SQL Database

SELECT *
FROM dbo.NYC_Payroll_Data;

9. Count Records in SQL Database

SELECT COUNT(*)
FROM dbo.NYC_Payroll_Data;

10. Verify Employee Master Data

SELECT *
FROM dbo.NYC_Payroll_EMP_MD;

11. Verify Title Master Data

SELECT *
FROM dbo.NYC_Payroll_TITLE_MD;

12. Verify Agency Master Data
SELECT *
FROM dbo.NYC_Payroll_AGENCY_MD;

14. Verify Payroll Data in Synapse
    
SELECT *
FROM dbo.NYC_Payroll_Data;

16. Verify Summary Table
    
SELECT *
FROM dbo.NYC_Payroll_Summary;

18. Count Records in Summary Table
    
SELECT COUNT(*)
FROM dbo.NYC_Payroll_Summary;

20. Verify Aggregated Results
    
SELECT FiscalYear,
       AgencyName,
       TotalPaid
FROM dbo.NYC_Payroll_Summary
ORDER BY FiscalYear, AgencyName;
       TotalPaid
FROM dbo.NYC_Payroll_Summary
ORDER BY FiscalYear, AgencyName;
