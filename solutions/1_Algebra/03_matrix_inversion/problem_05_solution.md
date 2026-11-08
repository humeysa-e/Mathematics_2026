# Exercise 5. A 3×3 Matrix

## Question

Use Gauss–Jordan elimination to find the inverse of

```math
A=\begin{pmatrix} 1 & 1 & 0 \\ 0 & 1 & 1 \\ 1 & 0 & 1 \end{pmatrix}.
```

Check the result by multiplication.

> **Why this exercise:** provides necessary practice with the full method in a situation where the $`2\times 2`$ formula no longer applies.

## Solution

**Method.** We write the augmented matrix $`[A\mid I]`$ and use row operations to turn the left part into $`I`$. The same operations are applied to the right part, which then becomes $`A^{-1}`$.

**Start.**

```math
\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 1 & 0 & 1 & 0 & 0 & 1 \end{array}\right).
```

**Step 1.** Replace $`R_3`$ by $`R_3 - R_1`$:

```math
\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & -1 & 1 & -1 & 0 & 1 \end{array}\right).
```

**Step 2.** Replace $`R_3`$ by $`R_3 + R_2`$:

```math
\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & 0 & 2 & -1 & 1 & 1 \end{array}\right).
```

**Step 3.** Multiply $`R_3`$ by $`\frac12`$:

```math
\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 1 & 0 & 1 & 0 \\ 0 & 0 & 1 & -\frac12 & \frac12 & \frac12 \end{array}\right).
```

**Step 4.** Replace $`R_2`$ by $`R_2 - R_3`$:

```math
\left(\begin{array}{ccc|ccc} 1 & 1 & 0 & 1 & 0 & 0 \\ 0 & 1 & 0 & \frac12 & \frac12 & -\frac12 \\ 0 & 0 & 1 & -\frac12 & \frac12 & \frac12 \end{array}\right).
```

**Step 5.** Replace $`R_1`$ by $`R_1 - R_2`$:

```math
\left(\begin{array}{ccc|ccc} 1 & 0 & 0 & \frac12 & -\frac12 & \frac12 \\ 0 & 1 & 0 & \frac12 & \frac12 & -\frac12 \\ 0 & 0 & 1 & -\frac12 & \frac12 & \frac12 \end{array}\right).
```

The left part is now $`I`$, so the right part is the inverse.

**Conclusion.**

```math
A^{-1}=\frac12\begin{pmatrix} 1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1 \end{pmatrix}.
```

**Verification.** We multiply $`A`$ by the matrix $`C=\begin{pmatrix} 1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1 \end{pmatrix}`$, so that $`A^{-1}=\frac12 C`$:

```math
AC=\begin{pmatrix} 1\cdot1+1\cdot1+0\cdot(-1) & 1\cdot(-1)+1\cdot1+0\cdot1 & 1\cdot1+1\cdot(-1)+0\cdot1 \\ 0\cdot1+1\cdot1+1\cdot(-1) & 0\cdot(-1)+1\cdot1+1\cdot1 & 0\cdot1+1\cdot(-1)+1\cdot1 \\ 1\cdot1+0\cdot1+1\cdot(-1) & 1\cdot(-1)+0\cdot1+1\cdot1 & 1\cdot1+0\cdot(-1)+1\cdot1 \end{pmatrix}=\begin{pmatrix} 2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2 \end{pmatrix}=2I.
```

Therefore $`A\cdot\frac12 C = I`$, so $`A^{-1}=\frac12 C`$ is correct.