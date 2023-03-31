# Data-Cleaning-with-Python
The dataset is randomly generated using the Faker package in Python, similar to the 1881 census in the United Kingdom. The goal is to clean the dataset and prepare it for further analysis.

# import libraries
import pandas as pd
import seaborn as sns
import numpy as np

sns.set_theme()
import matplotlib.pyplot as plt
%matplotlib inline

# Read the data
census_data = pd.read_csv('census_data.csv')

# print out the first five rows to have an overview of the dataset
census_data.head()

# To check the number of rows and columns in the dataset
census_data.shape

#Displays the data type, and number of entries of the data
census_data.info()

# Check the total number of missing values
census_data.isna().sum()

# Check for duplicate
dupli = census_data.duplicated()
census_data[dupli]

# Drop the duplicate row
census_data = census_data.drop(7309)
