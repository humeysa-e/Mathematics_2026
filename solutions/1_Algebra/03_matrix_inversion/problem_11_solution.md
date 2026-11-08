# Exercise 11. Parameter and Invertibility

## Question

For

```math
A(t)=\begin{pmatrix} 1 & t \\ t & 1 \end{pmatrix}
```

find all $`t`$ for which the matrix is invertible, and then give a formula for $`A(t)^{-1}`$. Explain what happens to this formula at the excluded values.

> **Why this exercise:** combines a parameter, determinant, and an explicit inverse formula in one problem.

## Solution

**Rule.** For a $`2 \times 2`$ matrix

```math
M=\begin{pmatrix} a & b \\ c & d \end{pmatrix}
```

the determinant is $`\det M = ad-bc`$. The matrix is invertible exactly when $`\det M \neq 0`$, and then

```math
M^{-1}=\frac{1}{ad-bc}\begin{pmatrix} d & -b \\ -c & a \end{pmatrix}.
```

**Part 1: The determinant.** Here $`a=1`$, $`b=t`$, $`c=t`$, $`d=1`$, so

```math
\det A(t) = 1\cdot 1 - t\cdot t = 1 - t^2.
```

**Part 2: The values of $`t`$ for which the matrix is invertible.** We have $`1 - t^2 = 0`$ exactly when $`t^2 = 1`$, that is, $`t = 1`$ or $`t = -1`$. So $`A(t)`$ is invertible exactly for $`t \neq 1`$ and $`t \neq -1`$.

**Part 3: The formula for the inverse.** For $`t \neq \pm 1`$,

```math
A(t)^{-1}=\frac{1}{1-t^2}\begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix}.
```

**Part 4: The excluded