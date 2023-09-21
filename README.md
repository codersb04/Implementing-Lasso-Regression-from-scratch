# Implementing-Lasso-Regression-from-scratch
## Lasso Regression
Y = wX + b</br>
Y: Dependent Variable</br>
X: Independent Variable</br>
w: Weight</br>
b: Bias</br>
    
### Gradient Descent for Lasso Regression
w = w - L*(dj/dw)</br>
b = b - L*(dj/db)</br>
L: Learning Rate</br>
dj/dw: Partial derivative of cost function with respect to weight</br>
dj/db: Partial derivative of cost function with respect to Bias</br></br>
    
dj/db = -2/m[(y_i - y_hat_i)]</br>
m: number of data points</br>
i: 1 to m </br>
y_i: actual value</br>
y_hat_i: predicted value</br></br>
    
dj/dw:</br>
if w>0:</br>
    dj/dw = -2/m[[(y_i-y_hat_i)]+ lambda]</br>
if w >= 0:</br>
    dj/dw = -2/m[[(y_i-y_hat_i)]- lambda]</br>
lambda: Penalty Term</br></br>

### Cost Function for Lasso Regression
J = 1/m[(y_i-y_hat_i)+(lambda*wj)]</br>
j: values ranges from 1 to n (n: NUmber of features)</br>

## Building the Lasso Regression
- Create a class for Lasso Regressiom
- Define all the necessary function inside the class
- Intiate the Hyperparameter(External Parameter) in __init__ function: learning rate, number of Iterations and Lambda parameter
- Create a function to fit the dataset to the model
  - Get the number of row(Number of data points) and columns(Number of features except the target) using the dataset shape
  - Intitat the model parameter "Weight" and "Bias"
  - Implement the Gradient Descent for Optimization
- Function for ypdating the Weight and Bias values i.e Gradient Descent
  - Predicting the Y value using the X
  - Intital 'dw' value (Gradient for weight)
  - Calculate the value of dj/dw for both the cases where w > 0 and w<=0
  - Calculate the value for dj/db
  - Update the w value using the learning rate and calculate dw and db values
- Function to predict the Target variable
  - Linear Equation is calculated: Y = wX + b </br></br></br>

  reference: 7.4.4. Building Lasso Regression from Scratch in Python, Siddhardhan, https://www.youtube.com/watch?v=V0yi-sBRI1A&list=PLfFghEzKVmjsNtIRwErklMAN8nJmebB0I&index=110


