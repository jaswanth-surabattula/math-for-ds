# Systems of Equations: Lines and Planes

## Introduction
In Linear Algebra, systems of equations can be visualized as geometric objects like lines and planes. Understanding this geometric interpretation helps us see how solutions to systems of equations work in a visual and intuitive way.

## Systems of Equations as Lines

### Two Variables
When we have a system of linear equations with two variables, each equation represents a line in the 2D plane.

**Example:**
$`
\begin{cases}
x + y = 3 \\
2x - y = 1
\end{cases}
`$

- The first equation $` x + y = 3 `$ can be rewritten as $` y = -x + 3 `$.
- The second equation $` 2x - y = 1 `$ can be rewritten as $` y = 2x - 1 `$.

These equations represent two lines on the 2D plane. The solution to the system is the point where these lines intersect.

### Geometric Interpretation
- **One Solution:** If the lines intersect at a single point, there is one unique solution.
- **No Solution:** If the lines are parallel and never intersect, there is no solution.
- **Infinite Solutions:** If the lines are identical (overlap completely), there are infinitely many solutions.

## Systems of Equations as Planes

### Three Variables
When we have a system of linear equations with three variables, each equation represents a plane in 3D space.

**Example:**
$`
\begin{cases}
x + y + z = 6 \\
2x - y + 3z = 14 \\
-x + 4y - z = -2
\end{cases}
`$

These equations represent three planes in 3D space. The solution to the system is the point or points where these planes intersect.

### Geometric Interpretation
- **One Solution:** If the planes intersect at a single point, there is one unique solution.
- **No Solution:** If the planes do not all intersect at a common point, there may be no solution.
- **Infinite Solutions:** If the planes intersect along a line or overlap completely, there are infinitely many solutions.

### Example Breakdown
1. **One Solution:** The planes intersect at one point (e.g., $` x = 1, y = 2, z = 3 `$).
2. **No Solution:** The planes are parallel and do not intersect or form a triangular prism with no common intersection.
3. **Infinite Solutions:** The planes intersect along a line or all three planes are the same.

## Singular and Non-Singular Systems in Geometry

### Singular Systems
A singular system does not have a unique solution. This happens when the planes are parallel or all lie on the same plane.

**Example:**
$`
\begin{cases}
x + y + z = 6 \\
2x + 2y + 2z = 12 \\
-x - y - z = -6
\end{cases}
`$
Here, the second and third equations are just multiples of the first, so they all represent the same plane.

### Non-Singular Systems
A non-singular system has exactly one unique solution where all planes intersect at a single point.

**Example:**
$`
\begin{cases}
x + y + z = 6 \\
2x - y + 3z = 14 \\
-x + 4y - z = -2
\end{cases}
`$
Here, the planes intersect at a single unique point in 3D space.

## Conclusion
Visualizing systems of equations as lines in 2D or planes in 3D helps us understand the possible solutions. By interpreting equations geometrically, we can see whether there is a unique solution, no solution, or infinitely many solutions, making the concepts of singular and non-singular systems clearer.
