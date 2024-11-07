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
The following analysis was done on excel using the excel formulas and functions
- To calculate Revenue for each product (Revenu = Quantity*Unit Price)
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

SQL (Below are some of the queries run on SQL)











