# Exercise 8. Determinant of a Product

## Question

Let $`A,B`$ be square matrices such that $`\det A=3`$ and $`\det B=-5`$. Compute $`\det(AB)`$, $`\det(BA)`$ and, if it exists, $`\det(A^{-1}B)`$. Explain why the first two results are equal even though usually $`AB\neq BA`$.

> **Why this exercise:** organizes how determinants behave with respect to products and inverses.

## Solution

**Rules.** For two $`n \times n`$ matrices $`A`$ and $`B`$:

- $`\det(AB) = \det A\cdot\det B`$;
- a matrix $`A`$ is invertible exactly when $`\det A \neq 0`$, and in that case $`\det(A^{-1}) = \dfrac{1}{\det A}`$. This follows from $`AA^{-1}=I`$, because $`\det A\cdot\det(A^{-1}) = \det I = 1`$.

We assume that $`A`$ and $`B`$ are square matrices of the same size, so that the products $`AB`$ and $`BA`$ are defined.

**Part 1: $`\det(AB)`$.** By the product rule,

```math
\det(AB) = \det A\cdot\det B = 3\cdot(-5) = -15.
```

**Part 2: $`\det(BA)`$.** By the same rule,

```math
\det(BA) = \det B\cdot\det A = (-5)\cdot 3 = -15.
```

**Part 3: Why the first two results are equal.** The matrices $`AB`$ and $`BA`$ are usually different, because matrix multiplication is not commutative. But the determinant of a product is the product of two numbers, $`\det A`$ and $`\det B`$, and multiplication of numbers is commutative. Therefore

```math
\det(AB) = \det A\cdot\det B = \det B\cdot\det A = \det(BA).
```

So two different matrices $`AB`$ and $`BA`$ can still have the same determinant.

**Part 4: $`\det(A^{-1}B)`$.** Since $`\det A = 3 \neq 0`$, the matrix $`A`$ is invertible, so $`A^{-1}`$ exists and $`\det(A^{-1}) = \dfrac{1}{3}`$. Using the product rule,

```math
\det(A^{-1}B) = \det(A^{-1})\cdot\det B = \frac{1}{3}\cdot(-5) = -\frac{5}{3}.
```

**Conclusion.**

```math
\det(AB) = -15,\qquad \det(BA) = -15,\qquad \det(A^{-1}B) = -\frac{5}{3}.
```

**Verification.** We check the results on one example of $`2\times 2`$ matrices with $`\det A=3`$ and $`\det B=-5`$:

```math
A=\begin{pmatrix} 1 & 1 \\ 0 & 3 \end{pmatrix},\qquad B=\begin{pmatrix} 1 & 0 \\ 2 & -5 \end{pmatrix}.
```

Indeed, $`\det A = 1\cdot 3 - 1\cdot 0 = 3`$ and $`\det B = 1\cdot(-5) - 0\cdot 2 = -5`$. Then

```math
AB=\begin{pmatrix} 3 & -5 \\ 6 & -15 \end{pmatrix},\qquad BA=\begin{pmatrix} 1 & 1 \\ 2 & -13 \end{pmatrix}.
```

These matrices are different, so $`AB\neq BA`$. Their determinants are

```math
\det(AB) = 3\cdot(-15) - (-5)\cdot 6 = -45 + 30 = -15,\qquad \det(BA) = 1\cdot(-13) - 1\cdot 2 = -15.
```

Both agree with the result above. For the inverse, $`A^{-1}=\begin{pmatrix} 1 & -\frac13 \\ 0 & \frac13 \end{pmatrix}`$, so

```math
A^{-1}B=\begin{pmatrix} \frac13 & \frac53 \\ \frac23 & -\frac53 \end{pmatrix},\qquad
\det(A^{-1}B) = \frac13\cdot\left(-\frac53\right) - \frac53\cdot\frac23 = -\frac59 - \frac{10}{9} = -\frac{15}{9} = -\frac53.
```

This agrees with Part 4.