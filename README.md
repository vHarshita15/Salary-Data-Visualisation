import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
df = pd.read_csv("/content/salary.csv")
df.head()
df.isnull().sum()
df.dropna(inplace=True)
df.drop_duplicates()
df.dtypes
df.columns
df
plt.scatter(df.age, df.fnlwgt, alpha=0.5, cmap='viridis')

plt.title("Sample Scatter Plot")
plt.xlabel("Age")
plt.ylabel("fnlwgt")
plt.show()
plt.bar(df.age, df.relationship, width = 0.6)

plt.title("BarPlot")
plt.xlabel("Age")
plt.ylabel("Relation")
plt.show()
