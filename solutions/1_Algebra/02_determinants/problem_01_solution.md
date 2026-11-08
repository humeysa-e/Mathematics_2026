# Exercise 1. Determinant of a 2×2 Matrix

## Question

Compute

```math
\det\begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}, \qquad \det\begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}.
```

Which matrix is invertible? Justify your answer.

> **Why this exercise:** introduces the simplest determinant calculation and immediately connects it with invertibility.

## Solution

**Rule.** For a $`2 \times 2`$ matrix

```math
M=\begin{pmatrix} a & b \\ c & d \end{pmatrix}
```

the determinant is $`\det M = ad - bc`$. A square matrix is invertible exactly when its determinant is not zero.

**Part 1: The first matrix.** Let

```math
P=\begin{pmatrix} 3 & -2 \\ 5 & 4 \end{pmatrix}.
```

Here $`a=3`$, $`b=-2`$, $`c=5`$, $`d=4`$, so

```math
\det P = 3\cdot 4 - (-2)\cdot 5 = 12 + 10 = 22.
```

**Part 2: The second matrix.** Let

```math
Q=\begin{pmatrix} 1 & 7 \\ 2 & 14 \end{pmatrix}.
```

Here $`a=1`$, $`b=7`$, $`c=2`$, $`d=14`$, so

```math
\det Q = 1\cdot 14 - 7\cdot 2 = 14 - 14 = 0.
```

**Conclusion.** Since $`\det P = 22 \neq 0`$, the matrix $`P`$ is invertible. Since $`\det Q = 0`$, the matrix $`Q`$ is not invertible.

**Verification.** We check the result for $`Q`$ in a different way. The second row of $`Q`$ is $`(2, 14)`$, which is $`2`$ times the first row $`(1, 7)`$. So the rows are dependent, and a matrix with dependent rows cannot be invertible. This agrees with $`\det Q = 0`$.