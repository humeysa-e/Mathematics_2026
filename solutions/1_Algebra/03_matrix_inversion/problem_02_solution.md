# Exercise 2. Formula for a 2×2 Matrix

## Question

Find the inverse of

```math
A=\begin{pmatrix} 3 & 2 \\ 5 & 4 \end{pmatrix}
```

using the formula for a $`2\times 2`$ matrix. At the end, check the result by computing one product with $`A`$.

> **Why this exercise:** teaches the simplest explicit formula for an inverse and requires verification using the definition.

## Solution

**Rule.** For a $`2 \times 2`$ matrix

```math
M=\begin{pmatrix} a & b \\ c & d \end{pmatrix}
```

with $`\det M = ad - bc \neq 0`$, the inverse is

```math
M^{-1}=\frac{1}{ad-bc}\begin{pmatrix} d & -b \\ -c & a \end{pmatrix}.
```

If $`\det M = 0`$, the inverse does not exist.

**Part 1: The determinant.** Here $`a=3`$, $`b=2`$, $`c=5`$, $`d=4`$, so

```math
\det A = 3\cdot 4 - 2\cdot 5 = 12 - 10 = 2.
```

Since $`\det A \neq 0`$, the inverse exists.

**Part 2: The inverse.** We swap the diagonal entries, change the signs of the other two entries, and divide by the determinant:

```math
A^{-1}=\frac{1}{2}\begin{pmatrix} 4 & -2 \\ -5 & 3 \end{pmatrix}=\begin{pmatrix} 2 & -1 \\ -\frac52 & \frac32 \end{pmatrix}.
```

**Conclusion.**

```math
A^{-1}=\begin{pmatrix} 2 & -1 \\ -\frac52 & \frac32 \end{pmatrix}.
```

**Verification.** We compute the product $`AA^{-1}`$:

```math
AA^{-1}=\begin{pmatrix} 3\cdot2+2\cdot\left(-\frac52\right) & 3\cdot(-1)+2\cdot\frac32 \\ 5\cdot2+4\cdot\left(-\frac52\right) & 5\cdot(-1)+4\cdot\frac32 \end{pmatrix}=\begin{pmatrix} 6-5 & -3+3 \\ 10-10 & -5+6 \end{pmatrix}=\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}=I.
```

The product is the identity matrix, so the inverse is correct.