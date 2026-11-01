# Exercise 10. Columns of a Matrix Product

## Question

Given

```math
A=\begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}, \qquad B=\begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix}.
```

Denote the columns of $`B`$ by $`b_1,b_2`$.

1. Compute $`Ab_1`$ and $`Ab_2`$.
2. Compute the matrix $`AB`$.
3. Compare the results and explain why the columns of $`AB`$ are exactly the vectors $`Ab_1`$ and $`Ab_2`$.

> **Why this exercise:** extends the interpretation of matrix-vector multiplication to a product of two matrices instead of simply repeating another $`Ax`$ exercise.

## Solution

**Rule.** The matrix $`A`$ is $`2 \times 3`$ and $`B`$ is $`3 \times 2`$, so the inner numbers are equal ($`3=3`$) and $`AB`$ is a $`2 \times 2`$ matrix. The columns of $`B`$ are

```math
b_1=\begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix}, \qquad b_2=\begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}.
```

Each entry of a matrix-vector product is the dot product of a row of $`A`$ with the vector.

**Part 1: Computing $`Ab_1`$ and $`Ab_2`$.** We multiply each row of $`A`$ by the vector:

```math
Ab_1=\begin{pmatrix} 1\cdot1+2\cdot(-1)+0\cdot3 \\ 0\cdot1+1\cdot(-1)+1\cdot3 \end{pmatrix}=\begin{pmatrix} -1 \\ 2 \end{pmatrix},
```

```math
Ab_2=\begin{pmatrix} 1\cdot2+2\cdot0+0\cdot1 \\ 0\cdot2+1\cdot0+1\cdot1 \end{pmatrix}=\begin{pmatrix} 2 \\ 1 \end{pmatrix}.
```

**Part 2: Computing $`AB`$.** The entry $`(AB)_{ij}`$ is the dot product of row $`i`$ of $`A`$ with column $`j`$ of $`B`$:

```math
AB=\begin{pmatrix} 1\cdot1+2\cdot(-1)+0\cdot3 & 1\cdot2+2\cdot0+0\cdot1 \\ 0\cdot1+1\cdot(-1)+1\cdot3 & 0\cdot2+1\cdot0+1\cdot1 \end{pmatrix}=\begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}.
```

**Part 3: Comparison and explanation.** The first column of $`AB`$ is $`(-1,2)^T`$, which is $`Ab_1`$, and the second column of $`AB`$ is $`(2,1)^T`$, which is $`Ab_2`$. So

```math
AB=\begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix}.
```

This is true because of how the product is defined. The entry in column $`j`$ of $`AB`$ is the dot product of a row of $`A`$ with column $`j`$ of $`B`$, that is, with $`b_j`$. These are exactly the same dot products that we compute in $`Ab_j`$, row by row. Therefore column $`j`$ of $`AB`$ equals $`Ab_j`$. In other words, multiplying $`A`$ by $`B`$ means multiplying $`A`$ by each column of $`B`$ separately and writing the results side by side.

**Verification.** We check one entry in a different way. The entry in row 2, column 1 of $`AB`$ is $`0\cdot1+1\cdot(-1)+1\cdot3=2`$, which is the second entry of $`Ab_1`$. The sizes also agree: each $`Ab_j`$ has 2 entries, and $`AB`$ has 2 rows and 2 columns.