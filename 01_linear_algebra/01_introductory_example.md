# Linear Algebra in Machine Learning: Linear Regression Example

## Introduction
Linear Algebra plays a crucial role in Machine Learning, providing the mathematical foundation for various algorithms. One key application is in Linear Regression, a fundamental technique used for predictive modeling.

## Linear Regression Overview
Linear Regression models the relationship between a dependent variable and one or more independent variables using a linear equation. The general form of the linear regression equation is:

$`[ y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + \ldots + \beta_n x_n ]`$

Where:
- \( y \) is the dependent variable (target)
- \( x_1, x_2, \ldots, x_n \) are the independent variables (features)
- \( \beta_0 \) is the intercept
- \( \beta_1, \beta_2, \ldots, \beta_n \) are the coefficients of the independent variables

## Example: Wind Turbines and Power Output

### Problem Statement
We want to predict the power output (\( P \)) of wind turbines based on various parameters such as wind speed (\( W_s \)), air density (\( \rho \)), blade length (\( B \)), and temperature (\( T \)).

### Linear Regression Model
Our linear regression model for predicting power output can be expressed as:

\[ P = \beta_0 + \beta_1 W_s + \beta_2 \rho + \beta_3 B + \beta_4 T \]

### Data Representation in Linear Algebra
In linear algebra, we represent the model using matrices and vectors. Suppose we have \( m \) observations (data points). We can represent our data as:

- **Feature Matrix \( X \)**:
  \[
  X = \begin{bmatrix}
  1 & W_{s1} & \rho_1 & B_1 & T_1 \\
  1 & W_{s2} & \rho_2 & B_2 & T_2 \\
  \vdots & \vdots & \vdots & \vdots & \vdots \\
  1 & W_{sm} & \rho_m & B_m & T_m \\
  \end{bmatrix}
  \]

- **Target Vector \( y \)**:
  \[
  y = \begin{bmatrix}
  P_1 \\
  P_2 \\
  \vdots \\
  P_m \\
  \end{bmatrix}
  \]

- **Coefficient Vector \( \beta \)**:
  \[
  \beta = \begin{bmatrix}
  \beta_0 \\
  \beta_1 \\
  \beta_2 \\
  \beta_3 \\
  \beta_4 \\
  \end{bmatrix}
  \]

### Matrix Equation
The linear regression model can be written in matrix form as:

\[ y = X\beta \]

### Solving for Coefficients
To find the coefficients \( \beta \), we use the Normal Equation:

\[ \beta = (X^T X)^{-1} X^T y \]

### Example Calculation
Suppose we have the following data:

| Wind Speed (\( W_s \)) | Air Density (\( \rho \)) | Blade Length (\( B \)) | Temperature (\( T \)) | Power Output (\( P \)) |
|-----------------------|------------------------|----------------------|---------------------|-----------------------|
| 5                     | 1.225                  | 30                   | 15                  | 500                   |
| 6                     | 1.225                  | 30                   | 18                  | 600                   |
| 7                     | 1.225                  | 30                   | 20                  | 700                   |

The feature matrix \( X \) and target vector \( y \) are:

\[
X = \begin{bmatrix}
1 & 5 & 1.225 & 30 & 15 \\
1 & 6 & 1.225 & 30 & 18 \\
1 & 7 & 1.225 & 30 & 20 \\
\end{bmatrix}, \quad
y = \begin{bmatrix}
500 \\
600 \\
700 \\
\end{bmatrix}
\]

Using the Normal Equation, we can solve for \( \beta \):

\[ \beta = (X^T X)^{-1} X^T y \]

This will give us the coefficients \( \beta_0, \beta_1, \beta_2, \beta_3, \beta_4 \) that best fit our data.

## Conclusion
Linear Algebra provides the tools to model and solve the linear regression problem efficiently. By representing data in matrix form and using matrix operations, we can predict outcomes and gain insights from our data.

