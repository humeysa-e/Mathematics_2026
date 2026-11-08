# Exercise 1. From a System to a Matrix

## Question

Write the system

```math
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7.
\end{cases}
```

in the form $`Ax=b`$.
Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

> **Why this exercise:** teaches how to move between a system of equations and matrix notation.

## Solution

**Rule.** A system of linear equations can be written as $`Ax=b`$, where $`A`$ is the matrix of the coefficients of the unknowns, $`x`$ is the column vector of the unknowns, and $`b`$ is the column vector of the right-hand sides. Row $`i`$ of $`A`$ contains the coefficients of equation $`i`$, in the same order as the unknowns.

**Part 1: The coefficient matrix.** We read the coefficients of $`x`$, $`y`$, $`z`$ in each equation. In the first equation they are $`2, -1, 1`$, in the second $`1, 3, -2`$, and in the third $`3, 1, 1`$:

```math
A=\begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix}.
```

**Part 2: The vector of unknowns and the right-hand side.**

```math
x=\begin{pmatrix} x \\ y \\ z \end{pmatrix},\qquad b=\begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}.
```

**Part 3: The matrix form.**

```math
\begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix}\begin{pmatrix} x \\ y \\ z \end{pmatrix}=\begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}.
```

**Part 4: Rows and equations.** The entry of $`Ax`$ in row $`i`$ is the dot product of row $`i`$ of $`A`$ with $`x`$. This is exactly the left side of equation $`i`$, and it must be equal to entry $`i`$ of $`b`$. So row 1 of the matrix equation is $`2x-y+z=4`$, row 2 is $`x+3y-2z=1`$, and row 3 is $`3x+y+z=7`$.

**Conclusion.** The system is $`Ax=b`$ with

```math
A=\begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix},\qquad x=\begin{pmatrix} x \\ y \\ z \end{pmatrix},\qquad b=\begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}.
```

**Verification.** We multiply $`A`$ by $`x`$ and check that we get back the original equations:

```math
Ax=\begin{pmatrix} 2x-y+z \\ x+3y-2z \\ 3x+y+z \end{pmatrix}=\begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}.
```

Comparing the rows, we obtain exactly the three equations of the system.