# Exercise 15. Associativity of Multiplication and Different Calculation Paths

## Question

Given

```math
A=\begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix}, \quad B=\begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix}, \quad C=\begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix}.
```

Compute $`(AB)C`$ and $`A(BC)`$. Compare the results and the number of intermediate operations. Explain what associativity of matrix multiplication means in this example.

> **Why this exercise:** reinforces associativity by comparing two mathematically equivalent calculation paths.

## Solution

**Rule.** The entry $`(XY)_{ij}`$ is the dot product of row $`i`$ of $`X`$ with column $`j`$ of $`Y`$. The sizes are $`A`$: $`2\times3`$, $`B`$: $`3\times2`$, $`C`$: $`2\times2`$. All the products below are defined, because the inner numbers are equal in each case.

**Part 1: The path $`(AB)C`$.** First, $`AB`$ is $`(2\times3)(3\times2)=2\times2`$:

```math
AB=\begin{pmatrix} 1\cdot1+2\cdot2+0\cdot(-1) & 1\cdot0+2\cdot1+0\cdot3 \\ 0\cdot1+1\cdot2+1\cdot(-1) & 0\cdot0+1\cdot1+1\cdot3 \end{pmatrix}=\begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix}.
```

Then $`(AB)C`$ is $`(2\times2)(2\times2)=2\times2`$:

```math
(AB)C=\begin{pmatrix} 5\cdot2+2\cdot0 & 5\cdot1+2\cdot(-1) \\ 1\cdot2+4\cdot0 & 1\cdot1+4\cdot(-1) \end{pmatrix}=\begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}.
```

**Part 2: The path $`A(BC)`$.** First, $`BC`$ is $`(3\times2)(2\times2)=3\times2`$:

```math
BC=\begin{pmatrix} 1\cdot2+0\cdot0 & 1\cdot1+0\cdot(-1) \\ 2\cdot2+1\cdot0 & 2\cdot1+1\cdot(-1) \\ -1\cdot2+3\cdot0 & -1\cdot1+3\cdot(-1) \end{pmatrix}=\begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix}.
```

Then $`A(BC)`$ is $`(2\times3)(3\times2)=2\times2`$:

```math
A(BC)=\begin{pmatrix} 1\cdot2+2\cdot4+0\cdot(-2) & 1\cdot1+2\cdot1+0\cdot(-4) \\ 0\cdot2+1\cdot4+1\cdot(-2) & 0\cdot1+1\cdot1+1\cdot(-4) \end{pmatrix}=\begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}.
```

**Part 3: Comparison of the results.** Both paths give the same matrix:

```math
(AB)C=A(BC)=\begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}.
```

**Part 4: Comparison of the number of operations.** A product of an $`m\times n`$ matrix and an $`n\times q`$ matrix has $`mq`$ entries, and each entry needs $`n`$ multiplications, so it needs $`mnq`$ multiplications in total.

| Path | First product | Second product | Total multiplications |
|---|---|---|---|
| $`(AB)C`$ | $`AB`$: $`2\cdot3\cdot2=12`$ | $`(AB)C`$: $`2\cdot2\cdot2=8`$ | $`20`$ |
| $`A(BC)`$ | $`BC`$: $`3\cdot2\cdot2=12`$ | $`A(BC)`$: $`2\cdot3\cdot2=12`$ | $`24`$ |

So the result is the same, but the path $`(AB)C`$ uses fewer multiplications ($`20`$ against $`24`$) in this example. The reason is that in this path the intermediate matrix $`AB`$ is only $`2\times2`$, while in the other path the intermediate matrix $`BC`$ is larger, $`3\times2`$.

**Part 5: What associativity means.** Associativity means that for matrices of compatible sizes

```math
(AB)C=A(BC),
```

so the way we place the brackets does not change the result, and we can write the product simply as $`ABC`$. In this example we checked it directly: both paths gave $`\begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}`$. It is important that associativity allows us to change the brackets, but it does not allow us to change the order of the factors. We still cannot write $`BAC`$ instead of $`ABC`$, because matrix multiplication is not commutative (see Exercise 4). The brackets only change the amount of work, as Part 4 shows.

**Verification.** We check one entry independently. The entry in row 1, column 2 of $`(AB)C`$ is $`5\cdot1+2\cdot(-1)=3`$, and the entry in row 1, column 2 of $`A(BC)`$ is $`1\cdot1+2\cdot1+0\cdot(-4)=3`$. They are equal, and both match the entry $`3`$ of the final matrix.