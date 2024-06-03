# Gaussian Elimination

## Introduction
Gaussian Elimination is a method used to solve systems of linear equations. It involves performing row operations to transform a matrix into Row Echelon Form (REF) or Reduced Row Echelon Form (RREF), from which the solutions can be easily determined.

## Steps in Gaussian Elimination

### Step 1: Form the Augmented Matrix
Convert the system of linear equations into an augmented matrix.

### Example:
Given the system of equations:
$`
\begin{cases}
x + y + z = 6 \\
2x + 3y + z = 10 \\
x + 2y + 2z = 8
\end{cases}
`$

The augmented matrix is:
$`
\begin{bmatrix}
1 & 1 & 1 & | & 6 \\
2 & 3 & 1 & | & 10 \\
1 & 2 & 2 & | & 8
\end{bmatrix}
`$

### Step 2: Perform Row Operations to Achieve Upper Triangular Form
Use the following row operations:
1. Swap two rows.
2. Multiply a row by a non-zero scalar.
3. Add or subtract a multiple of one row from another row.

#### Example:
1. Subtract 2 times Row 1 from Row 2:
$`
\begin{bmatrix}
1 & 1 & 1 & | & 6 \\
0 & 1 & -1 & | & -2 \\
1 & 2 & 2 & | & 8
\end{bmatrix}
`$

2. Subtract Row 1 from Row 3:
$`
\begin{bmatrix}
1 & 1 & 1 & | & 6 \\
0 & 1 & -1 & | & -2 \\
0 & 1 & 1 & | & 2
\end{bmatrix}
`$

3. Subtract Row 2 from Row 3:
$`
\begin{bmatrix}
1 & 1 & 1 & | & 6 \\
0 & 1 & -1 & | & -2 \\
0 & 0 & 2 & | & 4
\end{bmatrix}
`$

The matrix is now in Row Echelon Form (REF).

### Step 3: Back Substitution
Solve the equations starting from the last row and working upwards.

1. From Row 3: $`2z = 4 \implies z = 2`$
2. From Row 2: $`y - z = -2 \implies y - 2 = -2 \implies y = 0`$
3. From Row 1: $`x + y + z = 6 \implies x + 0 + 2 = 6 \implies x = 4`$

### Conclusion
The solutions are:
$`
x = 4, \quad y = 0, \quad z = 2
`$

## Summary
Gaussian Elimination is a systematic method for solving linear systems by transforming the augmented matrix into a form where the solutions can be easily found through back substitution. The process involves forming the augmented matrix, performing row operations to achieve upper triangular form, and solving the resulting system using back substitution.
