# Exploratory Data Analysis
This is a Jupyter notebook containing the code and analysis for Exploratory Data Analysis (EDA) of a dataset. The dataset includes the following variables:
Name: the name of the student
Age:age of name
Gender:gender of the student
Hours_Studied:number of hours studied
Physics_Marks: marks obtained in Physics
Chemistry_Marks:marks obtained in Chemistry
Maths_Marks: marks obtained in Mathematics
Has_Part_Time_Job: whether the student has a part-time job or not
# 1. Importing Libraries and Reading the Data
Let's start by importing the required libraries and reading the dataset into a Pandas DataFrame.

# Importing the libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Reading the data
df=pd.read_csv('student_ml_dataset.csv')

# 2. Data Cleaning and Preprocessing
Next, we'll perform any necessary data cleaning and preprocessing steps like handling missing values, removing outliers, etc.
print(df.isnull().sum())

# 3. Univariate Analysis
In this section, we'll analyze individual variables to uncover patterns, outliers, distributions, etc. We can use various techniques like summary statistics, histograms,bar graph,scatterplot, box plots, etc.

# Summary Statistics
print(df.describe())

# Histograms
df.hist(figsize = (10,10),bins=50, color='red', alpha=0.6, rwidth=0.9)
plt.title('Histogram', fontsize=15, fontweight='bold')
plt.xlabel('Values', fontsize=10, fontweight='bold')
plt.ylabel('Frequency', fontsize=10, fontweight='bold')
plt.show()

# Box Plots
sns.boxplot(data=data, x='Gender', y='Maths Marks')
plt.xlabel('Gender')
plt.ylabel('Marks')
plt.title('Maths Marks Distribution by Gender')
plt.show()

# More Univariate Analysis...
4. Bivariate Analysis
Next, we'll explore the relationships between variables by performing bivariate analysis. We can use techniques like scatter plots, correlation analysis, etc. to understand the relationships among variables.

# Scatter Plot
sns.scatterplot(data=data, x='IQ', y='Physics Marks')
plt.xlabel('IQ')
plt.ylabel('Physics Marks')
plt.title('Relationship between IQ and Physics Marks')
plt.show()

# Correlation Analysis

# More Bivariate Analysis...
5. Multivariate Analysis
Lastly, we'll explore the interactions and patterns among multiple variables using multivariate analysis techniques. We can create visualizations like scatter matrix, parallel coordinates plot, etc. to understand these complex relationships.

# Scatter Matrix
pd.plotting.scatter_matrix(df[['Physics Marks', 'Chemistry Marks', 'Maths Marks', 'IQ']],
                           figsize=(10, 10))
plt.show()
