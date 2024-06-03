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

# Determining Infinite Solutions or No Solutions with One Zero Row

## Introduction
When using Gaussian Elimination, the presence of a zero row in the augmented matrix can indicate different scenarios for the solutions of the system. Here’s how to determine if the system has infinite solutions or no solutions.

## Augmented Matrix

### Example:
Consider the system of equations:
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

## Performing Gaussian Elimination

1. **Row Operations to Achieve REF:**
   - Subtract 2 times Row 1 from Row 2:
   $`
   \begin{bmatrix}
   1 & 1 & 1 & | & 6 \\
   0 & 1 & -1 & | & -2 \\
   1 & 2 & 2 & | & 8
   \end{bmatrix}
   `$

   - Subtract Row 1 from Row 3:
   $`
   \begin{bmatrix}
   1 & 1 & 1 & | & 6 \\
   0 & 1 & -1 & | & -2 \\
   0 & 1 & 1 & | & 2
   \end{bmatrix}
   `$

   - Subtract Row 2 from Row 3:
   $`
   \begin{bmatrix}
   1 & 1 & 1 & | & 6 \\
   0 & 1 & -1 & | & -2 \\
   0 & 0 & 2 & | & 4
   \end{bmatrix}
   `$

The matrix is now in Row Echelon Form (REF).

## Analyzing the Zero Row

### Zero Row in Augmented Matrix:
A zero row in the augmented matrix appears as:
$`
[0 \quad 0 \quad 0 \quad | \quad 0]
`$

### No Solution (Inconsistent System):
- If a row in the augmented matrix has the form:
  $`
  [0 \quad 0 \quad 0 \quad | \quad c]
  `$
  where $` c \neq 0 `$ (a row of zeros except for the last entry), the system is inconsistent and has no solution.

### Infinite Solutions:
- If a row in the augmented matrix has the form:
  $`
  [0 \quad 0 \quad 0 \quad | \quad 0]
  `$
  and there are fewer non-zero rows than the number of variables, the system has infinite solutions. This occurs when there are free variables.

## Example Analysis:

### No Solution:
If the augmented matrix were:
$`
\begin{bmatrix}
1 & 1 & 1 & | & 6 \\
0 & 1 & -1 & | & -2 \\
0 & 0 & 0 & | & 1
\end{bmatrix}
`$

The row $` [0 \quad 0 \quad 0 \quad | \quad 1] `$ indicates the system is inconsistent and has no solution.

### Infinite Solutions:
If the augmented matrix were:
$`
\begin{bmatrix}
1 & 1 & 1 & | & 6 \\
0 & 1 & -1 & | & -2 \\
0 & 0 & 0 & | & 0
\end{bmatrix}
`$

The row $` [0 \quad 0 \quad 0 \quad | \quad 0] `$ indicates that there are fewer non-zero rows than the number of variables, leading to infinite solutions.

## Conclusion
By analyzing the zero row in the augmented matrix, we can determine if a system of equations has no solution (inconsistent) or infinite solutions. A row of zeros with a non-zero constant indicates no solution, while a row of zeros with a zero constant, along with fewer non-zero rows than variables, indicates infinite solutions.
