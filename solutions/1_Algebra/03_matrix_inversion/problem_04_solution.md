# Exercise 4. Gauss–Jordan

## Question

Find $`A^{-1}`$ using the Gauss–Jordan method for

```math
A=\begin{pmatrix} 1 & 2 \\ 3 & 5 \end{pmatrix}.
```

Show the augmented matrix $`[A\mid I]`$ after successive operations and explain why obtaining $`I`$ on the left gives the inverse on the right.

> **Why this exercise:** introduces the Gauss–Jordan method together with its meaning, not merely as a sequence of operations.

## Solution

**Method.** We write the augmented matrix $`[A\mid I]`$ and use row operations to turn the left part into $`I`$. The same operations are applied to the right part.

**Start.**

```math
\left(\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 3 & 5 & 0 & 1 \end{array}\right).
```

**Step 1.** Replace $`R_2`$ by $`R_2 - 3R_1`$ to create a zero below the first pivot. Here $`(3,5\mid 0,1) - 3\cdot(1,2\mid 1,0) = (0,-1\mid -3,1)`$:

```math
\left(\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 0 & -1 & -3 & 1 \end{array}\right).
```

**Step 2.** Multiply $`R_2`$ by $`-1`$ to make the second pivot equal to $`1`$:

```math
\left(\begin{array}{cc|cc} 1 & 2 & 1 & 0 \\ 0 & 1 & 3 & -1 \end{array}\right).
```

**Step 3.** Replace $`R_1`$ by $`R_1 - 2R_2`$ to create a zero above the second pivot. Here $`(1,2\mid 1,0) - 2\cdot(0,1\mid 3,-1) = (1,0\mid -5,2)`$:

```math
\left(\begin{array}{cc|cc} 1 & 0 & -5 & 2 \\ 0 & 1 & 3 & -1 \end{array}\right).
```

The left part is now $`I`$.

**Why the right part is the inverse.** Each row operation is the same as multiplying from the left by an invertible matrix. If $`E`$ is the product of all the matrices used, then the whole process changes $`[A\mid I]`$ into $`[EA\mid EI]=[EA\mid E]`$. We obtained $`EA=I`$ on the left, so for square matrices $`E=A^{-1}`$. The right part is $`EI=E`$, so it is exactly $`A^{-1}`$.

**Conclusion.**

```math
A^{-1}=\begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix}.
```

**Verification.** We multiply $`A`$ by the result:

```math
AA^{-1}=\begin{pmatrix} 1\cdot(-5)+2\cdot3 & 1\cdot2+2\cdot(-1) \\ 3\cdot(-5)+5\cdot3 & 3\cdot2+5\cdot(-1) \end{pmatrix}=\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}=I.
```

This also agrees with the $`2\times 2`$ formula: $`\det A = 1\cdot5-2\cdot3=-1`$, so $`A^{-1}=\frac{1}{-1}\begin{pmatrix} 5 & -2 \\ -3 & 1 \end{pmatrix}=\begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix}`$.