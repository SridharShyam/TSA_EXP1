# Ex.No: 01A PLOT A TIME SERIES DATA
### Date: 12/08/2025
### Name: SHYAM S
### Reg.No: 212223240156

# AIM:
To develop a Python program to plot month-wise total money spent on coffee using transaction data to analyze spending trends.

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

data = pd.read_csv("/content/index_1.csv")

data.head()
data.tail()
data['date'] = pd.to_datetime(data['date'])
data.set_index('date', inplace=True)
monthly_data = data['money'].resample('M').mean()

plt.figure(figsize=(10,8))
plt.plot(monthly_data, marker='o', color='green')
plt.title("Monthly Time Series Plot")
plt.xlabel("Month")
plt.ylabel("Value")
plt.xticks(rotation=45)
plt.grid(True)
plt.show()
```

# OUTPUT:

<img width="841" height="738" alt="image" src="https://github.com/user-attachments/assets/e04b696d-4e8f-438e-8be6-c7bbc2823843" />

# RESULT:
Thus we have created the python code for plotting the time series of given data.
