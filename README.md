## Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
Hardware – PCs

Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Get the independent variable X and dependent variable Y.

2.Calculate the mean of the X -values and the mean of the Y -values.

3.Find the slope m of the line of best fit using the formula.

![image](https://github.com/Apravinraj/Find-the-best-fit-line-using-Least-Squares-Method/assets/118707879/11f590a1-1e12-40fd-aa79-7c2e2cbef91d)


4. Compute the y -intercept of the line by using the formula:

![image](https://github.com/Apravinraj/Find-the-best-fit-line-using-Least-Squares-Method/assets/118707879/02b8737e-2389-4783-9908-e352f9b36f0b)


5. Use the slope m and the y -intercept to form the equation of the line. 6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
Program to implement univariate Linear Regression to fit a straight line using least squares.
Developed by: PRAVIN RAJ.A
RegisterNumber: 212222240079 
```
```
import numpy as np
import matplotlib.pyplot as plt
x =np.array(eval(input()))
y =np.array(eval(input()))

x_mean = np.mean(x)
y_mean = np.mean(y)
num,den=0,0

for i in range(len(x)):
  num +=(x[i]-x_mean)*(y[i]-y_mean)
  den += (x[i]-x_mean)**2
m=num/den
b=y_mean-m*x_mean
print(m,b)

y_predicted=m*x+b
print(y_predicted)

plt.scatter(x,y)
plt.plot(x,y_predicted,color='red')
plt.show()
```
## Output:
![image](https://github.com/Apravinraj/Find-the-best-fit-line-using-Least-Squares-Method/assets/118707879/33d6f6ac-839f-4d98-9d33-076bc5880fc2)


## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
