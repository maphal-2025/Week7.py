import pandas as pd

# Load dataset from a CSV file
df = pd.read_csv("supermarket_sales.csv")

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

print(df.head())

print(df.info())

print(df.isnull().sum())

try:
    df = pd.read_csv("supermarket_sales.csv")
except FileNotFoundError:
    print("Error: The file was not found.")
except Exception as e:
    print(f"An error occurred: {e}")

    print(df.describe())

    import matplotlib.pyplot as plt
import seaborn as sns

# Line Chart
plt.figure(figsize=(10, 5))
sns.lineplot(x="City", y="Total", data=df)
plt.title("Total per City")

# Bar chart
plt.figure(figsize=(10, 5))
sns.barplot(x="Branch", y="Total", data=df)
plt.title("Total per Branch")

# Histogram
plt.figure(figsize=(10, 5))
sns.histplot(df["Unit price"], bins=20, kde=True)
plt.title("Unit Price")

# Scatter Plot
plt.figure(figsize=(10, 5))
sns.scatterplot(x="Product line", y="Quantity", data=df)
plt.title("Quantity of product")

Link: https://nb.anaconda.cloud/jupyterhub/user/979a46ea-0500-4687-b91b-9363a6edaa59/lab/tree/python%20session%203/Seassion3/assignment/Week7.ipynb
