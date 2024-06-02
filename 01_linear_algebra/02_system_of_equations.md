# Systems of Equations

## Introduction
In Linear Algebra, a system of equations is a set of equations with the same variables. These systems help us find values for the variables that satisfy all the equations simultaneously.

## Types of Systems

### Complete Systems
A complete system is one where there are exactly as many independent equations as there are variables. This usually means we can find a unique solution.

**Example:**
$`
\begin{cases}
x + 2y = 3 \\
2x - y = 1
\end{cases}
`$
Here, we have two equations and two variables. We can solve this system to find unique values for $` x `$ and $` y `$.

### Redundant Systems
A redundant system has more equations than necessary because some equations are combinations of others. This doesn't change the solutions but can make the system appear more complex.

**Example:**
$`
\begin{cases}
x + 2y = 3 \\
2x - y = 1 \\
3x + y = 4
\end{cases}
`$
The third equation is just the sum of the first two equations, making it redundant.

### Contradictory Systems
A contradictory system is one where the equations contradict each other, meaning there is no solution that satisfies all the equations.

**Example:**
$`
\begin{cases}
x + y = 3 \\
x + y = 5
\end{cases}
`$
Here, the same combination of $` x `$ and $` y `$ cannot equal both 3 and 5, so there is no solution.

## Singular and Non-Singular Systems

### Singular Systems
A singular system (also called degenerate) is one where the matrix of coefficients does not have an inverse. This usually happens when the determinant of the matrix is zero, and it often means there are either no solutions or infinitely many solutions.

**Example:**
$`
\begin{cases}
x + y = 2 \\
2x + 2y = 4
\end{cases}
`$
The second equation is just twice the first, so they are not independent. The system has infinitely many solutions.

### Non-Singular Systems
A non-singular system is one where the matrix of coefficients has an inverse (the determinant is not zero). This usually means there is exactly one unique solution.

**Example:**
$`
\begin{cases}
x + y = 3 \\
2x - y = 1
\end{cases}
`$
The matrix of coefficients is:
$`
A = \begin{bmatrix}
1 & 1 \\
2 & -1
\end{bmatrix}
`$
Since the determinant of $` A `$ is not zero, the system is non-singular and has a unique solution.

## Conclusion
Understanding the different types of systems of equations is crucial in Linear Algebra. Complete systems have unique solutions, redundant systems have unnecessary equations, and contradictory systems have no solutions. Singular systems may have no or infinite solutions, while non-singular systems have exactly one solution.
