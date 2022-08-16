# MODULE 7 CHALLENGE : ETF ANALYZER

In this challenge our job is to build a financial database and web application by using SQL, Python, and the Voila library to analyze the performance of a hypothetical fintech ETF. In recent years, finance has had an explosion in passive investing. Passive investing means that you invest in a basket of assets that’s called an exchange-traded fund (ETF). This way, you don’t spend time researching individual stocks or companies or take the risk of investing in a single stock. ETFs offer more diversification. For this challenge we be analyzing ETF data from a SQL database and creating a professionally styled and formatted interactive visualizations.








To calculate and plot the number of housing units per year we want to use the groupby function to group the data by year. When using the group by function we also have to aggregate the results, and to do this we are going to use the mean function. To plot our resuting dataframe we want to use the .hvplot and .bar function, and make sure to specify what variables we want the axes to correlate. 

To calculate the average sale prices per square foot we create a new dataframe like before, using the groupby function along with the mean aggregation. This time we only want to deal with the sale prices and gross rent columns so we use the drop function to filter out the housing units column. To plot our resulting dataframe we use the hvplot and line function to produce a line graph that visualizes the sale prices per square foot and the gross rent over the seven year period in the dataframe.

To compare the average sale prices by neighborhood we use widgets help create an interactive plot for each neighborhood. We would use the same syntax as before except inside the parentheses for the line function we would also include a groupby function and have it grouped by neighborhoods so there will be a widget on the side to specify what neighborhood we would like to view.

To build an interactive map of the neighborhoods we are going to have to read another csv file that has the respective coordinates for each of the neighborhoods, and we are going to specify that the neighborhood column is going to be the index column. We are then going to create another dataframe just like we did in the beginning of the challenge with using the groupby function and grouping the data by neighborhoods this time as well as taking the average of the results. We do this so that the index of this dataframe will be the same as the index of the dataframe with the coordinates. We want to combine the two dataframes by using the concat function to concatenate the two dataframe and its going to add the coordinates to our main dataframe that we have been working with prior. Some of the neighborhoods do not have coordinates listed and or some neigborhoods from the coordinates dataframe do not have housing information so to get rid of the NaN values we see we use the dropna function. To actually plot the map we use the hvplot and points function while specifying that we want the map displayed based on the coordinates and set the appropriate variables for the colors and sizes. Once that is done you can hover and use the other interactive features to see the gross rent and sale price per square foot for each neighborhood on the map. 


---

## Technologies

This project leverages python 3.7 with the following packages:

* [Pandas](https://github.com/google/pandas) - Pandas is a powerfull tool for data analysis and manipulation. Pandas provides a plethora of useful functions that make it easy to express, analyze, and manipulate data.

* [Hvplot](https://github.com/google/hvplot) - This Module provides a high-level potting API that allows for users to easily generate a wide array of plot types. HvPlot's main benefit is that it allows for very interactive visualizations.


---

## Installation Guide

Before running the application first install the following dependencies.

```
import numpy as np
import pandas as pd
import hvplot.pandas
import sqlalchemy


```

---

## Usage

To use the Financial Planning Tools file simply clone the repository and open the san_francisco_housing.ipynb file in Jupyter Notebook.

Upon opening the file you will have the option to run the whole note book and that will provide you with all of the calculations, evaluations, and visualizations for the valuations of the housing data in San Francisco. 

This is where we used the groupby function to group the census data by year and created a dataframe that averages the results.![Screenshot 2022-08-10 140925](https://user-images.githubusercontent.com/107158380/184040102-54250a64-6b8b-4ca4-94d0-8b9cd3492e1d.png)

This is where we plotted the grouped data using the hvplot.bar function. ![Screenshot 2022-08-10 140957](https://user-images.githubusercontent.com/107158380/184040270-cecf83cb-abef-4c0f-a420-4d6ab8b27838.png)  Over the period between 2010 through 2016, the general trand in the number of housing units is around a 2000 increase in the number of housing units every year.

This is after we took that same dataframe and dropped the housing units column so we could take a closer look at the sale price per square foot and the gross rent. ![Screenshot 2022-08-10 141038](https://user-images.githubusercontent.com/107158380/184040470-d510294e-3c94-45c3-94b8-90481b3f23b1.png) The lowest gross rent reported for the period between 2010 through 2016 would be in the year 2010, where the average gross rent was around $1239. The highest gross rent reported for the period between 2010 through 2016 would be in the year 2016, where the average gross rent was around $4390.

This is where we plotted the dataframe using the hvplot.line function. ![Screenshot 2022-08-10 141118](https://user-images.githubusercontent.com/107158380/184040630-68f33143-3640-4425-ba08-b6d9831af8d3.png) In 2011 there was a drop in the average sale price per square foot where it was $341.90 compared to when it was \$369.84 in 2010. During this time the gross rent increased from $1,239 to $1,530.

This is where we created a new dataframe with using the groupby function to group the data by year and neighborhood, while aggregating the results by taking the average values. ![Screenshot 2022-08-10 141140](https://user-images.githubusercontent.com/107158380/184040936-06bd329c-4ffd-4729-b4d4-ac64a81e3517.png)

This is where we took that same dataframe and dropped the housing units column again using the drop function. ![Screenshot 2022-08-10 141206](https://user-images.githubusercontent.com/107158380/184041027-864c1b9d-d33d-4da5-878f-a1c06371546f.png)

This is where we plotted the dataframe and added a widget that allows the user to go interact with the visiualization and select which neighborhood they would like to see. ![Screenshot 2022-08-10 141252](https://user-images.githubusercontent.com/107158380/184041144-cdbf7ce6-1051-4f7f-b78b-408208921775.png) For the Anza Vista neighborhood, the average sale price per square foot for 2016 is $88.40, which is significantly less than it was in 2012 at $344.49

This is where we are reading in a new csv file that is required soon and creating a dataframe for it. ![Screenshot 2022-08-10 141312](https://user-images.githubusercontent.com/107158380/184041239-b7cd3ff6-1e8a-46bf-bd05-c9ae6c0f7513.png)

This is where we created a new dataframe with the original data grouped by neighborhood. ![Screenshot 2022-08-10 141336](https://user-images.githubusercontent.com/107158380/184050860-712d550a-bf8b-4777-9738-ecf6a3f48b87.png)

This is after we concantenated the two dataframes to include the housing information and the coordinates.![Screenshot 2022-08-10 141359](https://user-images.githubusercontent.com/107158380/184050935-3703e349-5d72-423a-8528-b151fc52be93.png)

This is where we used the new dataframe with the housing information and coordinates to plot this points visualization. ![Screenshot 2022-08-10 141525](https://user-images.githubusercontent.com/107158380/184051007-2944f72a-dd18-4f56-918f-0f93e2dd1e7e.png)

The neighborhood that has the highest gross rent would be Westwood Park with a gross rent of $3,959. The neighborhood that has the highest sale price per square foot would be Union Square District with a sale price per square foot of $903.99. Generally speaking, the growth in rental income significantly exceeds that of the growth in sales prices. The uptick in sales prices is so miniscule for most neighborhoods, and there are also some neighborhoods where the sales price is on the decline. The neighborhoods that I would suggest for investment inlcude Alamo Square, Anza Vista ,Financial District South, Hayes Valley, Ingleside, and Marina just to name a few. The thing that all of these neighborhoods have in common is that they all have recent declining trends in sales prices. Rent is skyrocketing across all neighborhoods regardless of their sales price. It obviously is more complicated that what we are demonstrating here, but the main idea that we are trying to prove is that their is a higher profit margin for the investments with lower costs, with similar sources of revenue.


---

## Contributors

Completed by Adam Cooke

---

## License

MIT

