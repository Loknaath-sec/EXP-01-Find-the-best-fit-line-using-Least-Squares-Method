# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
#Program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by: LOKNAATH P
#RegisterNumber: 212223240080


import numpy as np
import matplotlib.pyplot as plt

# Preprocessing Input data

x=np.array(eval(input("Enter the list of x:")))
y=np.array(eval(input("Enter the list of y:")))

# Mean

xmean=np.mean(x)
ymean=np.mean(y)
num=0 # for slope
den=0 # for slope

# To Find sum of (xi-x') & (yi-y') (xi-x')^2

for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
    
# Calculate slope
m=num/den

# y-intercept
c=ymean-m*xmean


# Calculate intercept
b=ymean-m*xmean

# Line equation
ypred=m*x+b
print(ypred)

print("Numerator : ",num)
print("Denominator : ",den)
print("Slope / m : ",m)
print("Y-Intercept : ",c)
print("Y-Precict : ",ypred)

# To plot graph
plt.scatter(x,y,color="Red")
plt.plot(x,ypred,color="Blue")
plt.show()

```

## Output:
![image](https://github.com/user-attachments/assets/e24c90c8-35c4-4fbc-ac64-ee8523d25a0c)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
