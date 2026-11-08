# Exercise 9. Matrix Equation

## Question

Given

```math
A=\begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix},\qquad B=\begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix}.
```

Solve the equation $`AX=B`$ for $`X`$. Before calculating, decide on which side of the equation $`A^{-1}`$ must be used. Then check the result by computing $`AX`$.

> **Why this exercise:** teaches that order matters in matrix equations and must guide the solution.

## Solution

**Rule.** For a $`2 \times 2`$ matrix

```math
M=\begin{pmatrix} a & b \\ c & d \end{pmatrix}
```

with $`\det M = ad-bc \neq 0`$, the inverse is

```math
M^{-1}=\frac{1}{ad-bc}\begin{pmatrix} d & -b \\ -c & a \end{pmatrix}.
```

**Part 1: On which side to use $`A^{-1}`$.** In the equation $`AX=B`$ the matrix $`A`$ stands on the left of $`X`$. To remove it we must multiply by $`A^{-1}`$ **from the left** on both sides, so that $`A^{-1}`$ meets $`A`$:

```math
A^{-1}(AX)=A^{-1}B \quad\Longrightarrow\quad (A^{-1}A)X=A^{-1}B \quad\Longrightarrow\quad X=A^{-1}B.
```

Multiplying from the right would give $`AXA^{-1}`$, which does not simplify, because matrix multiplication is not commutative.

**Part 2: The inverse of $`A`$.** Here $`\det A = 1\cdot1-2\cdot0 = 1 \neq 0`$, so

```math
A^{-1}=\begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix}.
```

**Part 3: The solution.**

```math
X=A^{-1}B=\begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix}=\begin{pmatrix} 1\cdot3-2\cdot2 & 1\cdot1-2\cdot4 \\ 0\cdot3+1\cdot2 & 0\cdot1+1\cdot4 \end{pmatrix}=\begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}.
```

**Conclusion.**

```math
X=\begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}.
```

**Verification.** We compute $`AX`$:

```math
AX=\begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}=\begin{pmatrix} 1\cdot(-1)+2\cdot2 & 1\cdot(-7)+2\cdot4 \\ 0\cdot(-1)+1\cdot2 & 0\cdot(-7)+1\cdot4 \end{pmatrix}=\begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix}=B.
```

The equation holds, so the solution is correct.