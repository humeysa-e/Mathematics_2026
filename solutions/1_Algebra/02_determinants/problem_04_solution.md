# Exercise 4. Triangular Matrix

## Question

Without expanding the determinant, compute

```math
\det\begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix}.
```

State the rule for an arbitrary triangular matrix and explain it using this example.

> **Why this exercise:** reinforces an important property of triangular matrices.

## Solution

**Rule.** A square matrix is called upper triangular if all entries below the main diagonal are zero, and lower triangular if all entries above the main diagonal are zero. The determinant of any triangular matrix is the product of its diagonal entries:

```math
\det M = m_{11}\, m_{22} \cdots m_{nn}.
```

**Part 1: The matrix is triangular.** Let

```math
M=\begin{pmatrix} 2 & 4 & 1 \\ 0 & -3 & 5 \\ 0 & 0 & 7 \end{pmatrix}.
```

All entries below the main diagonal are zero, so $`M`$ is upper triangular. Its diagonal entries are $`2`$, $`-3`$ and $`7`$.

**Part 2: The determinant.** By the rule,

```math
\det M = 2\cdot(-3)\cdot 7 = -42.
```

**Part 3: Why the rule works in this example.** For a $`3\times 3`$ matrix with entries $`a,b,c;\ d,e,f;\ g,h,i`$, Sarrus' rule gives

```math
\det M = aei + bfg + cdh - ceg - bdi - afh.
```

In our matrix $`d=0`$, $`g=0`$ and $`h=0`$, which are exactly the entries below the diagonal. Every term except $`aei`$ contains at least one of $`d`$, $`g`$, $`h`$:

```math
bfg,\ ceg \ \text{contain } g, \qquad cdh,\ bdi \ \text{contain } d, \qquad afh \ \text{contains } h.
```

So all these terms are $`0`$, and only the diagonal product remains:

```math
\det M = aei = 2\cdot(-3)\cdot 7 = -42.
```

The same idea works for any size: every term of the determinant uses one entry from each row and each column, and in a triangular matrix the only such choice without a zero is the main diagonal. The argument for a lower triangular matrix is the same, with the zeros above the diagonal.

**Conclusion.** The determinant of a triangular matrix is the product of its diagonal entries, so

```math
\det M = -42.
```

Since $`\det M \neq 0`$, the matrix $`M`$ is invertible.

**Verification.** We check the result in a different way. The first column of $`M`$ is $`(2,0,0)^T`$, so expanding along it leaves only the entry $`2`$:

```math
\det M = 2\cdot\det\begin{pmatrix} -3 & 5 \\ 0 & 7 \end{pmatrix} = 2\cdot\big((-3)\cdot 7 - 5\cdot 0\big) = 2\cdot(-21) = -42.
```

This agrees with the product of the diagonal entries.