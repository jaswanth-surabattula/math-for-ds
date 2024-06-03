# Linear Dependence and Linear Independence

## Introduction
In Linear Algebra, understanding whether a set of vectors is linearly dependent or independent is crucial. These concepts help in determining the span and dimensionality of vector spaces.

## Linear Dependence

### Definition
A set of vectors is **linearly dependent** if at least one of the vectors can be written as a linear combination of the others. In other words, there exist scalars (not all zero) such that:

$` c_1 \mathbf{v_1} + c_2 \mathbf{v_2} + \ldots + c_n \mathbf{v_n} = \mathbf{0} `$

where $` \mathbf{v_1}, \mathbf{v_2}, \ldots, \mathbf{v_n} `$ are vectors and $` c_1, c_2, \ldots, c_n `$ are scalars.

### Example
Consider the vectors $` \mathbf{v_1} = \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix} `$ and $` \mathbf{v_2} = \begin{bmatrix} 2 \\ 4 \\ 6 \end{bmatrix} `$. 

We can see that $` \mathbf{v_2} = 2\mathbf{v_1} `$ which means $` \mathbf{v_2} `$ is a scalar multiple of $` \mathbf{v_1} `$. Hence, these vectors are linearly dependent.

## Linear Independence

### Definition
A set of vectors is **linearly independent** if none of the vectors can be written as a linear combination of the others. In other words, the only solution to:

$` c_1 \mathbf{v_1} + c_2 \mathbf{v_2} + \ldots + c_n \mathbf{v_n} = \mathbf{0} `$

is $` c_1 = c_2 = \ldots = c_n = 0 `$. This means no vector in the set can be expressed as a combination of the others.

### Example
Consider the vectors $` \mathbf{v_1} = \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix} `$ and $` \mathbf{v_2} = \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix} `$. 

To determine if these vectors are linearly independent, we check if the only solution to:

$` c_1 \mathbf{v_1} + c_2 \mathbf{v_2} = \mathbf{0} `$ 

is $` c_1 = 0 `$ and $` c_2 = 0 `$. Here, $` c_1 \begin{bmatrix} 1 \\ 0 \\ 0 \end{bmatrix} + c_2 \begin{bmatrix} 0 \\ 1 \\ 0 \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \\ 0 \end{bmatrix} `$ 

implies $` c_1 = 0 `$ and $` c_2 = 0 `$; therefore, these vectors are linearly independent.

## Geometric Interpretation

### Linear Dependence
In 2D, linearly dependent vectors lie on the same line. In 3D, they lie in the same plane or line.

### Linear Independence
In 2D, linearly independent vectors form different lines that intersect at the origin. In 3D, they span the entire space, not lying in the same plane.

## Conclusion
Determining linear dependence or independence helps in understanding the structure of vector spaces. Linearly independent vectors span a space fully, while dependent vectors indicate redundancy or constrained dimensions.

# Relationship Between Linear Dependence & Independence and Singular & Non-Singular Systems

## Linear Dependence and Independence

### Linear Dependence
- A set of vectors is **linearly dependent** if at least one vector can be written as a combination of others.
- Example: $` \mathbf{v_2} = 2\mathbf{v_1} `$
- In 2D, they lie on the same line; in 3D, on the same plane.

### Linear Independence
- A set of vectors is **linearly independent** if no vector can be written as a combination of others.
- Example: $` \mathbf{v_1} = \begin{bmatrix} 1 \\ 0 \end{bmatrix}, \mathbf{v_2} = \begin{bmatrix} 0 \\ 1 \end{bmatrix} `$
- They span the space they are in, fully covering 2D or 3D.

## Singular and Non-Singular Systems

### Singular Systems
- A matrix is **singular** if it does not have an inverse, typically when the determinant is zero.
- This occurs when the system has no unique solution (either no solution or infinitely many).
- Geometrically, it corresponds to linearly dependent vectors.

### Non-Singular Systems
- A matrix is **non-singular** if it has an inverse, meaning the determinant is non-zero.
- This indicates the system has a unique solution.
- Geometrically, this corresponds to linearly independent vectors.

## Relationship

### Linear Dependence and Singularity
- A matrix formed by linearly dependent vectors is singular.
- Example: $` A = \begin{bmatrix} 1 & 2 \\ 2 & 4 \end{bmatrix} `$. The rows (or columns) are multiples of each other, making $` \det(A) = 0 `$.

### Linear Independence and Non-Singularity
- A matrix formed by linearly independent vectors is non-singular.
- Example: $` A = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} `$. The rows (or columns) are independent, making $` \det(A) \neq 0 `$.

### Summary
- **Linear Dependence** implies **Singularity** (no unique solution).
- **Linear Independence** implies **Non-Singularity** (unique solution).

Understanding these relationships helps in solving systems of equations and analyzing vector spaces efficiently.
