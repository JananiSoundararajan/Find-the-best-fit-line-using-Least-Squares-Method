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
Developed by: JANANI.S
RegisterNumber: 212222230049  
*/
```
```Python
import numpy as np
import matplotlib.pyplot as plt
x=np.array(eval(input()))
y=np.array(eval(input()))
X_mean=np.mean(x)
Y_mean=np.mean(y)
num=0
denom=0
for i in range((len(x))):
    num+=(x[i]-X_mean)*(y[i]-Y_mean)
    denom+=(x[i]-X_mean)**2
m=num/denom
c=Y_mean-(m*(X_mean))
print('slope',m)
y_pred=m*x+c
print('predicted values',y_pred)
plt.scatter(x,y)
plt.plot(x,y_pred,color='red')
plt.show()
```

## Output:
![MLO1](https://github.com/JananiSoundararajan/Find-the-best-fit-line-using-Least-Squares-Method/assets/119477549/76b42c72-39ba-46fb-878d-0d044cabde6a)

## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
