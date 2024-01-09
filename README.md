# simple_LR
## Creating a Linear Regression Model from Scratch

### General Idea
Start with the basics of Machine Learning (ML). How does linear regression work, understand the math, and implement one with a very simple dataset.

### Concept
The data has a linear relationship on the x and y axes. Draw a line of best fit through the data points, minimizing the difference between the predicted y-values and the actual y-values.

### Mathematical Formulation
The general form of a linear regression model with \( n \) independent variables is:
\[ y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \cdots + \beta_n x_n + \epsilon \]

Where:
- \( x_1, x_2, \ldots, x_n \) are independent variables (features).
- \( \beta_0 \) is the intercept, the value of y when all x values are 0.
- \( \beta_1, \ldots, \beta_n \) are the coefficients of the model, representing the change in y for a one-unit change in the corresponding x value.

### Finding Coefficients
The most commonly used method is Ordinary Least Squares (OLS). The objective is to minimize the cost function \( J(\beta) \), defined as:
\[ J(\beta) = \sum_{i=1}^{m} (y^{(i)} - \hat{y}^{(i)})^2 \]

Where:
- \( m \) is the number of data points.
- \( y^{(i)} \) is the actual value.
- \( \hat{y}^{(i)} \) is the predicted value from the equation.

To minimize \( J(\beta) \), take the partial derivative of \( J \) with respect to each coefficient \( \beta_j \) and set it to zero.

### Matrix Notation
In matrix notation, the model is expressed as:
\[ Y = X\beta + \epsilon \]

Where:
- \( Y \) is a vector of the dependent variable.
- \( X \) is a matrix where each column is a vector of each independent variable, and the first column is all 1's to represent the intercept \( \beta_0 \).
- \( \beta \) is a vector of coefficients.
- \( \epsilon \) is a vector of errors.

The solution to the normal equations is:
\[ \beta = (X^T X)^{-1} X^T Y \]
assuming \( X^T X \) is invertible.
