# INCUBATOR-HUB-CAPSTONE-PROJECT
A detailed documentation of the report of capstone sales dataset
## Analysis of Capstone Project Sales Data
### PROJECT OVERVIEW
This project has to do with the analysis of the product performance of the capstone company as it relates with some important factor one of which is the location. 
It pays attention to the product with the highest performance and also the region with the highest performance.
### DATA SOURCES
- Microsoft Excel [Download Here](https://www.microsoft.com)
- The Incubator Hub Capstone Data Set
- 
### Data Cleaning and Preparations
##### Microsoft Excel was used to perform the following
- for Data Cleaning; in this phase, duplicates were removed, and new columns were added, also there are some data types that needed to be changed, these was also part of the task performed in this section.
- for Analysis; after ensuring the data was clean, a good number of analysis was carried out on the clean data. some of the formulas used with be updated in this report.
- Visualization; the pivot table is a very beautiful visualization tool in excel, this was used to ptesent the summary of the result.
    Next in line is the Structured Query Language.
    
##### SQL - (Structured Query Language), This model was used to write queries for all necessary reports needed, but befor writing the query, i imported the clean data from excel into my SQL work station. Here are the steps involved in importing the data.
- convert the excel 'xlsl' file to 'csv'(comma delimited) file
- open the SQL work station
- create a new data base or use an existing one
- click and right click on the database
- proceed to 'task', then to 'import flat file', pick your file from the appropriate location, change table name if necessary and click next.
- the data types were change to the compatible ones for SQL
- then the data was uploaded.
##### Power BI, The data used on excel was also imported to power Bi through the following steps
- Go to 'Get Data'
- click excel wook book
- pick your file
- click to preview
- then transform data

  ### DATA EXPLORATORY
  On the three analysis tool used for this project (excel, SQL and Power BI), thorugh data exploration was done, some new columns were added in excel, for example the 'Revenue' column, some other columns were added in SQL with the help of sql quesries and also in power BI, i added spme conditional column and also measures.
  The pivot table was used to summerise the report in excel, some pivot chats were also used.
  The were differen visuals generated on Power BI that gave an overview of the sales pattern as it was on excel. Power BI visuals also provided a detailed trend in the products performances as it relates to different regions.
### DATA ANALYSIS
##### The following analysis was done on excel using the excel formulas and functions
To calculate Revenue for each product (Revenu = Quantity*Unit Price)
```
=F2*G2
```
To get the Transaction Category
```
=IF(F2<=5,"Low",IF(F2<=10,"Medium","High"))
```
Total Quantity Sold
```
=SUM(F2:F9922)
```
Average Quantity Sold
```
=AVERAGE(F2:F9922)
```
Total Revenue Or Total Sales
```
=SUM(H2:H9922)
```
Average Revenue
```
=AVERAGE(H2:H9922)
```
Total Quantity Sold for Each Product
```
=SUMIF(C2:C9922,"productname",F2:F9922)
```
Total Revenue for each Product
```
=SUMIF(C2:C9922,"productname",H2:H9922)
```
Total Revenue generated by each Region
```
=SUMIF(D2:D9922,"Region",H2:H9922)
```
Average Revenue generated by each Region
```
=AVERAGEIF(D2:D9922,"Region",H2:H9922)
```

### EXCEL REPORTS
##### Below are the reports generated in excel.
![Screenshot 2024-11-05 144127](https://github.com/user-attachments/assets/cb25b41a-0730-4ffe-b456-5d8ea3da649c) ![Screenshot 2024-11-05 144144](https://github.com/user-attachments/assets/281a2413-20ee-451f-a036-e4e29ae008a9) ![Screenshot 2024-11-05 144225](https://github.com/user-attachments/assets/81c0c959-53df-4aba-b3c7-3b7a878071ae) ![Screenshot 2024-11-05 144250](https://github.com/user-attachments/assets/33a69d44-9ad9-4b94-8d46-618b96fc6b7f) ![Screenshot 2024-11-05 144304](https://github.com/user-attachments/assets/49e71445-3510-4a60-8b08-333772c5d2f1) ![Screenshot 2024-11-05 144329](https://github.com/user-attachments/assets/98204d37-23d4-40ac-a326-abb25415ecf5) ![Screenshot 2024-11-05 144354](https://github.com/user-attachments/assets/6cd140c9-6339-445c-96f7-00e797dbff96) ![Screenshot 2024-11-05 144407](https://github.com/user-attachments/assets/71e1373a-f139-4497-a391-d7f510a45b9b) ![Screenshot 2024-11-05 144430](https://github.com/user-attachments/assets/727119be-86aa-41d1-a3d3-eed3090f0a61) ![Screenshot 2024-11-05 144506](https://github.com/user-attachments/assets/720faf59-0bc9-4116-abb6-e612f3e88705) ![Screenshot 2024-11-05 144527](https://github.com/user-attachments/assets/4fa282d7-6e31-4df5-8aa0-164687741b0f) ![Screenshot 2024-11-05 144537](https://github.com/user-attachments/assets/3d62c4b5-5f1d-47db-bf6f-6dcbf48730e5) ![Screenshot 2024-11-05 144631](https://github.com/user-attachments/assets/4cffc8ae-1f9f-4bdb-a66a-f5591d41a651) ![Screenshot 2024-11-05 144641](https://github.com/user-attachments/assets/ab28b433-b880-4cdd-b5fd-45b8b49d6486)

##### SQL (Below are some of the queries run on SQL)
- To retrieve the total sales for each product category
```
select product,sum(revenue) as Total_Revenue
from[dbo].[SALES_DATA_] Group by Product
```
- Number of sales transaction in rach region
```
Select Region,sum(Revenue) as Total_Sales
from  [dbo].[SALES_DATA_] Group by Region
```
- Highest selling product by total sales value
```
Select Product, sum(Quantity) as Total_sales_or_Total_Quantity_Sold
from [dbo].[SALES_DATA_] Group by Product
Order by Total_sales_or_Total_Quantity_Sold Desc
```
- Total Revenue per product
```
Select Product,sum(Revenue) as Total_Revenue_per_Product
from [dbo].[SALES_DATA_]
Group by Product
```
- Total Revenue by Region
```
Select Region,sum(Revenue) as Total_Revenue_per_Region
from [dbo].[SALES_DATA_]
Group by Region
```
- Monthly sales total for the current year
  Some queries were written to alter the existing table in order to add the months of transaction befor writing a query for the monthly sales data for the current year. 
```
SELECT SUM(Quantity) AS TOTAL_SALES FROM [dbo].[SALES_DATA_]
WHERE OrderYear = '2024'
Group by Order_Month
```
- Top 5 customers by total purchase amount
```
Select Top 5 Customer_id,sum(Quantity) as Total_Purchase_Amount
from [dbo].[SALES_DATA_]
Group by Customer_Id
order by Total_Purchase_Amount desc
```
- The percentage of total sales contributed by each region
```
SELECT Region, SUM(Revenue)/SUM(Quantity)*0.1 as Percentage_of_Total_Sales
From [dbo].[SALES_DATA_] 
Group by Region
Order by Percentage_of_Total_Sales desc
```
- Products with no sales in the last quarter.
```
Select Product,Sum(Quantity) as Nil_Sales
From [dbo].[SALES_DATA_]
Where Month(OrderDate) between 10 and 12
Group by Product Having Sum(Quantity)= 0
```
###### Below are some of the results of the query
![Screenshot 2024-11-07 103217](https://github.com/user-attachments/assets/40281d1a-ba27-477c-8712-959afd7c4742)
![Screenshot 2024-11-07 103246](https://github.com/user-attachments/assets/727a9e6b-5596-451e-bc22-be3a7d5e754d)
![Screenshot 2024-11-07 103358](https://github.com/user-attachments/assets/f7cba088-2c66-4a74-ac0d-4db55055bb63)
![Screenshot 2024-11-07 103418](https://github.com/user-attachments/assets/7cadd5e5-c63f-4318-92e1-4fe3c4b9cfa1)
![Screenshot 2024-11-07 103455](https://github.com/user-attachments/assets/de4cfc5f-ffe0-4aa4-aeb3-4f485b836ed2)
![Screenshot 2024-11-07 103521](https://github.com/user-attachments/assets/b653c6b6-c21f-4053-9893-3cfa35390747)

##### Analysis on Power BI
some of the following analysis were carried out on Power BI with DAX function




