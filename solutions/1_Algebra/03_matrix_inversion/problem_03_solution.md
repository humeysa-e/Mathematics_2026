# Exercise 3. When Does the Inverse Not Exist?

## Question

For

```math
A=\begin{pmatrix} 2 & 4 \\ 1 & 2 \end{pmatrix}
```

explain in two ways why $`A^{-1}`$ does not exist: using the determinant and using dependence between the rows.

> **Why this exercise:** connects two signs of noninvertibility instead of treating them as unrelated facts.

## Solution

**Rule.** A square matrix is invertible exactly when its determinant is not zero. Equivalently, a square matrix with linearly dependent rows is not invertible.

**Way 1: The determinant.** For a $`2\times 2`$ matrix the determinant is $`ad-bc`$. Here

```math
\det A = 2\cdot 2 - 4\cdot 1 = 4 - 4 = 0.
```

If $`A^{-1}`$ existed, then $`AA^{-1}=I`$ would give $`\det A\cdot\det(A^{-1}) = \det I = 1`$. This is impossible when $`\det A = 0`$, because $`0\cdot\det(A^{-1}) = 0 \neq 1`$. So $`A^{-1}`$ does not exist.

**Way 2: Dependence between the rows.** The rows of $`A`$ are $`R_1=(2,4)`$ and $`R_2=(1,2)`$. We see that

```math
R_1 = 2\cdot R_2,
```

so the first row is $`2`$ times the second row. Equivalently, $`R_1 - 2R_2 = (0,0)`$. The rows are linearly dependent, so the matrix cannot be invertible.

**Conclusion.** Both arguments lead to the same result: $`\det A = 0`$ and the rows of $`A`$ are dependent, so $`A^{-1}`$ does not exist. The two facts are connected: dependent rows make the determinant zero, and a zero determinant means the matrix is not invertible.

**Verification.** We check directly that no inverse can exist. Suppose $`AX=I`$ for some matrix $`X`$ whose first column is $`(x,y)^T`$. The first column of $`AX`$ must be the first column of $`I`$, that is $`(1,0)^T`$:

```math
\begin{aligned} 2x + 4y &= 1,\\ x + 2y &= 0. \end{aligned}
```

The second equation gives $`x + 2y = 0`$, so $`2x+4y = 0`$, which contradicts the first equation $`2x+4y=1`$. So there is no such $`X`$.