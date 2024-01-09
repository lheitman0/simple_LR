# simple_LR
## Creating a Linear Regression Model from Scratch

### General Idea
Start with the basics of ML. How does linear regression work? Understand the math behind gradient descent. Implement with a very simple dataset. Draw a line of best fit through the data points, minimizing the difference between the predicted y-values and the actual y-values.

### Dataset
Using a really simple data set to understand the core concepts better. Contains Years of Experience and Salary. Will use years of experience as y to predict Salary, X. 

### Mathematical Formulation
The general form of a linear regression model with n independent variables is:
y = β0 + β1x1 + β2x2 + … + βnxn + ε

Where:
- x1, x2, ..., xn are independent variables (features).
- β0 is the intercept, the value of y when all x values are 0.
- β1, ..., βn are the coefficients of the model, representing the change in y for a one-unit change in the corresponding x value.

### Finding Coefficients
The most commonly used method is Ordinary Least Squares (OLS). The objective is to minimize the cost function J(β), defined as:
J(β) = Σ (from i=1 to m) of (yi - y-hat(i))^2

Where:
- m is the number of data points.
- yi is the actual value.
- y-hat(i) is the predicted value from the equation.

To minimize J(β), take the partial derivative of J with respect to each coefficient βj and set it to zero.

### Matrix Notation
In matrix notation, the model is expressed as:
Y = Xβ + ε

Where:
- Y is a vector of the dependent variable.
- X is a matrix where each column is a vector of each independent variable, and the first column is all 1's to represent the intercept β0.
- β is a vector of coefficients.
- ε is a vector of errors.

The solution to the normal equations is:
β = (X^T X)^(-1) X^T Y
assuming X^T X is invertible.
