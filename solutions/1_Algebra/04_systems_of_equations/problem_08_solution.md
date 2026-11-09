# Exercise 8. Two Systems with the Same Coefficient Matrix

## Question

Solve by elimination the two systems

```math
\begin{cases}
2x+y=5, \\
x-y=1,
\end{cases}
```

```math
\begin{cases}
2x+y=1, \\
x-y=4.
\end{cases}
```

Compare the successive elimination steps. Which part of the calculation is the same in both cases, and why?

> **Why this exercise:** shows the role of the coefficient matrix independently of the right-hand side.

## Solution

**Method.** We use Gaussian elimination on the augmented matrix. Both systems have the same coefficient matrix

```math
A=\begin{pmatrix} 2 & 1 \\ 1 & -1 \end{pmatrix},
```

and they differ only in the right-hand side.

**Part 1: The first system.** The augmented matrix is

```math
\left(\begin{array}{cc|c} 2 & 1 & 5 \\ 1 & -1 & 1 \end{array}\right).
```

Step 1: swap $`R_1`$ and $`R_2`$, so that the first pivot is $`1`$:

```math
\left(\begin{array}{cc|c} 1 & -1 & 1 \\ 2 & 1 & 5 \end{array}\right).
```

Step 2: replace $`R_2`$ by $`R_2 - 2R_1`$. Here $`(2,1\mid 5) - 2\cdot(1,-1\mid 1) = (0,3\mid 3)`$:

```math
\left(\begin{array}{cc|c} 1 & -1 & 1 \\ 0 & 3 & 3 \end{array}\right).
```

Step 3: back substitution. The second row gives $`3y=3`$, so $`y=1`$. The first row gives $`x-y=1`$, so $`x=2`$.

**Part 2: The second system.** The augmented matrix is

```math
\left(\begin{array}{cc|c} 2 & 1 & 1 \\ 1 & -1 & 4 \end{array}\right).
```

Step 1: swap $`R_1`$ and $`R_2`$:

```math
\left(\begin{array}{cc|c} 1 & -1 & 4 \\ 2 & 1 & 1 \end{array}\right).
```

Step 2: replace $`R_2`$ by $`R_2 - 2R_1`$. Here $`(2,1\mid 1) - 2\cdot(1,-1\mid 4) = (0,3\mid -7)`$:

```math
\left(\begin{array}{cc|c} 1 & -1 & 4 \\ 0 & 3 & -7 \end{array}\right).
```

Step 3: back substitution. The second row gives $`3y=-7`$, so $`y=-\dfrac73`$. The first row gives $`x=4+y=4-\dfrac73=\dfrac53`$.

**Part 3: Comparison.** In both systems the row operations were exactly the same: swap $`R_1`$ and $`R_2`$, then $`R_2\leftarrow R_2-2R_1`$. The coefficient part became the same matrix in both cases:

```math
\begin{pmatrix} 1 & -1 \\ 0 & 3 \end{pmatrix}.
```

Only the right-hand column was different: $`(1,3)^T`$ for the first system and $`(4,-7)^T`$ for the second.

**Why the operations are the same.** The choice of row operations depends only on the entries of the coefficient matrix, because we use them to create zeros and pivots in the left part. The right-hand side is only carried along by the same operations. So the left part of the calculation can be done once and reused for both systems, for example by working with the matrix $`\left(\begin{array}{cc|cc} 2 & 1 & 5 & 1 \\ 1 & -1 & 1 & 4 \end{array}\right)`$.

**Conclusion.** The first system has the solution $`(x,y)=(2,1)`$ and the second system has the solution $`(x,y)=\left(\tfrac53,\ -\tfrac73\right)`$. The elimination steps are the same, because the coefficient matrix is the same.

**Verification.** For the first system: $`2\cdot2+1=5`$ and $`2-1=1`$. For the second system: $`2\cdot\tfrac53+\left(-\tfrac73\right)=\tfrac{10}{3}-\tfrac73=1`$ and $`\tfrac53-\left(-\tfrac73\right)=\tfrac{12}{3}=4`$. All four equations hold.