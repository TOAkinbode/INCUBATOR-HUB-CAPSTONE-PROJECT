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
T    
