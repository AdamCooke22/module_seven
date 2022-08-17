# MODULE 7 CHALLENGE : ETF ANALYZER

In this challenge our job is to build a financial database and web application by using SQL, Python, and the Voila library to analyze the performance of a hypothetical fintech ETF. In recent years, finance has had an explosion in passive investing. Passive investing means that you invest in a basket of assets that’s called an exchange-traded fund (ETF). This way, you don’t spend time researching individual stocks or companies or take the risk of investing in a single stock. ETFs offer more diversification. For this challenge we be analyzing ETF data from a SQL database and creating a professionally styled and formatted interactive visualizations.

We start this challenge by initiating our SQLite database and populating the database with records from a seed file in the startercode. We then create an engine so that we can interact with the database using the sql.create_engine functoin. After that we can use the engine.table_names function to see if our integration was successful and to see the tables that we will be working with. 

When wanting to analyze a particular table in the database we are going to need to use queries. Queries allow for us to read through the database and by using the pd.read_sq_table function, it also allows for us to create dataframes from the database. With the dataframes that we created we can provide futher analysis and we able to plot out the data to help visualize and enhance the readability of the data.

To optimize our queries we can use additional functions like WHERE, which allows for the use of conditional statements; ORDER, which allows for the use of sorting the resulting data in a particular manner; and LIMIT, which allows for the use of displaying only the top number of results.

To view data from multiple tables we can adjust our query statements to include the INNER JOIN command to join each table based on the data from a particular column.

To finish off this challenge we use the Voila librarh to deploy our notebook as a web application to view all of the outputs from our code.

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

