# Exercise 14. A System of Equations and the Determinant

## Question

Consider the system $`Ax=b`$, where

```math
A=\begin{pmatrix} 1 & 2 \\ k & 4 \end{pmatrix}.
```

For which values of $`k`$ does the system have exactly one solution for every $`b`$? For the remaining value, give an example of a right-hand side $`b`$ for which the system has infinitely many solutions, and an example for which it has no solution.

> **Why this exercise:** connects the determinant with uniqueness of solutions and requires distinguishing the exceptional cases.

## Solution

**Rule.** For a square matrix $`A`$, the system $`Ax=b`$ has exactly one solution for every $`b`$ exactly when $`A`$ is invertible, that is, when $`\det A \neq 0`$. If $`\det A = 0`$, then for some $`b`$ there is no solution and for other $`b`$ there are infinitely many solutions.

**Part 1: The determinant.**

```math
\det A = 1\cdot 4 - 2\cdot k = 4 - 2k.
```

**Part 2: Unique solutions.** We have $`\det A = 0`$ exactly when $`4 - 2k = 0`$, that is, $`k = 2`$. So for every $`k \neq 2`$ we have $`\det A \neq 0`$, and the system has exactly one solution for every $`b`$.

**Part 3: The remaining value $`k=2`$.** For $`k=2`$ the system is

```math
\begin{pmatrix} 1 & 2 \\ 2 & 4 \end{pmatrix}\begin{pmatrix} x \\ y \end{pmatrix}=\begin{pmatrix} b_1 \\ b_2 \end{pmatrix},
\qquad\text{that is,}\qquad
\begin{aligned} x + 2y &= b_1,\\ 2x + 4y &= b_2. \end{aligned}
```

The second row of the matrix is $`2`$ times the first row, so the left side of the second equation is always $`2`$ times the left side of the first equation. If we subtract $`2`$ times the first equation from the second, we get $`0 = b_2 - 2b_1`$. So the system has solutions exactly when $`b_2 = 2b_1`$.

**Part 4: An example with infinitely many solutions.** Take $`b=\begin{pmatrix} 1 \\ 2 \end{pmatrix}`$. Then $`b_2 = 2b_1`$, and the two equations $`x+2y=1`$ and $`2x+4y=2`$ say the same thing. Every pair $`(x,y)=(1-2y,\,y)`$ is a solution, for example $`(1,0)`$ and $`(-1,1)`$. So there are infinitely many solutions.

**Part 5: An example with no solution.** Take $`b=\begin{pmatrix} 1 \\ 3 \end{pmatrix}`$. Then $`b_2 \neq 2b_1`$. The first equation gives $`x+2y=1`$, so $`2x+4y=2`$, but the second equation requires $`2x+4y=3`$. This is a contradiction, so there is no solution.

**Conclusion.** The system has exactly one solution for every $`b`$ for all $`k \neq 2`$. For $`k=2`$ we have $`\det A = 0`$; then $`b=(1,2)^T`$ gives infinitely many solutions and $`b=(1,3)^T`$ gives no solution.

**Verification.** We check two solutions from Part 4 in the system with $`k=2`$ and $`b=(1,2)^T`$. For $`(x,y)=(1,0)`$: $`1+0=1`$ and $`2\cdot1+0=2`$. For $`(x,y)=(-1,1)`$: $`-1+2=1`$ and $`-2+4=2`$. Both satisfy the system.