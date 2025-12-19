PROCESS:
This project is based upon the adventureworks schema + tables. The goal of this project was to build an a data lakehouse + ETL pipeline to represent my business process. 

1.Extract
For this step, there were 3 parts. First, my dimension tables were read from csv files stored on my machine. Second, my fact tables were JSON files that were loaded into mongoDB collections. Then I was able to retrieve these collections using pandas dataframes. Finally, my dim_date table was retrieved from the mySQL database.

2.Transform
For this step, I cleaned and standardized my data by renaming and reordering columns. 

3.Load
For this step, I loaded my data into the data lakehouse using medallion layers. Then I was able to test my work through sql queries.



CODE: 
main folder- holds my notebook, spark warehouse, and data
mySQL_scripts folders- scripts used to create adventureworks in MySQL
FinalProject.ipynb- python pipeline notebook
README.md- documentation



DEPLOYMENT STRATEGY:
To deploy this project, I first ran my scripts found in the scripts folder in MySQL to setup the adventureworks schema+tables. Then I was able to export the csv files for dim_customers, dim_employees, and dim_products. Then I exported the json file of fact_sales_orders. Then in my python notebook I connected to MySQL and mongoDB. I ran mongoDB locally on my computer using docker desktop. Once I was connected I was able to run my entire notebook smoothly.