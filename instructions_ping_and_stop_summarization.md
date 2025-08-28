
# GPS Mobility Data Analysis Take Home Task for Research Assistants

Welcome to the **GPS Mobility Data Analysis** take home task for research assistant candidates at the CSSLab. This task is intended to test your coding, data analysis, and visualization skills and will be taken into account when considering your application. This task is intended to take under four hours to complete, but it can take you less time if you are succinct (which might be preferred). 

The goal of this task is to summarize and visualize the mobility patterns of individuals from the **Garden City** dataset, which is available in this repository, consisting of raw GPS pings (latitude, longitude, timestamp). The data is partitioned by date in `parquet` format. This project will require you to load, parse and analyze this type of data to answer the question: **how broad is the movement of the individuals in this panel?** Your results should be presented in a *short report* emailed to fbarrer@sas.upenn.edu (subject: coding task) with your code and graphics. A jupyter or colab notebook could be a good way to present these results, but feel free to present them in any way you see fit.

## 1. Data Ingestion and Processing

Download the raw data from the Github repository (or clone it) and read it with methods from either `pandas` or `pyarrow` to import parquet files. Optionally, you can try using methods from [nomad](https://github.com/Watts-Lab/nomad), after installing it via `pip install git+https://github.com/Watts-Lab/nomad.git`. The columns in this data can be described as:

| Default Name | Column Name      | Description                                |
|--------------|------------------|--------------------------------------------|
| user_id      | identifier       | Unique identifier for the user             |
| timestamp    | unix_timestamp   | Event time recorded as a Unix timestamp    |
| latitude     | device_lat       | Latitude from the device’s location        |
| longitude    | device_lon       | Longitude from the device’s location       |
| datetime     | local_datetime   | Local date and time of the event           |
| date         | date             | Calendar date in YYYY-MM-DD format         |


## 2. Temporal gaps and bursts of pings
Use the time column in the data to summarize:
1. The number of GPS pings per user
2. The average and maximum temporal gaps per user
3. The number of active users each hour

**Report on the summary statistics (numbers or tables) obtained.**


## 3. Breadth of movement

Pick a single day of data. Forgetting about the time column (for now), can you summarize the (daily) location of each user with a point? What about the deviations from that point? **Show a plot of the spatial representation of user movements (on a map) and a plot of the distribution of these statistics.**

## 4. Stop detection

An initial step to process pings is to group pings that are close in space and time into clusters called "stops". Stop-detection algorithms are variations of commonly used clustering algorithms in ML, augmented to deal with the temporal dimension gracefully. Detect stops in the provided dataset using an algorithm from the `stop_detection` module in the `nomad` library (see installations above), or, alternatively, using [scikit-mobility](https://github.com/scikit-mobility/scikit-mobility). It might be easiest to follow [this tutorial](https://github.com/Watts-Lab/nomad/blob/main/tutorials/IC2S2-2025/%5B3%5Dstop-detection.ipynb) on stop detection. **Produce some plots summarizing your results or, alternatively, visualizing the clustered trajectory of a single user.** 

## 5. Breadth of movement revisited 
For brevity, we will use a pre-computed stop table available in this repository under data/gc_data_stops/ . Read this data and try to answer the same question as in part *3.* , this time for the whole period. How can you incorporate the fact that the temporal variables now determine a time range rather than a point? Try to summarize the movement of each user with a point and a radius (often called "radius of gyration"), and then with a point and radius at a daily aggregation frequency (instead of the whole period). **Which method do you think would be more useful as a summary statistic? using raw pings or stops?**

