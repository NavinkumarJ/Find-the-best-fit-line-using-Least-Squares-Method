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
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Navin Kumar J
RegisterNumber: 212222240071
*/
import numpy as np
import matplotlib.pyplot as plt
x=np.array(eval(input()))
y=np.array(eval(input()))
X_mean=np.mean(x)
Y_mean=np.mean(y)
num,deno=0,0
for i in range(len(x)):
  num+=((x[i]-X_mean)*(y[i]-Y_mean))
  deno+=(x[i]-X_mean)**2
m=num/deno
b=Y_mean-m*X_mean
print(m,b)
Y_prediction=m*x+b
print(Y_prediction)
plt.scatter(x,y)
plt.plot(x,Y_prediction,color='blue')
plt.show()
```

## Output:
![LROut](https://user-images.githubusercontent.com/115530758/225860495-fcd01935-1160-4bae-95b8-2276e8d90bf8.png)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
