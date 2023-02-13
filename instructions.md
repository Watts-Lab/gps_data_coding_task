
# GPS Mobility Data Analysis Take Home Task for Research Assistants

Welcome to the **GPS Mobility Data Analysis** take home task for research assistant candidates at the CSSLab. This task is intended to test your coding, data analysis, and visualization skills and will be taken into account when considering your application. We estimate that this task should take approximately three hours to complete, but you can have a whole week if needed. 

The goal of this task is to analyze and visualize visits data from **Safegraph**, which is available on an online repository and is free to use. The data has been normalized and structured in large CSV files. This project will require you to use the weekly census tract to census tract flows, corresponding to March and April of 2020 and 2021. Your results should be presented in a short report emailed to shape@seas.upenn.edu with all code and graphics used for producing them also attached (you can choose any programming language that you prefer). 

## 1. Data Ingestion and Processing 
Download data from the dataset's Github repository and process it into a format suitable for analysis. The data can be downloaded at https://github.com/GeoDS/COVID19USFlows#code-usage, which also contains all the appropriate documentation. This dataset was prepared as part of the research publication Kang, Y., Gao, S., Liang, Y. Li, M., Rao, J. and Kruse, J. Multiscale dynamic human mobility flow dataset in the U.S. during the COVID-19 epidemic (Scientific Data 7, 390 (2020). https://www.nature.com/articles/s41597-020-00734-5). You should subset this data to origins and destinations in the city of Philadelphia---this corresponds to Census Tracts starting with the string "42101". Please describe the methodology used to prepare this data and the advantages and disadvantages of using it to measure human mobility in the context of an epidemic. Provide details of how you accessed the data, cleaned it up, and prepared it for analysis. 

## 2. Descriptive Statistics
Produce descriptive statistics about the number of visits of each census tract, the top visited census tracts in Philadelphia, and whether these **change over time** in the weeks spanning March and April 2020. Discuss whether these summary statistics seem reasonable in the context of the stay-at-home mandate that took place on March 23rd 2020. 

## 3 Visualization
Plot the top visited census tracts for a few origin census tracts and answer whether it seems like users mostly visit geographies close to their home. Produce an overlay on a map of Philadelphia using geopandas or another library of your choice and explain any metrics you used to support your answers. 

## 4 Clustering & Analysis 
Use some algorithm of your preference for clustering census tracts according to their visitation patterns (for March and April 2020). Explain your clustering procedure, its advantages, and its limitations. Perform the same exercise for the year of 2021; do you obtain the same results? Are any differences due to the nature of algorithm or because mobility patterns have changed? 

## 5 Overall Reflection   
How much time did it take you to complete this task? How did you approach this task? If given more time what are additional extensions or improvements that could be made? 

## Conclusion 
We look forward to reviewing your work! Please don’t hesitate to reach out if you have any questions or need help understanding any part of this task - we are here to help!

