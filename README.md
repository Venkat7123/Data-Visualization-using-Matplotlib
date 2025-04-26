# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
```
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

```
x1 = [1,2,3]
y1 = [2,4,1]
plt.plot(x1,y1,color = 'yellow',label = 'line1')
x2 = [1,2,3]
y2 = [4,1,3]
plt.plot(x2,y2,color = 'blue',label = 'line2')
plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.title('Two lines on the same graph')
plt.legend()
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 213843.png>)
```
x = [1,2,3,4,5,6]
y = [2,4,1,5,2,6]
plt.plot(x,y,'r',linestyle = 'dashed', linewidth = 2.5, marker = '.', markerfacecolor = 'yellow', markersize = 18)
plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.xlim(1,8)
plt.ylim(1,8)
plt.title('Line Graph')
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 213850.png>)
```
years = range(2000,2012)
apples = [0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]
oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.89, 0.896]
plt.plot(years,apples,marker = 'o',label = 'apples')
plt.plot(years,oranges,marker = 'x',label = 'orange')
plt.xlabel('Year')
plt.ylabel('Yield(tons per hectare)')
plt.title('Crop Yields in Kanto')
plt.legend()
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 213858.png>)
```
x = np.arange(0,10)
y = np.arange(11,21);
x
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 213903.png>)
```
y
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 213907.png>)
```
plt.scatter(x,y,c='b');
plt.xlabel('X Axis')
plt.ylabel('Y Axis')
plt.title('Scatter Plot')
plt.savefig('fig.png')
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 213914.png>)
```
y = x*x;
y
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 213920.png>)
```
plt.plot(x,y,'b*',linestyle = 'dotted', markersize = 12, linewidth = 2);
plt.xlabel('X Axis')
plt.ylabel('Y Axis')
plt.title('Line Plot')
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 213927.png>)
```
plt.subplot(2,2,1)
plt.plot(x,y,'r--')
plt.subplot(2,2,2)
plt.plot(x,y,'g*--')
plt.subplot(2,2,3)
plt.plot(x,y,'bo')
plt.subplot(2,2,4)
plt.plot(x,y,'go')
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 213933.png>)
```
np.pi
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 213938.png>)
```
x = np.arange(0, 4 * np.pi, 0.1);
y = np.sin(x);
plt.plot(x,y);
plt.title("Sine Wave Form")
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 213943.png>)
```
x = [1,2,3,4,5]
y1 = [10,12,14,16,18]
y2 = [5,7,9,11,13]
y3 = [2,4,6,8,10]
plt.fill_between(x,y1,color = 'blue')
plt.fill_between(x,y2,color = 'yellow')
plt.plot(x,y1,color = 'yellow')
plt.plot(x,y2,color = 'blue')
plt.legend(['y1','y2'])
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 213951.png>)
```
plt.stackplot(x,y1,y2,y3,colors = ['red','blue','yellow'])
plt.legend(['y1','y2','y3'])
plt.title("Stacked Line Chart")
plt.xlabel('X Axis')
plt.ylabel('Y Axis')
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 213957.png>)
```
from scipy.interpolate import make_interp_spline
x = np.array([1,2,3,4,5,6,7,8,9,10])
y = np.array([2,4,5,7,8,8,9,10,11,12])
spl = make_interp_spline(x,y)
x_smooth = np.linspace(x.min(),x.max(),100)
y_smooth = spl(x_smooth)
plt.plot(x,y,'o',label = 'data')
plt.plot(x_smooth,y_smooth,label = 'spline')
plt.legend()
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 214005.png>)
```
x = [2,8,10]
y = [11,16,9]
x2 = [3,9,11]
y2 = [6,15,7]
plt.bar(x,y,label = 'Bar1',color = 'red')
plt.bar(x2,y2,label = 'Bar2',color = 'yellow')
plt.xlabel('X Axis')
plt.ylabel('Y Axis')
plt.title('Bar Chart')
plt.legend()
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 214010.png>)
```
ages=[2,5,70,40,30,45,50,45,43,40,44,60,7,13,57,18,90,77,32,21,20,40]
range = (0,100);
bins = 10
plt.hist(ages,bins,range,color = 'yellow',histtype = 'bar',rwidth = 0.8)
plt.xlabel('X Axis')
plt.ylabel('Y Axis')
plt.title('Histogram')
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 214017.png>)
```
x = [2,1,6,4,2,4,8,9,4,2,4,10,6,4,5,7,7,3,2,7,5,3,5,9,2,1]
plt.hist(x, bins, color='blue', alpha = 0.5)
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 214022.png>)
```
np.random.seed(0);
data = np.random.normal(loc = 0, scale = 1, size = 100)
data
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 214028.png>)
```
fig , ax = plt.subplots()
ax.boxplot(data)
ax.set_xlabel('Data')
ax.set_ylabel('Value')
ax.set_title('Box Plot')
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 214033.png>)
```
activities = ['Eat', 'Sleep', 'Work', 'Play']
slices = [3,9,5,8]
color = ['green','yellow','blue','red']
plt.pie(slices, labels = activities, colors = color, startangle = 90, shadow = True, explode = (0,0.1,0,0), radius = 1,  autopct = '%1.1f%%')
plt.legend()
plt.show()
```
![alt text](<Output Screenshots/Screenshot 2025-04-26 214039.png>)
# Result:
Data visualization through Matplotlib was completed and the results have been successfully verified.
