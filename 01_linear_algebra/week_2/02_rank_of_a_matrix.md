# Rank of a Matrix

## Definition
The rank of a matrix is the number of linearly independent rows or columns in the matrix. It is a fundamental concept in linear algebra because it provides information about the solutions to a system of linear equations represented by the matrix.

## Calculating Rank

### Row Echelon Form (REF)
To determine the rank using REF:
1. Convert the matrix to REF using row operations.
2. Count the number of nonzero rows.

### Reduced Row Echelon Form (RREF)
To determine the rank using RREF:
1. Convert the matrix to RREF using row operations.
2. Count the number of nonzero rows.

### Example
Given matrix:
$`
A = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{bmatrix}
`$

#### Convert to REF:
1. Subtract 4 times Row 1 from Row 2:
   $`
   \begin{bmatrix}
   1 & 2 & 3 \\
   0 & -3 & -6 \\
   7 & 8 & 9
   \end{bmatrix}
   `$
2. Subtract 7 times Row 1 from Row 3:
   $`
   \begin{bmatrix}
   1 & 2 & 3 \\
   0 & -3 & -6 \\
   0 & -6 & -12
   \end{bmatrix}
   `$
3. Divide Row 2 by -3:
   $`
   \begin{bmatrix}
   1 & 2 & 3 \\
   0 & 1 & 2 \\
   0 & -6 & -12
   \end{bmatrix}
   `$
4. Add 6 times Row 2 to Row 3:
   $`
   \begin{bmatrix}
   1 & 2 & 3 \\
   0 & 1 & 2 \\
   0 & 0 & 0
   \end{bmatrix}
   `$
   - Rank = 2 (Two nonzero rows)

#### Convert to RREF:
1. From the REF, subtract 2 times Row 2 from Row 1:
   $`
   \begin{bmatrix}
   1 & 0 & -1 \\
   0 & 1 & 2 \\
   0 & 0 & 0
   \end{bmatrix}
   `$
   - Rank = 2 (Two nonzero rows)

# Relation with Echelon Forms

## Row Echelon Form (REF)
- The number of nonzero rows in REF is the rank of the matrix.
- The process involves applying row operations to convert the matrix to upper triangular form.

## Reduced Row Echelon Form (RREF)
- The number of nonzero rows in RREF is also the rank of the matrix.
- Each leading entry in the RREF is 1 and is the only nonzero entry in its column.

## Importance of Rank
- **Consistency of Systems:** A system of linear equations has a solution if the rank of the augmented matrix equals the rank of the coefficient matrix.
- **Number of Solutions:**
  - If the rank equals the number of variables, there is a unique solution.
  - If the rank is less than the number of variables, there are infinitely many solutions.

### Example: Solving a System of Equations
Given the system:
$`
\begin{cases}
x + y + z = 6 \\
2x + 3y + z = 10 \\
x + 2y + 2z = 8
\end{cases}
`$
1. Convert to augmented matrix:
   $`
   \begin{bmatrix}
   1 & 1 & 1 & | & 6 \\
   2 & 3 & 1 & | & 10 \\
   1 & 2 & 2 & | & 8
   \end{bmatrix}
   `$
2. Perform row reduction to REF:
   $`
   \begin{bmatrix}
   1 & 1 & 1 & | & 6 \\
   0 & 1 & -1 & | & -2 \\
   0 & 1 & 1 & | & 2
   \end{bmatrix}
   `$
3. Further reduce to RREF:
   $`
   \begin{bmatrix}
   1 & 0 & 2 & | & 4 \\
   0 & 1 & -1 & | & -2 \\
   0 & 0 & 0 & | & 0
   \end{bmatrix}
   `$
   - Rank = 2 (Two nonzero rows)

## Conclusion
The rank of a matrix is a key concept in linear algebra that indicates the maximum number of linearly independent rows or columns. It helps determine the solutions of a system of linear equations and is closely related to the matrix's echelon forms (REF and RREF). By converting a matrix to these forms, we can easily find its rank and understand the nature of the system it represents.
