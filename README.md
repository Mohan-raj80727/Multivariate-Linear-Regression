# NAME : MOHANRAJ.S
# REG NO : 212224100036
# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Input: Load dataset with multiple features (X) and one target variable (y).
### Step2
Normalize: Standardize features by subtracting mean and dividing by standard deviation.
### Step3
Add Bias: Append a column of ones to X to represent the intercept term.
### Step4
Initialize: Set all weights (θ) to zero or small values.
### Step5
![image](https://github.com/user-attachments/assets/5f19686e-5246-412d-a492-bc0dd3b03b8d)
### step6
![image](https://github.com/user-attachments/assets/84507861-c7fe-44dc-85a3-62ebac894605)
### step7
![image](https://github.com/user-attachments/assets/7f89b77c-fb2b-4ece-9c70-d5c1419a7a93)
### step8
Repeat: Iterate gradient descent for fixed epochs until convergence.
### step9
Predict: Use learned θ to predict output for new input data.
## Program:
```PYTHON

import pandas as pd
from sklearn import linear_model
df = pd.read_csv("/content/carsemission.csv")
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

### Insert your output

![image](https://github.com/user-attachments/assets/3f83ae3e-7eb7-496c-a07b-529939f2c345)


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
