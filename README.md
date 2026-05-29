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
```Python
#Developed by: R Tharun Rathish
#RegisterNumber: 212225230284
import pandas as pd
from sklearn.linear_model import LinearRegression
data = {
    'Weight': [790, 1160, 929, 865, 1140, 929, 1109, 1365],
    'Volume': [1000, 1200, 1000, 900, 1500, 1000, 1400, 1500],
    'CO2': [99, 95, 95, 90, 105, 98, 99, 104]
}
df = pd.DataFrame(data)
X = df[['Weight', 'Volume']]
y = df['CO2']
model = LinearRegression()
model.fit(X, y)
print("Coefficients:", model.coef_)
print("Intercept:", model.intercept_)
input_data = pd.DataFrame([[3300, 1300]], columns=['Weight', 'Volume'])
predictedCO2 = model.predict(input_data)
print("Predicted CO2 for the corresponding weight and volume:", predictedCO2[0])
```
## Output:

<img width="1036" height="471" alt="WhatsApp Image 2026-05-29 at 11 25 53" src="https://github.com/user-attachments/assets/f7472706-e98e-440b-8443-6cf92cb8f1f0" />
<img width="1045" height="109" alt="WhatsApp Image 2026-05-29 at 11 26 05" src="https://github.com/user-attachments/assets/18b93541-b9eb-4614-9c73-79365c6a63ff" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
