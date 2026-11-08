# Exercise 5. Row Operations

## Question

For

```math
A=\begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}
```

find $`\det A`$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

> **Why this exercise:** connects determinants with row operations and requires conscious tracking of every step.

## Solution

**Rule.** The effect of row operations on the determinant is:

- swapping two rows multiplies the determinant by $`-1`$;
- multiplying a row by a number $`k`$ multiplies the determinant by $`k`$;
- adding a multiple of one row to another row does not change the determinant.

Also, the determinant of a triangular matrix is the product of its diagonal entries. We will use only the third operation, so the determinant stays the same at every step.

**Step 1: Make the first column below the pivot zero (row 2).** Replace $`R_2`$ by $`R_2 - 2R_1`$. Here $`(2,1,0) - 2\cdot(1,2,3) = (0,-3,-6)`$:

```math
\begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 0 \\ -1 & 4 & 2 \end{pmatrix}
\longrightarrow
\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ -1 & 4 & 2 \end{pmatrix}.
```

We added a multiple of one row to another row, so the determinant does not change.

**Step 2: Make the first column below the pivot zero (row 3).** Replace $`R_3`$ by $`R_3 + R_1`$. Here $`(-1,4,2) + (1,2,3) = (0,6,5)`$:

```math
\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ -1 & 4 & 2 \end{pmatrix}
\longrightarrow
\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 & 5 \end{pmatrix}.
```

Again we added a multiple of one row to another row, so the determinant does not change.

**Step 3: Make the second column below the pivot zero.** Replace $`R_3`$ by $`R_3 + 2R_2`$. Here $`(0,6,5) + 2\cdot(0,-3,-6) = (0,0,-7)`$:

```math
\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 6 & 5 \end{pmatrix}
\longrightarrow
U=\begin{pmatrix} 1 & 2 & 3 \\ 0 & -3 & -6 \\ 0 & 0 & -7 \end{pmatrix}.
```

Once more the determinant does not change.

**Step 4: The determinant of the triangular matrix.** The matrix $`U`$ is upper triangular, so its determinant is the product of the diagonal entries:

```math
\det U = 1\cdot(-3)\cdot(-7) = 21.
```

**Conclusion.** No step changed the determinant, so $`\det A = \det U = 21`$. Since $`\det A \neq 0`$, the matrix $`A`$ is invertible.

**Verification.** We check the result with Sarrus' rule. The positive terms are

```math
1\cdot 1\cdot 2 = 2, \qquad 2\cdot 0\cdot(-1) = 0, \qquad 3\cdot 2\cdot 4 = 24,
```

and the negative terms are

```math
3\cdot 1\cdot(-1) = -3, \qquad 2\cdot 2\cdot 2 = 8, \qquad 1\cdot 0\cdot 4 = 0.
```

Therefore

```math
\det A = (2 + 0 + 24) - (-3 + 8 + 0) = 26 - 5 = 21.
```

This agrees with the result from row operations.