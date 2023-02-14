ED Volumes Data Readme

This repository contains data for emergency department (ED) volumes for the years 2019 and 2020. The data is stored in two dataframes, ED_Volumes_2019 and 

ED_Volumes_2020.

Data Pre-processing

Before analyzing the data, certain pre-processing steps were taken to clean and prepare the data. The following steps were performed:

The Date_of_visit column was converted to datetime format in both dataframes.

In the wt dataset, there were 54 missing values in the TWIB column. The missing values were filled with the mean value of the column.

The AGE_NUM and TWIB columns were converted to int64 data type.

The numerical and categorical columns in the wt dataset were separated.

The descriptive statistics of the numerical columns were computed. It was observed that the AGE_NUM column had a maximum value of 999 and a minimum value of 0, which 
indicates the presence of outliers.

Outliers in the numerical columns were removed. The 999 value in the AGE_NUM column was removed and outliers in the TWIB column were removed using the IQR method.

A new column was created in the ED_Volumes_2020 dataframe for each common column in both dataframes, with the new column name being the original column name followed by "_difference". The values in each new column were the difference between the corresponding values in ED_Volumes_2020 and ED_Volumes_2019.

The Year column was created in the ED_Volumes_2019 dataframe by extracting the year from the Date_of_visit column.

Data Description

The dataframes contain information about ED visits, including the date of the visit, patient age, and various other features. The wt dataset contains 66,674 observations and several columns, including numerical and categorical features. The ED_Volumes_2019 and ED_Volumes_2020 dataframes contain information about ED visits for the respective years, with the ED_Volumes_2020 dataframe also containing the differences between the values in the corresponding columns of both dataframes.

This codebase and the accompanying data provide a starting point for further analysis of ED volumes over time and the potential impact of different factors on ED utilization.
