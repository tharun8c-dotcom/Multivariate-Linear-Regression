# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import the required libraries (pandas and LinearRegression) and load the dataset from the CSV file.

### Step2
Select the independent variables (features) and the dependent variable (target) from the dataset.

### Step3
Create and train the Linear Regression model using the training data.

### Step4
Predict the output for the given input values and display the predicted result.


## Program:
```

#Developed by: R Tharun Rathish
#RegisterNumber: 212225230284
import numpy as np
X = np.array(eval(input()))
Y = np.array(eval(input()))
X_mean = np.mean(X)
Y_mean = np.mean(Y)
num = 0
den = 0
for i in range(len(X)):
    num += (X[i] - X_mean) * (Y[i] - Y_mean)
    den += (X[i] - X_mean) ** 2
m = num / den
c = Y_mean - m * X_mean
print(m, c)
Y_pred = m * X + c
print(Y_pred)




```
## Output:

<img width="365" height="98" alt="image" src="https://github.com/user-attachments/assets/437f19dc-556f-4437-aeec-ceb50779cd6b" />


<br>

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
