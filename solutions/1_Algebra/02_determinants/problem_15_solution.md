# Exercise 15. Combining Determinant Properties

## Question

Let $`A`$ and $`B`$ be invertible $`2\times 2`$ matrices with

```math
\det A=-2,\qquad \det B=3.
```

Without finding the entries of the matrices, compute

```math
\det\left(B^{-1}A^TB\right).
```

State the determinant properties you use in order and explain why the factors involving $`B`$ eventually cancel.

> **Why this exercise:** tests the transfer of several known properties into one short problem instead of checking a single property again with numbers.

## Solution

**Properties.** For $`n \times n`$ matrices:

1. $`\det(XY) = \det X\cdot\det Y`$ (product rule);
2. $`\det(X^T) = \det X`$;
3. if $`X`$ is invertible, then $`\det(X^{-1}) = \dfrac{1}{\det X}`$. This follows from $`XX^{-1}=I`$, because $`\det X\cdot\det(X^{-1}) = \det I = 1`$.

**Part 1: Split the product.** By property 1 (applied twice),

```math
\det\left(B^{-1}A^TB\right) = \det(B^{-1})\cdot\det(A^T)\cdot\det B.
```

**Part 2: Use the transpose and the inverse.** By property 2, $`\det(A^T) = \det A = -2`$. By property 3, $`\det(B^{-1}) = \dfrac{1}{\det B} = \dfrac{1}{3}`$. So

```math
\det\left(B^{-1}A^TB\right) = \frac{1}{3}\cdot(-2)\cdot 3.
```

**Part 3: Why the factors with $`B`$ cancel.** Determinants are numbers, and multiplication of numbers is commutative, so we can reorder the factors:

```math
\det(B^{-1})\cdot\det B\cdot\det(A^T) = \frac{1}{\det B}\cdot\det B\cdot\det(A^T) = 1\cdot\det(A^T).
```

The factors $`\det(B^{-1})`$ and $`\det B`$ are reciprocal numbers, so their product is $`1`$. The matrices $`B^{-1}`$, $`A^T`$ and $`B`$ do not commute, but this does not matter, because the product rule turns the matrix product into a product of numbers.

**Conclusion.**

```math
\det\left(B^{-1}A^TB\right) = \det A = -2.
```

**Verification.** We check the result on one example of $`2\times 2`$ matrices with $`\det A=-2`$ and $`\det B=3`$:

```math
A=\begin{pmatrix} -2 & 0 \\ 0 & 1 \end{pmatrix},\qquad B=\begin{pmatrix} 1 & 1 \\ 0 & 3 \end{pmatrix}.
```

Indeed, $`\det A = -2`$ and $`\det B = 1\cdot 3 - 1\cdot 0 = 3`$. Here $`A^T = A`$ and $`B^{-1}=\begin{pmatrix} 1 & -\frac13 \\ 0 & \frac13 \end{pmatrix}`$. Then

```math
A^TB=\begin{pmatrix} -2 & -2 \\ 0 & 3 \end{pmatrix},\qquad
B^{-1}A^TB=\begin{pmatrix} -2 & -3 \\ 0 & 1 \end{pmatrix}.
```

The determinant of this matrix is $`(-2)\cdot 1 - (-3)\cdot 0 = -2`$, which agrees with the result above.