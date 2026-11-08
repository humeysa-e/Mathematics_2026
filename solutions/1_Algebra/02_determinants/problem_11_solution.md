# Exercise 11. Shortening the Calculation with Row Operations

## Question

Compute

```math
\det\begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 4 \\ 1 & 4 & 6 \end{pmatrix}
```

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

> **Why this exercise:** develops planning instead of mechanically repeating the same procedure.

## Solution

**Rule.** The effect of row operations on the determinant is:

- swapping two rows multiplies the determinant by $`-1`$;
- multiplying a row by a number $`k`$ multiplies the determinant by $`k`$;
- adding a multiple of one row to another row does not change the determinant.

Also, the determinant of a triangular matrix is the product of its diagonal entries.

**Plan.** All three entries in the first column are equal to $`1`$, so the first row can be used to create zeros below it. Then the second row can be used to create the last zero. We will use only the operation of adding a multiple of one row to another row.

**Step 1: Row 2.** Replace $`R_2`$ by $`R_2 - R_1`$. Here $`(1,3,4) - (1,2,3) = (0,1,1)`$:

```math
\begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 4 \\ 1 & 4 & 6 \end{pmatrix}
\longrightarrow
\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1 & 4 & 6 \end{pmatrix}.
```

We added a multiple of one row to another row, so the determinant does not change.

**Step 2: Row 3.** Replace $`R_3`$ by $`R_3 - R_1`$. Here $`(1,4,6) - (1,2,3) = (0,2,3)`$:

```math
\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 1 & 4 & 6 \end{pmatrix}
\longrightarrow
\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 2 & 3 \end{pmatrix}.
```

Again the determinant does not change.

**Step 3: The last zero.** Replace $`R_3`$ by $`R_3 - 2R_2`$. Here $`(0,2,3) - 2\cdot(0,1,1) = (0,0,1)`$:

```math
\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 2 & 3 \end{pmatrix}
\longrightarrow
U=\begin{pmatrix} 1 & 2 & 3 \\ 0 & 1 & 1 \\ 0 & 0 & 1 \end{pmatrix}.
```

Once more the determinant does not change.

**Step 4: The determinant of the triangular matrix.** The matrix $`U`$ is upper triangular, so

```math
\det U = 1\cdot 1\cdot 1 = 1.
```

**Conclusion.** All three operations were of the type "add a multiple of one row to another row", so none of them changed the determinant. Therefore

```math
\det\begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 4 \\ 1 & 4 & 6 \end{pmatrix} = \det U = 1.
```

**Verification.** We check the result with Sarrus' rule. The positive terms are

```math
1\cdot 3\cdot 6 = 18, \qquad 2\cdot 4\cdot 1 = 8, \qquad 3\cdot 1\cdot 4 = 12,
```

and the negative terms are

```math
3\cdot 3\cdot 1 = 9, \qquad 2\cdot 1\cdot 6 = 12, \qquad 1\cdot 4\cdot 4 = 16.
```

Therefore

```math
\det = (18 + 8 + 12) - (9 + 12 + 16) = 38 - 37 = 1.
```

This agrees with the result from row operations.