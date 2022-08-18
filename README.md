# MODULE 7 CHALLENGE : ETF ANALYZER

In this challenge our job is to build a financial database and web application by using SQL, Python, and the Voila library to analyze the performance of a hypothetical fintech ETF. In recent years, finance has had an explosion in passive investing. Passive investing means that you invest in a basket of assets that’s called an exchange-traded fund (ETF). This way, you don’t spend time researching individual stocks or companies or take the risk of investing in a single stock. ETFs offer more diversification. For this challenge we be analyzing ETF data from a SQL database and creating a professionally styled and formatted interactive visualizations.

We start this challenge by initiating our SQLite database and populating the database with records from a seed file in the startercode. We then create an engine so that we can interact with the database using the sql.create_engine functoin. After that we can use the engine.table_names function to see if our integration was successful and to see the tables that we will be working with. 

When wanting to analyze a particular table in the database we are going to need to use queries. Queries allow for us to read through the database and by using the pd.read_sq_table function, it also allows for us to create dataframes from the database. With the dataframes that we created we can provide futher analysis and we able to plot out the data to help visualize and enhance the readability of the data.

To optimize our queries we can use additional functions like WHERE, which allows for the use of conditional statements; ORDER, which allows for the use of sorting the resulting data in a particular manner; and LIMIT, which allows for the use of displaying only the top number of results.

To view data from multiple tables we can adjust our query statements to include the INNER JOIN command to join each table based on the data from a particular column.

To finish off this challenge we use the Voila library to deploy our notebook as a web application to view all of the outputs from our code.

---

## Technologies

This project leverages python 3.7 with the following packages:

* [Pandas](https://github.com/google/pandas) - Pandas is a powerfull tool for data analysis and manipulation. Pandas provides a plethora of useful functions that make it easy to express, analyze, and manipulate data.

* [Hvplot](https://github.com/google/hvplot) - This Module provides a high-level potting API that allows for users to easily generate a wide array of plot types. HvPlot's main benefit is that it allows for very interactive visualizations.

* [Numpy](https://github.com/google/numpy) - This module offers comprehensive mathematical functions, used for working with arrays. Numpy allows for seamlessand speedy integration with a wide variety of databases.

* [Sqlalchemy](https://github.com/google/sqlalchemy) - This module is a python toolkit and object relational mapper that gives developers the full power and flexibility of sql. It provides a full suite of well known enterprise-level persistence patterns, designed for efficient and high-performing database access, adapted into a simple and Pythonic domain language.

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

To use the Financial Planning Tools file simply clone the repository and open the etf_analyzer.ipynb file in Jupyter Notebook.

Upon opening the file you will have the option to run the whole note book and that will provide you with all of the calculations, evaluations, and visualizations for the analysis of the etf data in SQL. With the implementation of the Voila library you will have access to all of the outputs of the code as a web application. Some screenshots of that in action can be seen below.

![Screenshot 2022-08-14 133346](https://user-images.githubusercontent.com/107158380/185275862-40a458b4-6851-4047-8e22-1384b973ce6a.png)
![Screenshot 2022-08-14 133456](https://user-images.githubusercontent.com/107158380/185275884-8b454c17-4b93-4ad6-a47f-7cb50076fdcf.png)
![Screenshot 2022-08-14 133517](https://user-images.githubusercontent.com/107158380/185275911-a89af7bd-b17c-487e-abda-8e6142566e4f.png)
![Screenshot 2022-08-14 134011](https://user-images.githubusercontent.com/107158380/185276191-87bdd9fc-dd25-49df-b79e-56b777489aa1.png)
![Screenshot 2022-08-14 134030](https://user-images.githubusercontent.com/107158380/185276199-929b92c4-4aad-4803-b883-f17ed47136f9.png)
![Screenshot 2022-08-14 133637](https://user-images.githubusercontent.com/107158380/185275938-81ba9a66-f85e-4c33-ba39-808d94dd7c6d.png)
![Screenshot 2022-08-14 133718](https://user-images.githubusercontent.com/107158380/185276053-846b7d6b-877c-4cc0-986b-65f2bc882f73.png)
![Screenshot 2022-08-14 133740](https://user-images.githubusercontent.com/107158380/185276185-9b7295fe-64ac-481a-bb5b-2284c6206d2f.png)

---

## Contributors

Completed by Adam Cooke

---

## License

MIT

