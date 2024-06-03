# Solving a System of Linear Equations

## Introduction
A system of linear equations consists of multiple linear equations that share the same set of variables. The goal is to find values for these variables that satisfy all the equations simultaneously.

## Methods for Solving Systems of Linear Equations
1. **Substitution Method**
2. **Elimination Method**
3. **Matrix Method (using row reduction)**

# Row Echelon Form (REF)

## Definition
A matrix is in Row Echelon Form if:
- All nonzero rows are above rows of all zeros.
- The leading entry of each nonzero row is to the right of the leading entry of the row above it.
- The leading entry in any nonzero row is 1 (often called a pivot).

## Example
$`
\begin{bmatrix}
1 & 2 & 3 \\
0 & 1 & 4 \\
0 & 0 & 1
\end{bmatrix}
`$

# Reduced Row Echelon Form (RREF)

## Definition
A matrix is in Reduced Row Echelon Form if:
- It is in row echelon form.
- The leading entry in each nonzero row is 1.
- Each leading 1 is the only nonzero entry in its column.

## Example
$`
\begin{bmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{bmatrix}
`$

# Matrix Row Reduction

## Process
Matrix row reduction involves using row operations to transform a matrix into REF or RREF. The three row operations are:
1. **Row Swapping:** Swapping two rows.
2. **Row Multiplication:** Multiplying a row by a nonzero scalar.
3. **Row Addition:** Adding or subtracting a multiple of one row to another row.

# Row Operations Preserving Singularity

## Operations
Row operations that preserve singularity include:
1. **Row Swapping**
2. **Row Multiplication by a Nonzero Scalar**
3. **Row Addition or Subtraction**

## Example
Using these operations, we can reduce a matrix without changing its determinant.

# Calculation of Rank

## Definition
The rank of a matrix is the number of nonzero rows in its row echelon form or reduced row echelon form.

## Calculating Rank by Converting to Echelon Forms

### Step-by-Step Process
1. **Convert the Matrix to REF:**
   - Apply row operations to get zeros below each leading entry.
   - Count the nonzero rows.

2. **Convert the Matrix to RREF (optional for clearer understanding):**
   - Apply row operations to get zeros both above and below each leading entry.
   - Count the nonzero rows.

### Example
Given matrix:
$`
A = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{bmatrix}
`$

Convert to REF:
$`
\begin{bmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & 0
\end{bmatrix}
`$

Rank is 2 (two nonzero rows).

## Conclusion
Row reduction is a powerful tool for solving systems of linear equations and understanding matrix properties. By converting matrices to REF or RREF, we can easily find the rank and determine the consistency of systems.
