# Instructions
Instructions for this task can be found in the instructions.md file

# Access to data for flows coding task

The data consists of origin-destination flows derived from Safegraph foot-traffic data and is available for download for free on the following repository https://github.com/GeoDS/COVID19USFlows#code-usage. This data was prepared for the publication of Kang, Y., Gao, S., Liang, Y. Li, M., Rao, J. and Kruse, J. Multiscale dynamic human mobility flow dataset in the U.S. during the COVID-19 epidemic. Scientific Data 7, 390 (2020). https://www.nature.com/articles/s41597-020-00734-5.

# Access to data for GPS device-level data coding task

The data consists of a series of .plt files (which can be opened in Python or R) containing GPS records of 182 users in a period of over 5 years. This data can be downloaded for free on the following site https://www.microsoft.com/en-us/download/details.aspx?id=52367. The data is referenced in the publication Zheng, Yu, Xing Xie, and Wei-Ying Ma. "GeoLife: A collaborative social networking service among user, location and trajectory." IEEE Data Eng. Bull. 33.2 (2010): 32-39.

## Trajectory file
Every single folder of this dataset stores a user’s GPS log files, which were converted to PLT format. Each PLT file contains a single trajectory and is named by its starting time. To avoid potential confusion of time zone, we use GMT in the date/time property of each point, which is different from our previous release.
PLT format:
Line 1…6 are useless in this dataset, and can be ignored. Points are described in following lines, one for each line.
Field 1: Latitude in decimal degrees.
Field 2: Longitude in decimal degrees.
Field 3: All set to 0 for this dataset.
Field 4: Altitude in feet (-777 if not valid).
Field 5: Date - number of days (with fractional part) that have passed since 12/30/1899.
Field 6: Date as a string.
Field 7: Time as a string.
Note that field 5 and field 6&7 represent the same date/time in this dataset. You may use either of them.

Example:
39.906631,116.385564,0,492,40097.5864583333,2009-10-11,14:04:30
39.906554,116.385625,0,492,40097.5865162037,2009-10-11,14:04:35

## Further documentation

The file "User Guide 1.3.pdf" found in the downloadable zip file contains further information on the data. 
