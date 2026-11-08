# Exercise 6. Solving a System Using the Inverse

## Question

Solve

```math
Ax=b,
```

where

```math
A=\begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix},\qquad b=\begin{pmatrix} 5 \\ 7 \end{pmatrix},
```

using $`x=A^{-1}b`$. Then substitute the resulting vector back into the equation and check the result.

> **Why this exercise:** shows the connection between inverse matrices and solving a linear system.

## Solution

**Rule.** If $`A`$ is invertible, then multiplying $`Ax=b`$ from the left by $`A^{-1}`$ gives $`A^{-1}Ax = A^{-1}b`$, that is, $`x = A^{-1}b`$. For a $`2 \times 2`$ matrix

```math
M=\begin{pmatrix} a & b \\ c & d \end{pmatrix}
```

with $`\det M = ad-bc \neq 0`$, the inverse is

```math
M^{-1}=\frac{1}{ad-bc}\begin{pmatrix} d & -b \\ -c & a \end{pmatrix}.
```

**Part 1: The inverse of $`A`$.** Here $`\det A = 2\cdot 3 - 1\cdot 1 = 5 \neq 0`$, so $`A`$ is invertible and

```math
A^{-1}=\frac{1}{5}\begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}.
```

**Part 2: The solution.**

```math
x=A^{-1}b=\frac15\begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}\begin{pmatrix} 5 \\ 7 \end{pmatrix}=\frac15\begin{pmatrix} 3\cdot5-1\cdot7 \\ -1\cdot5+2\cdot7 \end{pmatrix}=\frac15\begin{pmatrix} 8 \\ 9 \end{pmatrix}=\begin{pmatrix} \frac85 \\ \frac95 \end{pmatrix}.
```

**Conclusion.**

```math
x=\begin{pmatrix} \frac85 \\ \frac95 \end{pmatrix}.
```

**Verification.** We substitute $`x`$ back into $`Ax`$:

```math
Ax=\begin{pmatrix} 2\cdot\frac85+1\cdot\frac95 \\ 1\cdot\frac85+3\cdot\frac95 \end{pmatrix}=\begin{pmatrix} \frac{16}{5}+\frac95 \\ \frac85+\frac{27}{5} \end{pmatrix}=\begin{pmatrix} \frac{25}{5} \\ \frac{35}{5} \end{pmatrix}=\begin{pmatrix} 5 \\ 7 \end{pmatrix}=b.
```

The equation holds, so the solution is correct.