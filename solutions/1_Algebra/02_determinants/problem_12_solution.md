# Exercise 12. A Parameter Revealed by a Row Operation

## Question

For

```math
A(t)=\begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & t \\ 0 & 1 & 1 \end{pmatrix}
```

find the values of $`t`$ for which the matrix is not invertible.

Before computing the determinant, perform the operation

```math
R_2\leftarrow R_2-2R_1
```

and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

> **Why this exercise:** combines a parameter, row operations, and recognition of dependence in one short argument.

## Solution

**Rule.** Adding a multiple of one row to another row does not change the determinant. A square matrix is not invertible exactly when its determinant is zero.

**Part 1: The row operation.** Replace $`R_2`$ by $`R_2 - 2R_1`$. Here

```math
(2,4,t) - 2\cdot(1,2,3) = (2-2,\ 4-4,\ t-6) = (0,0,t-6).
```

So

```math
A(t)\longrightarrow\begin{pmatrix} 1 & 2 & 3 \\ 0 & 0 & t-6 \\ 0 & 1 & 1 \end{pmatrix}.
```

We added a multiple of one row to another row, so the determinant does not change.

**Part 2: The determinant.** The first column of the new matrix is $`(1,0,0)^T`$, so we expand along it, and only the entry $`1`$ remains:

```math
\det A(t) = 1\cdot\det\begin{pmatrix} 0 & t-6 \\ 1 & 1 \end{pmatrix} = 0\cdot 1 - (t-6)\cdot 1 = 6 - t.
```

**Part 3: When the determinant is zero.** We solve $`\det A(t) = 0`$:

```math
6 - t = 0 \quad\Longleftrightarrow\quad t = 6.
```

For every $`t \neq 6`$ we have $`\det A(t) \neq 0`$, so $`A(t)`$ is invertible.

**Part 4: What happens to the rows for $`t=6`$.** For $`t=6`$ the matrix is

```math
A(6)=\begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 1 \end{pmatrix}.
```

The second row is $`(2,4,6) = 2\cdot(1,2,3)`$, so it is $`2`$ times the first row. Equivalently, after the row operation the second row becomes $`(0,0,t-6) = (0,0,0)`$, a row of zeros. The rows are linearly dependent, which is why the determinant is zero.

**Conclusion.** The matrix $`A(t)`$ is not invertible exactly for $`t = 6`$. For this value the second row is twice the first row, so the rows are dependent and $`\det A(6) = 0`$.

**Verification.** We compute $`\det A(t)`$ directly from the original matrix with Sarrus' rule. The positive terms are

```math
1\cdot 4\cdot 1 = 4, \qquad 2\cdot t\cdot 0 = 0, \qquad 3\cdot 2\cdot 1 = 6,
```

and the negative terms are

```math
3\cdot 4\cdot 0 = 0, \qquad 2\cdot 2\cdot 1 = 4, \qquad 1\cdot t\cdot 1 = t.
```

Therefore

```math
\det A(t) = (4 + 0 + 6) - (0 + 4 + t) = 6 - t,
```

which agrees with the result from the row operation.