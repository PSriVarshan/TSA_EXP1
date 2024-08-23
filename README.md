### Developed By : Sri Varshan P
### Register No. 212222240104
###  Date: 

# Ex.No: 01A PLOT A TIME SERIES DATA


# AIM:
To Develop a python program to Plot a time series data for Russian Losses of equipments in War

# ALGORITHM:

1. Import the required packages like pandas and matplot

2. Read the dataset using the pandas

3. Calculate the mean for the respective column.

4. Plot the data according to need and can be altered monthly, or yearly.

5. Display the graph.

# PROGRAM:

```py
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
```
```py
data = pd.read_csv('/content/russia_losses_equipment.csv')
```
```py
data['date'] = pd.to_datetime(data['date'])
```

```py
X = np.array(data.index).reshape(-1, 1)
y = data['tank']
```

```py
plt.figure(figsize=(12, 6))
plt.plot(data['date'], data['tank'], label='Tank Losses')
plt.xlabel('Date')
plt.ylabel('Tank Losses')
plt.title('Year-wise Tank Losses Over Time')
plt.grid(True)
plt.show()
```

# OUTPUT:

![image](https://github.com/user-attachments/assets/2f082266-8294-4769-9b0e-1fe2ed67cf1e)



# RESULT:
Thus we have created the python code for plotting the time series of given data.
