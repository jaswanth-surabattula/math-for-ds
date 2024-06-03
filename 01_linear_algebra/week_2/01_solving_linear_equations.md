# Solving a System of Linear Equations

## Introduction
A system of linear equations consists of multiple linear equations that share the same set of variables. The goal is to find values for these variables that satisfy all the equations simultaneously. These systems can be solved using various methods including substitution, elimination, and matrix methods.

## Methods for Solving Systems of Linear Equations

### Substitution Method
- **Example:**
  $`
  \begin{cases}
  x + y = 5 \\
  2x - y = 1
  \end{cases}
  `$
  - Solve the first equation for $` y `$:
    $`
    y = 5 - x
    `$
  - Substitute this into the second equation:
    $`
    2x - (5 - x) = 1 \implies 2x - 5 + x = 1 \implies 3x = 6 \implies x = 2
    `$
  - Substitute $` x = 2 `$ back into the first equation:
    $`
    2 + y = 5 \implies y = 3
    `$
  - Solution: $` (x, y) = (2, 3) `$

### Elimination Method
- **Example:**
  $`
  \begin{cases}
  2x + 3y = 6 \\
  4x - 3y = 12
  \end{cases}
  `$
  - Add the two equations to eliminate $` y `$:
    $`
    (2x + 3y) + (4x - 3y) = 6 + 12 \implies 6x = 18 \implies x = 3
    `$
  - Substitute $` x = 3 `$ into the first equation:
    $`
    2(3) + 3y = 6 \implies 6 + 3y = 6 \implies 3y = 0 \implies y = 0
    `$
  - Solution: $` (x, y) = (3, 0) `$

### Matrix Method (using row reduction)
- Represent the system as an augmented matrix:
  $`
  \begin{bmatrix}
  1 & 2 & | & 5 \\
  2 & -1 & | & 1
  \end{bmatrix}
  `$
- Use row operations to reduce the matrix to Row Echelon Form (REF) or Reduced Row Echelon Form (RREF).

# Row Echelon Form (REF)

## Definition
A matrix is in Row Echelon Form if:
- All nonzero rows are above rows of all zeros.
- The leading entry of each nonzero row (called a pivot) is to the right of the leading entry of the row above it.
- The leading entry in any nonzero row is 1.

## Example
Convert the matrix to REF:
$`
\begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{bmatrix}
`$
1. Subtract 4 times the first row from the second row:
   $`
   \begin{bmatrix}
   1 & 2 & 3 \\
   0 & -3 & -6 \\
   7 & 8 & 9
   \end{bmatrix}
   `$
2. Subtract 7 times the first row from the third row:
   $`
   \begin{bmatrix}
   1 & 2 & 3 \\
   0 & -3 & -6 \\
   0 & -6 & -12
   \end{bmatrix}
   `$
3. Divide the second row by -3:
   $`
   \begin{bmatrix}
   1 & 2 & 3 \\
   0 & 1 & 2 \\
   0 & -6 & -12
   \end{bmatrix}
   `$
4. Add 6 times the second row to the third row:
   $`
   \begin{bmatrix}
   1 & 2 & 3 \\
   0 & 1 & 2 \\
   0 & 0 & 0
   \end{bmatrix}
   `$
- The matrix is now in REF.

# Reduced Row Echelon Form (RREF)

## Definition
A matrix is in Reduced Row Echelon Form if:
- It is in row echelon form.
- The leading entry in each nonzero row is 1.
- Each leading 1 is the only nonzero entry in its column.

## Example
Convert the matrix to RREF:
Starting from the REF:
$`
\begin{bmatrix}
1 & 2 & 3 \\
0 & 1 & 2 \\
0 & 0 & 0
\end{bmatrix}
`$
1. Subtract 2 times the second row from the first row:
   $`
   \begin{bmatrix}
   1 & 0 & -1 \\
   0 & 1 & 2 \\
   0 & 0 & 0
   \end{bmatrix}
   `$
- The matrix is now in RREF.

# Matrix Row Reduction

## Process
Matrix row reduction involves using row operations to transform a matrix into REF or RREF. The three row operations are:
1. **Row Swapping:** Swapping two rows.
2. **Row Multiplication:** Multiplying a row by a nonzero scalar.
3. **Row Addition/Subtraction:** Adding or subtracting a multiple of one row to/from another row.

### Example
Given the matrix:
$`
A = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{bmatrix}
`$

1. **Row Swapping:** (If needed to position a row with a leading entry of 1)
   - Swap Row 1 and Row 3 to bring a different row to the top if necessary.

2. **Row Multiplication:** (Ensure leading entry is 1)
   - Multiply Row 1 by 1 to keep it the same (already in REF).

3. **Row Addition/Subtraction:** (Eliminate entries below the leading entry)
   - Subtract 4 times Row 1 from Row 2:
     $`
     \begin{bmatrix}
     1 & 2 & 3 \\
     0 & -3 & -6 \\
     7 & 8 & 9
     \end{bmatrix}
     `$
   - Subtract 7 times Row 1 from Row 3:
     $`
     \begin{bmatrix}
     1 & 2 & 3 \\
     0 & -3 & -6 \\
     0 & -6 & -12
     \end{bmatrix}
     `$
   - Divide Row 2 by -3:
     $`
     \begin{bmatrix}
     1 & 2 & 3 \\
     0 & 1 & 2 \\
     0 & -6 & -12
     \end{bmatrix}
     `$
   - Add 6 times Row 2 to Row 3:
     $`
     \begin{bmatrix}
     1 & 2 & 3 \\
     0 & 1 & 2 \\
     0 & 0 & 0
     \end{bmatrix}
     `$

# Row Operations Preserving Singularity

## Operations
Row operations that preserve singularity include:
1. **Row Swapping**
2. **Row Multiplication by a Nonzero Scalar**
3. **Row Addition or Subtraction**

## Example
Given matrix:
$`
A = \begin{bmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{bmatrix}
`$
- After row operations:
  $`
  \begin{bmatrix}
  1 & 2 & 3 \\
  0 & -3 & -6 \\
  0 & 0 & 0
  \end{bmatrix}
  `$
  - The determinant is zero, indicating the matrix is singular.
