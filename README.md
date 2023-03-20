# PyBer_Analysis


## Overview of Project

(As captured from Data Bootcamp Module 5) 

As the data analyst for Pyber, a Python-based ridesharing app company, I am helping V (the Client) analyze an entire dataset. My first assignment will be to perform an exploratory analysis on data in some very large CSV files. To aid this process, I will create several types of visualizations to tell a compelling story about the data.

In addition, as the data analyst, I will be utilizing the Matplotlib library. Matplotlib has a rich set of features for creating and annotating charts that visualize data in a Data Series or DataFrame. I will use Matplotlib to create line charts, bar charts, scatter plots, bubble charts, pie charts, and box-and-whisker plots, and make them visually compelling and informative by adding titles, axes labels, legends, and custom colors.

By the end of this module, as assigned Data Analyst, I will complete the following :
•	Create line, bar, scatter, bubble, pie, and box-and-whisker plots using Matplotlib.

•	Add and modify features of Matplotlib charts.

•	Add error bars to line and bar charts.

•	Determine mean, median, and mode using Pandas, NumPy, and SciPy statistics.


## Purpose
(This module is built around a project that mirrors a real-world scenario that would require data analysis and visualization.) 

As the data analyst, I will write Python scripts using Pandas libraries, the Jupyter Notebook, and Matplotlib to create a variety of charts that showcase the relationship between the type of city and the number of drivers and riders, as well as the percentage of total fares, riders, and drivers by type of city. The analysis and visualizations I produce will help Pyber improve access to ridesharing services and determine affordability for underserved neighborhoods.

This new assignment consists of two technical analysis deliverables and a written report to present my results. 

As such, I will submit the following:
•	Deliverable 1: A ride-sharing summary DataFrame by city type

•	Deliverable 2: A multiple-line chart of total fares for each city type

•	Deliverable 3: A written report for the PyBer analysis (README.md)



## Results

#Deliverable 1: A ride-sharing summary DataFrame by city type
•	In Step 1, use the groupby() function to create a Series of data that has the type of city as the index, then apply the count() method to the "ride_id" column.
![image](https://user-images.githubusercontent.com/117233641/226238165-c504acfa-8e3e-44c8-b33c-9fbe344b902e.png)
 

•	In Step 2, use the groupby() function to create a Series of data that has the type of city as the index, then apply the sum() method to the "driver_count" column.
 ![image](https://user-images.githubusercontent.com/117233641/226238210-5fab4338-ca41-4b15-bfe1-efe7da520151.png)


•	In Step 3, use the groupby() function to create a Series of data that has the type of city as the index, then apply the sum() method to the "fare" column.
 ![image](https://user-images.githubusercontent.com/117233641/226238265-6ff77de7-9a8f-47c9-97fd-280e27e6fed3.png)

•	In Step 4, calculate the average fare per ride by city type by dividing the sum of all the fares by the total rides.
 ![image](https://user-images.githubusercontent.com/117233641/226238390-9de51b27-7a0e-430c-984c-ee01e1b5d35a.png)


•	In Step 5, calculate the average fare per driver by city type by dividing the sum of all the fares by the total drivers.
![image](https://user-images.githubusercontent.com/117233641/226238415-4dc2e669-b09a-40da-96ed-4221226e4f43.png)
 

•	In Step 6, create a PyBer summary DataFrame with all the data gathered from Steps 1-5, using the column names shown below:
![image](https://user-images.githubusercontent.com/117233641/226238427-cdef57f8-4a9e-4682-ba27-1f2aec83c6c4.png)

•	In Step 7, use the provided code snippet to remove the index name ("type") from the PyBer summary DataFrame.
 ![image](https://user-images.githubusercontent.com/117233641/226238464-93c211b0-b982-4098-855f-a6a107e5ab5a.png)

•	In Step 8, format the columns of the Pyber summary DataFrame to look like this:
![image](https://user-images.githubusercontent.com/117233641/226238480-449b19a4-2c67-4a3f-88a7-9af4b9e3fca8.png)

 

##Deliverable 2: A multiple-line chart of total fares for each city type (45 points)

Using my Pandas skills and two new functions, pivot() andresample(), create a multiple-line graph that shows the total fares for each week by city type.

1.	In Step 1, create a new DataFrame with multiple indices using the groupby() function on the "type" and "date" columns of the pyber_data_df DataFrame, then apply the sum() method on the "fare" column to show the total fare amount for each date.
![image](https://user-images.githubusercontent.com/117233641/226238499-7d6a47b8-4bcd-4779-90aa-2ec88d4997fd.png)

2.	In Step 2, use the provided code snippet to reset the index. This is needed to use the pivot() function in the next step (Step 3).
![image](https://user-images.githubusercontent.com/117233641/226238524-0a00c44b-f113-4f2a-bbdb-645fd129250a.png)

3.	In Step 3, use the pivot() function to convert the DataFrame from the previous step so that the index is the "date," each column is a city "type," and the values are the "fare."
![image](https://user-images.githubusercontent.com/117233641/226238532-76d4a09d-23c8-48e3-aef0-e13524ffcb16.png)

In Step 4, create a new DataFrame by using the loc method on the following date range: 2019-01-01 through 2019-04-28.
![image](https://user-images.githubusercontent.com/117233641/226238563-f2add745-d3a0-4a0f-8c37-5067a8227199.png)

In Step 5, use the provided code snippet to reset the index of the DataFrame from the previous step (Step 4) to a datetime data type. This is necessary to use the resample() method in Step 7.
![image](https://user-images.githubusercontent.com/117233641/226238583-48b8ef12-da06-401a-b0e1-4b7948ca0193.png)

In Step 6, use the provided code snippet, df.info(), to check that the "date" is a datetime data type.
![image](https://user-images.githubusercontent.com/117233641/226238618-855b7a72-b431-4751-af8b-cdf8707bbcd4.png)
 


In Step 7, create a new DataFrame by applying the resample() function to the DataFrame you modified in Step 5. Resample the data in weekly bins, then apply the sum() method to get the total fares for each week.
![image](https://user-images.githubusercontent.com/117233641/226238638-ecfeca70-d624-4637-9f47-d0bcca5c6774.png)

 

in Step 8, graph the resampled DataFrame from Step 7 using the object-oriented interface method and the df.plot() method, as well as the Matplotlib "fivethirtyeight" graph style code snippet provided in the starter code. Annotate the y-axis label and the title, then use the appropriate code to save the figure as PyBer_fare_summary.png in your "analysis" folder.
![image](https://user-images.githubusercontent.com/117233641/226238650-5b6788d1-9571-44e2-befd-98a5edf47862.png)

 

#Results
Initial Analyst indicates the following
•	Rural cities has the least amount of drivers, rides and total fares.

•	Urban cities have the most amount of drivers, rides and total fares.

•	Suburban cities are in the middle having the 2nd most drivers, rides and total fares.
 ![image](https://user-images.githubusercontent.com/117233641/226238670-74a4215f-810f-4ba7-85d8-41d43fa9660f.png)


> * The Suburban fares started ~$1,000 -not profitable-fare dropped in March and in mid-April.  
> * The Rural fares started at ~$200-fares increase and dropped till the end of April.  
> * The Urban fares start with an average of $1,800 - consistent increase to ~$2,300. 


#Summary / Recommendations

The following are recommendations to the client based on my data/ report.
•	Expanding the business in rural and suburban cities, including hiring drivers, will result in more positive outcomes.

•	The Urban cities - opportunities to expand rides.

•	The Rural cities - opportunity to expand fares Total Fare by City Type,

In addition, from the data analysis we are able to tell what kind of fares will be “optimal” based on what city type the passenger is catching a ride in.
