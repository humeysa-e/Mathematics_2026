# Exercise 10. Inverse of a Diagonal Matrix

## Question

Given

```math
D=\begin{pmatrix} 2 & 0 & 0 \\ 0 & -3 & 0 \\ 0 & 0 & 5 \end{pmatrix},\qquad E=\begin{pmatrix} 2 & 0 & 0 \\ 0 & 0 & 0 \\ 0 & 0 & 5 \end{pmatrix}.
```

Without using Gauss–Jordan elimination, decide which matrix is invertible. For the invertible matrix, give the inverse and check the result by multiplication.

> **Why this exercise:** teaches how to recognize invertibility and the inverse without using a full procedure when the matrix structure gives the answer immediately.

## Solution

**Rule.** A diagonal matrix is triangular, so its determinant is the product of its diagonal entries. It is invertible exactly when all diagonal entries are nonzero, and then its inverse is the diagonal matrix whose diagonal entries are the reciprocals $`\dfrac{1}{d_i}`$ of the original ones.

**Part 1: The matrix $`D`$.** The diagonal entries of $`D`$ are $`2`$, $`-3`$ and $`5`$, all nonzero. Indeed, $`\det D = 2\cdot(-3)\cdot5 = -30 \neq 0`$, so $`D`$ is invertible.

**Part 2: The matrix $`E`$.** The diagonal entries of $`E`$ are $`2`$, $`0`$ and $`5`$. Here $`\det E = 2\cdot0\cdot5 = 0`$. Also the second row of $`E`$ is $`(0,0,0)`$, a row of zeros, so the rows are dependent. Therefore $`E`$ is not invertible.

**Part 3: The inverse of $`D`$.** We replace each diagonal entry by its reciprocal:

```math
D^{-1}=\begin{pmatrix} \frac12 & 0 & 0 \\ 0 & -\frac13 & 0 \\ 0 & 0 & \frac15 \end{pmatrix}.
```

**Conclusion.** The matrix $`D`$ is invertible with

```math
D^{-1}=\begin{pmatrix} \frac12 & 0 & 0 \\ 0 & -\frac13 & 0 \\ 0 & 0 & \frac15 \end{pmatrix},
```

and the matrix $`E`$ is not invertible, because it has a zero on the diagonal (a zero row) and $`\det E = 0`$.

**Verification.** We multiply $`D`$ by the result:

```math
DD^{-1}=\begin{pmatrix} 2\cdot\frac12 & 0 & 0 \\ 0 & (-3)\cdot\left(-\frac13\right) & 0 \\ 0 & 0 & 5\cdot\frac15 \end{pmatrix}=\begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix}=I.
```

For $`E`$ we can also see directly that no inverse exists: for any matrix $`X`$, the second row of $`EX`$ is $`(0,0,0)`$, because the second row of $`E`$ is zero. So $`EX`$ can never be $`I`$, whose second row is $`(0,1,0)`$.