# Exercise 4. Matrix Multiplication and Noncommutativity

## Question

For

```math
A=\begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}, \qquad B=\begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}
```

compute $`AB`$ and $`BA`$. Is $`AB=BA`$? Use this example to explain what noncommutativity of matrix multiplication means.

> **Why this exercise:** shows one of the most important differences between matrix multiplication and multiplication of numbers.

## Solution

**Rule.** For $`2 \times 2`$ matrices, the entry $`(XY)_{ij}`$ is the dot product of row $`i`$ of $`X`$ with column $`j`$ of $`Y`$, that is, $`(XY)_{ij} = x_{i1}y_{1j} + x_{i2}y_{2j}`$.

**Part 1: The product $`AB`$.** We multiply the rows of $`A`$ by the columns of $`B`$:

```math
AB = \begin{pmatrix} 1\cdot2+2\cdot3 & 1\cdot0+2\cdot1 \\ 0\cdot2+1\cdot3 & 0\cdot0+1\cdot1 \end{pmatrix} = \begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}.
```

**Part 2: The product $`BA`$.** Now the roles are exchanged, so we multiply the rows of $`B`$ by the columns of $`A`$:

```math
BA = \begin{pmatrix} 2\cdot1+0\cdot0 & 2\cdot2+0\cdot1 \\ 3\cdot1+1\cdot0 & 3\cdot2+1\cdot1 \end{pmatrix} = \begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}.
```

**Part 3: Is $`AB=BA`$?** Two matrices are equal only if all their corresponding entries are equal. Here the entries in row 1, column 1 are different ($`8 \neq 2`$), so

```math
AB \neq BA.
```

**Part 4: Noncommutativity.** For real numbers, the order of multiplication does not matter, $`ab=ba`$. This example shows that for matrices the order matters: even though both $`AB`$ and $`BA`$ are defined and have the same size $`2 \times 2`$, they give different results. Noncommutativity means that in general $`AB \neq BA`$, so we cannot swap the factors in a matrix product. (For some special pairs of matrices $`AB=BA`$ does hold, but it is not true in general, and one counterexample like this one is enough to show it.)

**Verification.** We recompute one entry in a different way. The entry in row 1, column 1 of $`AB`$ is $`1\cdot2+2\cdot3=2+6=8`$, and the entry in row 1, column 1 of $`BA`$ is $`2\cdot1+0\cdot0=2`$. These match the results above, and they are different.