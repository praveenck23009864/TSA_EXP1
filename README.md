# Ex.No: 01A PLOT A TIME SERIES DATA
###  Date: 08.03.2025

# AIM:
To Develop a python program to Plot a time series data (population/ market price of a commodity
/temperature.
# ALGORITHM:
1. Import the required packages like pandas and matplot
2. Read the dataset using the pandas
3. Calculate the mean for the respective column.
4. Plot the data according to need and can be altered monthly, or yearly.
5. Display the graph.
# PROGRAM:
```
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load the CSV file
file_path = "income.csv"
data = pd.read_csv(file_path)

# Display basic information about the dataset
print("Dataset Info:")
print(data.info())

# Display summary statistics
print("\nSummary Statistics:")
print(data.describe())

# Countplot of income distribution
plt.figure(figsize=(8, 5))
sns.countplot(x='income', data=data, palette='viridis')
plt.title('Income Distribution')
plt.xlabel('Income Category')
plt.ylabel('Count')
plt.grid(axis='y', linestyle='--', alpha=0.7)
plt.show()

# Bar plot of average hours-per-week by education level
plt.figure(figsize=(12, 6))
edu_hours = data.groupby('education')['hours-per-week'].mean().sort_values()
edu_hours.plot(kind='bar', color='blue')
plt.title('Average Working Hours per Week by Education Level')
plt.xlabel('Education Level')
plt.ylabel('Average Hours per Week')
plt.xticks(rotation=45)
plt.grid(axis='y', linestyle='--', alpha=0.7)
plt.show()
```









# OUTPUT:

![Screenshot 2025-03-08 155625](https://github.com/user-attachments/assets/dc526f1a-4b90-413c-8b18-9fffa42d0de0)





# RESULT:
Thus we have created the python code for plotting the time series of given data.
