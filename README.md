# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
Step 1:
Import the required libraries: pandas for data manipulation and linear_model from sklearn for regression.

Step 2:
Load the dataset using pd.read_csv() and store it in a DataFrame.

Step 3:
Separate the features (independent variables) and the target (dependent variable):

Assign the relevant columns to X (features). Assign the target column to y (output).

Step 4:
Create a linear regression model using linear_model.LinearRegression() and fit it to the data using regr.fit(X, y).

Step 5:
Print the regression coefficients (regr.coef_) and intercept (regr.intercept_).

Step 6:
Use the trained model to make predictions using regr.predict() with the given input values.

Step 7:
Display the predicted output.

## Program:
```
Developed by:Sriram arun S
Register no:212225040429
import pandas as pd
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)

```
## Output:
<img width="1033" height="119" alt="Screenshot 2026-03-27 210347" src="https://github.com/user-attachments/assets/8bddb11d-d9b8-4392-afe2-4ba8d5ae59e2" />

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
