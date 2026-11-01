# Exercise 6. Transpose

## Question

For

```math
A=\begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix}, \qquad B=\begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}
```

compute $`A^T`$, $`B^T`$, and $`AB`$. Then verify in this example that

```math
(AB)^T=B^TA^T.
```

> **Why this exercise:** teaches transposition and an important property that reverses the order of factors.

## Solution

**Rule.** The transpose $`X^T`$ of a matrix $`X`$ is obtained by writing the rows of $`X`$ as columns, that is, $`(X^T)_{ij} = x_{ji}`$. If $`X`$ has size $`m \times n`$, then $`X^T`$ has size $`n \times m`$. The product $`AB`$ is defined because $`A`$ is $`2 \times 3`$ and $`B`$ is $`3 \times 2`$, so the inner numbers are equal ($`3=3`$) and $`AB`$ is $`2 \times 2`$.

**Part 1: The transposes $`A^T`$ and $`B^T`$.** We write the rows as columns:

```math
A^T=\begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}, \qquad B^T=\begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix}.
```

**Part 2: The product $`AB`$.** Each entry is the dot product of a row of $`A`$ with a column of $`B`$:

```math
AB=\begin{pmatrix} 1\cdot1+2\cdot2+3\cdot(-1) & 1\cdot0+2\cdot1+3\cdot3 \\ 4\cdot1+5\cdot2+6\cdot(-1) & 4\cdot0+5\cdot1+6\cdot3 \end{pmatrix}=\begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix}.
```

**Part 3: The left side $`(AB)^T`$.** We transpose the matrix $`AB`$:

```math
(AB)^T=\begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}.
```

**Part 4: The right side $`B^TA^T`$.** The sizes are compatible: $`B^T`$ is $`2 \times 3`$ and $`A^T`$ is $`3 \times 2`$, so the result is $`2 \times 2`$. We multiply rows of $`B^T`$ by columns of $`A^T`$:

```math
B^TA^T=\begin{pmatrix} 1\cdot1+2\cdot2+(-1)\cdot3 & 1\cdot4+2\cdot5+(-1)\cdot6 \\ 0\cdot1+1\cdot2+3\cdot3 & 0\cdot4+1\cdot5+3\cdot6 \end{pmatrix}=\begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}.
```

**Conclusion.** Both sides give the same matrix, so in this example

```math
(AB)^T=B^TA^T=\begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}.
```

Note that the order of the factors is reversed. The product $`A^TB^T`$ would not even be defined here, because $`A^T`$ is $`3 \times 2`$ and $`B^T`$ is $`2 \times 3`$ would give a $`3 \times 3`$ matrix, which has the wrong size to equal $`(AB)^T`$.

**Verification.** We check one entry in a different way. The entry in row 1, column 2 of $`(AB)^T`$ is the entry in row 2, column 1 of $`AB`$, which is $`4\cdot1+5\cdot2+6\cdot(-1)=8`$. The entry in row 1, column 2 of $`B^TA^T`$ is $`1\cdot4+2\cdot5+(-1)\cdot6=8`$. They match.