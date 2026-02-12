# Comparison of Data Processing between Pandas and PySpark on Google Colab

This report examines an [open source](https://data.montgomerycountymd.gov/Community-Recreation/Warehouse-and-Retail-Sales/v76h-r7br/about_data) dataset related to warehouse and retail sales of alcoholic beverages which consists of nine feature columns and 308K rows (Table 1). This dataset is large enough to be considered for complex querying, and ideal to demonstrate comparisons between the use of traditional and big data analytical data processing techniques and therefore was chosen to conduct a series of data analytic queries using both Pandas and PySpark. All data processing and analytics uses google Colab. The features of this dataset are summarized in Table 1 below.



## Table 1. Data dictionary

| Column Name          | Description                                              | API Field Name       | Data Type |
|----------------------|----------------------------------------------------------|----------------------|-----------|
| YEAR                 | Calendar Year                                            | calendar_year        | Number    |
| MONTH                | Month                                                    | cal_month_num        | Number    |
| SUPPLIER             | Supplier Name                                            | supplier             | Text      |
| ITEM CODE            | Item code                                                | item_code            | Text      |
| ITEM DESCRIPTION     | Item description                                         | item_description     | Text      |
| ITEM TYPE            | Item Type                                                | item_type            | Text      |
| RETAIL SALES         | Cases of product sold from DLC dispensaries              | rtl_sales            | Number    |
| RETAIL TRANSFERS     | Cases of product transferred to DLC dispensaries         | rtl_transfers        | Number    |
| WAREHOUSE SALES      | Cases of product sold to MC licensees                    | whs_sales            | Number    |

The objective was to compare processing by Pandas and Pyspark to answer crucial business questions like: 

i. Which months or years have the biggest retail sales?

ii. What are the top retail sales items? 

iii. How do sales trends differ by supplier or product type?
 
iv. How efficient are retail transfers relative to warehouse sales?

The reasoning behind this project provides practical insights for inventory management, sales strategy optimisation, and supplier evaluation. The large dataset makes it excellent for evaluating the scalability and performance of Pandas (traditional analytics) and PySpark (big data analytics).

## Data analytics methods and rationale 
Pandas is used for normal analytics with PySpark intended for big data analytics. For small to medium-sized datasets, the analysis performed by Pandas can be done easily and efficiently in data processing, filtering, and aggregation. In contrast, PySpark runs for distributed processing and enables big data processing with thriving capabilities in executing complex queries that exceed limitations of memory in traditional tools. The motivating factor for selecting these techniques would be faster query execution time and demonstrating PySpark's ability to handle datasets that would drown Pandas in performance, providing an easy comparison of their efficiencies along many scales.

## Data preprocessing and analytics with Pandas 
To avoid any errors in analytics all NaN were removed. The records removed were relatively minimal to have any effect upon the analytics. The execution time reflects how Pandas processes the data in memory, which can become a bottleneck as dataset size increases.
