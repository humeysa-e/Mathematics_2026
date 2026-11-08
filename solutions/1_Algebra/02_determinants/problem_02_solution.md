# Exercise 2. Determinant of a 3×3 Matrix

## Question

For

```math
A=\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 2 & 1 & 5 \end{pmatrix}
```

compute $`\det A`$ using Sarrus' rule. Then perform one simple check using a chosen property of the determinant.

> **Why this exercise:** teaches a basic method for $`3\times 3`$ matrices and builds the habit of checking the result without adding a second full solution.

## Solution

**Rule (Sarrus).** For a $`3 \times 3`$ matrix

```math
M=\begin{pmatrix} a & b & c \\ d & e & f \\ g & h & i \end{pmatrix}
```

Sarrus' rule gives

```math
\det M = aei + bfg + cdh - ceg - bdi - afh.
```

The first three terms come from the diagonals going down to the right, and the last three terms come from the diagonals going up to the right.

**Part 1: The entries.** Here $`a=1`$, $`b=2`$, $`c=-1`$, $`d=0`$, $`e=3`$, $`f=4`$, $`g=2`$, $`h=1`$, $`i=5`$.

**Part 2: The three positive terms.**

```math
aei = 1\cdot 3\cdot 5 = 15, \qquad bfg = 2\cdot 4\cdot 2 = 16, \qquad cdh = (-1)\cdot 0\cdot 1 = 0.
```

**Part 3: The three negative terms.**

```math
ceg = (-1)\cdot 3\cdot 2 = -6, \qquad bdi = 2\cdot 0\cdot 5 = 0, \qquad afh = 1\cdot 4\cdot 1 = 4.
```

**Part 4: The determinant.** We add the positive terms and subtract the negative terms:

```math
\det A = (15 + 16 + 0) - (-6 + 0 + 4) = 31 - (-2) = 33.
```

**Conclusion.** $`\det A = 33`$. Since $`\det A \neq 0`$, the matrix $`A`$ is invertible.

**Verification.** We use the property that adding a multiple of one row to another row does not change the determinant. Replace row 3 by row 3 minus $`2`$ times row 1, that is, $`(2,1,5) - 2\cdot(1,2,-1) = (0,-3,7)`$. The new matrix is

```math
\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 4 \\ 0 & -3 & 7 \end{pmatrix}.
```

Its first column is $`(1,0,0)^T`$, so its determinant is $`1`$ times the determinant of the remaining $`2 \times 2`$ block:

```math
1\cdot\det\begin{pmatrix} 3 & 4 \\ -3 & 7 \end{pmatrix} = 3\cdot 7 - 4\cdot(-3) = 21 + 12 = 33.
```

This agrees with the result from Sarrus' rule.