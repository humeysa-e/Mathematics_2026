# Exercise 7. Using Properties Instead of Recomputing

## Question

Suppose that for a $`3\times 3`$ matrix, $`\det A=-4`$. Compute

```math
\det(2A),\qquad \det(A^T),\qquad \det(A^2),\qquad \det(-A).
```

Justify each answer using the appropriate property.

> **Why this exercise:** teaches how to use determinant properties instead of repeating a full calculation.

## Solution

**Rules.** For an $`n \times n`$ matrix $`A`$ and a number $`k`$:

- $`\det(kA) = k^n \det A`$, because multiplying the whole matrix by $`k`$ multiplies each of the $`n`$ rows by $`k`$, and each row multiplies the determinant by $`k`$;
- $`\det(A^T) = \det A`$;
- $`\det(AB) = \det A \cdot \det B`$ for two $`n \times n`$ matrices $`A`$ and $`B`$.

Here $`n = 3`$ and $`\det A = -4`$.

**Part 1: $`\det(2A)`$.** Using the first rule with $`k=2`$ and $`n=3`$:

```math
\det(2A) = 2^3\det A = 8\cdot(-4) = -32.
```

**Part 2: $`\det(A^T)`$.** A matrix and its transpose have the same determinant:

```math
\det(A^T) = \det A = -4.
```

**Part 3: $`\det(A^2)`$.** Since $`A^2 = A\cdot A`$, the product rule gives

```math
\det(A^2) = \det A\cdot\det A = (-4)\cdot(-4) = 16.
```

**Part 4: $`\det(-A)`$.** Here $`-A = (-1)A`$, so the first rule with $`k=-1`$ and $`n=3`$ gives

```math
\det(-A) = (-1)^3\det A = (-1)\cdot(-4) = 4.
```

**Conclusion.**

```math
\det(2A) = -32,\qquad \det(A^T) = -4,\qquad \det(A^2) = 16,\qquad \det(-A) = 4.
```

**Verification.** We check the answers on one example of a $`3\times 3`$ matrix with determinant $`-4`$, namely

```math
A=\begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & -4 \end{pmatrix}.
```

This matrix is diagonal, so $`\det A = 1\cdot 1\cdot(-4) = -4`$. Then

```math
2A=\begin{pmatrix} 2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & -8 \end{pmatrix},\qquad
A^2=\begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 16 \end{pmatrix},\qquad
-A=\begin{pmatrix} -1 & 0 & 0 \\ 0 & -1 & 0 \\ 0 & 0 & 4 \end{pmatrix}.
```

All of these are diagonal, so their determinants are the products of the diagonal entries: $`\det(2A) = 2\cdot 2\cdot(-8) = -32`$, $`\det(A^2) = 1\cdot 1\cdot 16 = 16`$, $`\det(-A) = (-1)\cdot(-1)\cdot 4 = 4`$. Also $`A^T = A`$ for this matrix, so $`\det(A^T) = -4`$. All four values agree with the results above.