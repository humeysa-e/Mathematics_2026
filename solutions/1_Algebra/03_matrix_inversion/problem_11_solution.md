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

**Part 4: The excluded values.** For $`t=1`$ and $`t=-1`$ the denominator $`1-t^2`$ equals $`0`$, so the formula cannot be used, and the inverse does not exist. This agrees with the structure of the matrix: for $`t=1`$ both rows are $`(1,1)`$, and for $`t=-1`$ the rows are $`(1,-1)`$ and $`(-1,1)`$, where the second row is $`-1`$ times the first. In both cases the rows are dependent, so the matrix is not invertible.

**Conclusion.** The matrix $`A(t)`$ is invertible exactly for $`t \neq \pm 1`$, and then

```math
A(t)^{-1}=\frac{1}{1-t^2}\begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix}.
```

For $`t=\pm 1`$ the determinant is $`0`$, the formula breaks down, and there is no inverse.

**Verification.** We multiply $`A(t)`$ by the matrix in the formula:

```math
\begin{pmatrix} 1 & t \\ t & 1 \end{pmatrix}\begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix}=\begin{pmatrix} 1-t^2 & -t+t \\ t-t & -t^2+1 \end{pmatrix}=(1-t^2)\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}.
```

After dividing by $`1-t^2`$ (allowed for $`t\neq\pm1`$) we get $`I`$, so the formula is correct.