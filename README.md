Salary Dataset Visualization:-
This repository contains code to visualize a salary dataset using various Python libraries such as Pandas, NumPy, Seaborn, and Matplotlib.
Dataset-
The dataset used in this project is salary.csv, which contains information about individuals, including their age, final weight (fnlwgt), and relationship status.
Installation-
To run the code in this repository, you need to have Python installed along with the following libraries:
pandas
numpy
seaborn
matplotlib
You can install these libraries using pip:
 pip install pandas numpy seaborn matplotlib
    
Code Explanation:-
The following sections explain the steps taken to preprocess the data and create visualizations.

1. Importing Libraries
First, we import the necessary libraries:
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

2. Loading the Dataset
We load the dataset using Pandas:
df = pd.read_csv("/content/salary.csv")

3. Data Exploration
We take a quick look at the first few rows of the dataset and check for any missing values:
df.head()
df.isnull().sum()

4. Data Cleaning
We remove any missing values and duplicates from the dataset:
df.dropna(inplace=True)
df.drop_duplicates(inplace=True)

5. Data Types and Columns
We check the data types of each column and list all the columns:
df.dtypes
df.columns

6. Visualizations
Scatter Plot
We create a scatter plot to visualize the relationship between age and fnlwgt:
plt.scatter(df.age, df.fnlwgt, alpha=0.5, cmap='viridis')
plt.title("Sample Scatter Plot")
plt.xlabel("Age")
plt.ylabel("fnlwgt")
plt.show()
Bar Plot
We create a bar plot to visualize the relationship between age and relationship:
plt.bar(df.age, df.relationship, width=0.6)
plt.title("Bar Plot")
plt.xlabel("Age")
plt.ylabel("Relation")
plt.show()

Usage
To run the code, simply execute the Python script after placing salary.csv in the correct directory. The visualizations will be displayed as output.

Contributing
If you would like to contribute to this project, please fork the repository and create a pull request with your changes.
