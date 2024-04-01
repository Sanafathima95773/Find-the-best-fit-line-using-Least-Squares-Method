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
```/*
/*
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: Sana Fathima H
RegisterNumber:  212223240145
*/
import numpy as np
import matplotlib.pyplot as plt
x=np.array([2,9,5,5,3,7,1,8,6,2])
y=np.array([69,98,82,77,71,84,55,94,84,64])
xbar=np.mean(x)
ybar=np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xbar)*(y[i]-ybar)
    den+=(x[i]-xbar)**2
b0=num/den
b1=ybar-m*xbar
print(b0,b1)
ynew=b0*x+b1
print(ynew)
plt.scatter(x,y,color='Green')
plt.plot(x,ynew,color='Red')
plt.show()
print("Equation: y=b0+b1(X) \n          y= 55.05+4.7(X)")
```

## Output:
![image](https://github.com/Sanafathima95773/Find-the-best-fit-line-using-Least-Squares-Method/assets/147084627/413613b2-23c7-453f-a004-01dc1d197377)



## Result:

Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
