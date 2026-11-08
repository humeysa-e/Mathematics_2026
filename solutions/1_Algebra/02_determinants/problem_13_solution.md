# Exercise 13. Determinant by Elimination

## Question

Compute the determinant

```math
A=\begin{pmatrix} 1 & 2 & 3 \\ 2 & 5 & 7 \\ 1 & 0 & 2 \end{pmatrix}
```

using elimination. Record the effect of every row operation used on the value of the determinant.

> **Why this exercise:** reinforces organizing a determinant calculation through row operations without introducing an unnecessary second procedure.

## Solution

**Rule.** The effect of row operations on the determinant is:

- swapping two rows multiplies the determinant by $`-1`$;
- multiplying a row by a number $`k`$ multiplies the determinant by $`k`$;
- adding a multiple of one row to another row does not change the determinant.

Also, the determinant of a triangular matrix is the product of its diagonal entries. We will use only the third operation.

**Step 1: Row 2.** Replace $`R_2`$ by $`R_2 - 2R_1`$. Here $`(2,5,7) - 2\cdot(1,2,3) = (0,1,1)`$:

```math
\begin{pmatrix} 1 & 2 & 3 \\ 2 & 5 & 7 \\ 1 & 0 & 2 \end{pmatrix}
\longrightarrow
\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1 & 0 & 2 \end{pmatrix}.
```

We added a multiple of one row to another row, so the determinant does not change.

**Step 2: Row 3.** Replace $`R_3`$ by $`R_3 - R_1`$. Here $`(1,0,2) - (1,2,3) = (0,-2,-1)`$:

```math
\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1 & 0 & 2 \end{pmatrix}
\longrightarrow
\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & -2 & -1 \end{pmatrix}.
```

Again the determinant does not change.

**Step 3: The last zero.** Replace $`R_3`$ by $`R_3 + 2R_2`$. Here $`(0,-2,-1) + 2\cdot(0,1,1) = (0,0,1)`$:

```math
\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & -2 & -1 \end{pmatrix}
\longrightarrow
U=\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix}.
```

Once more the determinant does not change.

**Step 4: The determinant of the triangular matrix.** The matrix $`U`$ is upper triangular, so

```math
\det U = 1\cdot 1\cdot 1 = 1.
```

**Conclusion.** All three operations were of the type "add a multiple of one row to another row", so none of them changed the determinant. Therefore $`\det A = \det U = 1`$. Since $`\det A \neq 0`$, the matrix $`A`$ is invertible.

**Verification.** We check the result with Sarrus' rule. The positive terms are

```math
1\cdot 5\cdot 2 = 10, \qquad 2\cdot 7\cdot 1 = 14, \qquad 3\cdot 2\cdot 0 = 0,
```

and the negative terms are

```math
3\cdot 5\cdot 1 = 15, \qquad 2\cdot 2\cdot 2 = 8, \qquad 1\cdot 7\cdot 0 = 0.
```

Therefore

```math
\det A = (10 + 14 + 0) - (15 + 8 + 0) = 24 - 23 = 1.
```

This agrees with the result from elimination.