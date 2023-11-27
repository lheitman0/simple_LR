# simple_LR
Creating a linear regression model from scratch

General idea: start with basics of ML. How does linear regression work, understand the math, implement one with very simple dataset

//Notes//

Idea is that the data has a linear relationship on x, y axis. Draw a line of best fit through data points, minimizing difference between predicted y and y.

General form with n independent variables --> y = β0 + β1x1 + β2x2 +…+βnxn +ϵ

-- where x1, x2,..xn are independent vars (features)

-- β0 is intercept, y when all x vals are 0

-- β1, .. βn are coefficients of model. change in y for one unit change in corresponding x val

---How do you find coefficients?---
most commonly usesd is Ordinary Least Squares (OLS)

find J(β) = sigma(m, i=1) (Y^(i)-y-hat^(i))^2

where m is the number of data points, y(i) is the actual value and y-hat^(i) is the predicted val given from the equation above

To minimize J(β) take partial derivative of J with respect to each coefficient β j and set to zero

Matrix Notation:

Y = Xβ + ϵ

Y is vector of dependent var, X is a matrix, each col is a vector of each independent varaible, first col is all 1's to represent intercept or β0

β is vector of coefficients, ϵ is vector of errors

The solution to normal equations is β = (X transposed * X)^(-1) * X transposed*Y --> assuming X^T*X is invertible

