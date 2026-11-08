# Exercise 10. Detecting Dependence

## Question

Without carrying out a full determinant calculation, explain why

```math
\det\begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \end{pmatrix}=0.
```

Identify a specific dependence between the rows and connect it with noninvertibility of the matrix.

> **Why this exercise:** teaches how to recognize a zero determinant from the structure of a matrix.

## Solution

**Rules.**

- Adding a multiple of one row to another row does not change the determinant.
- A matrix with a row of zeros has determinant $`0`$ (expand along that row, or note that every term of the determinant contains an entry from it).
- A square matrix is invertible exactly when its determinant is not zero.

**Part 1: The dependence between the rows.** Call the matrix $`M`$ and its rows $`R_1=(1,2,3)`$, $`R_2=(2,4,6)`$, $`R_3=(0,1,5)`$. Multiplying the first row by $`2`$ gives

```math
2R_1 = 2\cdot(1,2,3) = (2,4,6) = R_2.
```

So the second row is $`2`$ times the first row. Equivalently, $`R_2 - 2R_1 = (0,0,0)`$, which means the rows are linearly dependent.

**Part 2: Why the determinant is zero.** Replace $`R_2`$ by $`R_2 - 2R_1`$. This adds a multiple of one row to another row, so the determinant does not change:

```math
\det\begin{pmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \end{pmatrix}
=\det\begin{pmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 0 & 1 & 5 \end{pmatrix}.
```

The new matrix has a row of zeros, so its determinant is $`0`$. Therefore $`\det M = 0`$.

**Part 3: The connection with noninvertibility.** Since $`\det M = 0`$, the matrix $`M`$ is not invertible. This matches the dependence of the rows: a square matrix with linearly dependent rows cannot be invertible.

**Conclusion.** The second row is twice the first row, so the rows are dependent, $`\det M = 0`$, and the matrix $`M`$ is not invertible.

**Verification.** We check the result with Sarrus' rule. The positive terms are

```math
1\cdot 4\cdot 5 = 20, \qquad 2\cdot 6\cdot 0 = 0, \qquad 3\cdot 2\cdot 1 = 6,
```

and the negative terms are

```math
3\cdot 4\cdot 0 = 0, \qquad 2\cdot 2\cdot 5 = 20, \qquad 1\cdot 6\cdot 1 = 6.
```

Therefore

```math
\det M = (20 + 0 + 6) - (0 + 20 + 6) = 26 - 26 = 0.
```

This agrees with the result from the dependence of the rows.