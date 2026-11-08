# Exercise 1. Definition of the Inverse

## Question

For

```math
A=\begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix},\qquad B=\begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix}
```

check, without using a formula, whether $`B=A^{-1}`$. Compute $`AB`$ and $`BA`$ and relate the result to the definition of the inverse.

> **Why this exercise:** starts from the definition of the inverse through multiplication before any formulas or computational methods are introduced.

## Solution

**Definition.** A square matrix $`B`$ is the inverse of a square matrix $`A`$ of the same size if

```math
AB = I \quad\text{and}\quad BA = I,
```

where $`I`$ is the identity matrix. In that case we write $`B = A^{-1}`$.

**Part 1: The product $`AB`$.** Each entry is the dot product of a row of $`A`$ with a column of $`B`$:

```math
AB=\begin{pmatrix} 2\cdot1+1\cdot(-1) & 2\cdot(-1)+1\cdot2 \\ 1\cdot1+1\cdot(-1) & 1\cdot(-1)+1\cdot2 \end{pmatrix}=\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}=I.
```

**Part 2: The product $`BA`$.** Now we multiply rows of $`B`$ by columns of $`A`$:

```math
BA=\begin{pmatrix} 1\cdot2+(-1)\cdot1 & 1\cdot1+(-1)\cdot1 \\ (-1)\cdot2+2\cdot1 & (-1)\cdot1+2\cdot1 \end{pmatrix}=\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}=I.
```

**Conclusion.** Both products equal the identity matrix, $`AB = I`$ and $`BA = I`$. By the definition of the inverse, $`B`$ is the inverse of $`A`$:

```math
B = A^{-1}=\begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix}.
```

**Verification.** We check the result in a different way. Both products are the identity, so neither can be $`I`$ by accident in only one order. As a quick extra check, the determinant of $`A`$ is $`2\cdot1-1\cdot1=1`$ and the determinant of $`B`$ is $`1\cdot2-(-1)\cdot(-1)=1`$. Their product is $`1\cdot 1 = 1 = \det I`$, which is consistent with $`\det(AB)=\det I`$.