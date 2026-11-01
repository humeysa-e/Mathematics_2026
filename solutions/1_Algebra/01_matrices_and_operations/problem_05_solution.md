# Exercise 5. Matrix Times Vector

## Question

Let

```math
A=\begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix}, \qquad x=\begin{pmatrix} 4 \\ 2 \end{pmatrix}.
```

Compute $`Ax`$. Then express $`Ax`$ as a linear combination of the columns of $`A`$, with coefficients coming from the vector $`x`$.

> **Why this exercise:** shows that multiplying a matrix by a vector can be understood as a linear combination of the matrix columns.

## Solution

**Rule.** For a $`2 \times 2`$ matrix $`A`$ and a vector $`x`$ with 2 entries, each entry of $`Ax`$ is the dot product of a row of $`A`$ with $`x`$. The sizes are compatible: $`A`$ is $`2 \times 2`$ and $`x`$ is $`2 \times 1`$, so $`Ax`$ is $`2 \times 1`$.

**Part 1: Computing $`Ax`$.** We multiply each row of $`A`$ by $`x`$:

```math
Ax = \begin{pmatrix} 2\cdot4+(-1)\cdot2 \\ 1\cdot4+3\cdot2 \end{pmatrix} = \begin{pmatrix} 8-2 \\ 4+6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}.
```

**Part 2: Linear combination of the columns.** The columns of $`A`$ are

```math
a_1=\begin{pmatrix} 2 \\ 1 \end{pmatrix}, \qquad a_2=\begin{pmatrix} -1 \\ 3 \end{pmatrix}.
```

If $`x=(x_1, x_2)^T`$, then $`Ax = x_1 a_1 + x_2 a_2`$, that is, the entries of $`x`$ are the coefficients of the columns. Here $`x_1=4`$ and $`x_2=2`$, so

```math
Ax = 4\begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2\begin{pmatrix} -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 8 \\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\ 6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}.
```

**Verification.** Both methods give the same vector $`\begin{pmatrix} 6 \\ 10 \end{pmatrix}`$. For example, the first entry is $`2\cdot4-1\cdot2=6`$ by rows and $`4\cdot2+2\cdot(-1)=6`$ by columns.