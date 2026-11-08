# Exercise 15. Two Methods for Solving the Same System

## Question

For

```math
A=\begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix},\qquad b=\begin{pmatrix} 7 \\ 8 \end{pmatrix}
```

solve $`Ax=b`$ in two ways:

1. using $`A^{-1}b`$,
2. using Gaussian elimination.

Compare both solutions, the number of essential steps, and state which method was simpler in this example.

> **Why this exercise:** compares two known methods and prepares the student to choose a solution method consciously.

## Solution

**Method 1: Using $`A^{-1}b`$.**

*Step 1: The determinant.* $`\det A = 2\cdot3 - 1\cdot1 = 5 \neq 0`$, so $`A`$ is invertible.

*Step 2: The inverse.* By the $`2\times2`$ formula,

```math
A^{-1}=\frac15\begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}.
```

*Step 3: The product.*

```math
x=A^{-1}b=\frac15\begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}\begin{pmatrix} 7 \\ 8 \end{pmatrix}=\frac15\begin{pmatrix} 21-8 \\ -7+16 \end{pmatrix}=\frac15\begin{pmatrix} 13 \\ 9 \end{pmatrix}=\begin{pmatrix} \frac{13}{5} \\ \frac95 \end{pmatrix}.
```

**Method 2: Gaussian elimination.** We write the augmented matrix and swap the rows so that the first pivot is $`1`$:

```math
\left(\begin{array}{cc|c} 2 & 1 & 7 \\ 1 & 3 & 8 \end{array}\right)
\longrightarrow
\left(\begin{array}{cc|c} 1 & 3 & 8 \\ 2 & 1 & 7 \end{array}\right).
```

*Step 1: Eliminate.* Replace $`R_2`$ by $`R_2 - 2R_1`$. Here $`(2,1\mid 7) - 2\cdot(1,3\mid 8) = (0,-5\mid -9)`$:

```math
\left(\begin{array}{cc|c} 1 & 3 & 8 \\ 0 & -5 & -9 \end{array}\right).
```

*Step 2: Back substitution.* The second row gives $`-5y = -9`$, so $`y = \dfrac95`$. The first row gives

```math
x = 8 - 3y = 8 - \frac{27}{5} = \frac{40}{5}-\frac{27}{5} = \frac{13}{5}.
```

**Comparison.** Both methods give the same solution:

```math
x=\begin{pmatrix} \frac{13}{5} \\ \frac95 \end{pmatrix}.
```

Method 1 needed three essential steps (the determinant, the inverse with four entries, and the matrix–vector product). Method 2 needed essentially three steps as well (the row swap, one elimination, and back substitution), but it worked with whole numbers until the last line and did not require the whole inverse.

**Conclusion.** The solution is $`x=\left(\tfrac{13}{5},\ \tfrac95\right)^T`$. In this example Gaussian elimination was simpler, because for a single right-hand side $`b`$ we do not need the entire inverse matrix. The inverse method is more useful when the same matrix $`A`$ must be used with many different right-hand sides $`b`$, because then $`A^{-1}`$ is computed only once.

**Verification.** We substitute the solution into $`Ax`$:

```math
Ax=\begin{pmatrix} 2\cdot\frac{13}{5}+1\cdot\frac95 \\ 1\cdot\frac{13}{5}+3\cdot\frac95 \end{pmatrix}=\begin{pmatrix} \frac{26}{5}+\frac95 \\ \frac{13}{5}+\frac{27}{5} \end{pmatrix}=\begin{pmatrix} \frac{35}{5} \\ \frac{40}{5} \end{pmatrix}=\begin{pmatrix} 7 \\ 8 \end{pmatrix}=b.
```