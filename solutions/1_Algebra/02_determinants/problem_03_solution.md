# Exercise 3. Swapping Two Rows

## Question

For

```math
A=\begin{pmatrix} 1 & 2 & 0 \\ 0 & 3 & 1 \\ 2 & 1 & 1 \end{pmatrix}
```

compute $`\det A`$. Then form a matrix $`B`$ by swapping the first and second rows of $`A`$.

First predict $`\det B`$ using a determinant property, and then verify your prediction by calculation.

> **Why this exercise:** gives a second classical calculation with a $`3\times 3`$ determinant while teaching the precise effect of a row swap on the sign of the determinant.

## Solution

**Rule.** For a $`3 \times 3`$ matrix

```math
M=\begin{pmatrix} a & b & c \\ d & e & f \\ g & h & i \end{pmatrix}
```

Sarrus' rule gives

```math
\det M = aei + bfg + cdh - ceg - bdi - afh.
```

**Property.** Swapping two rows of a matrix changes the sign of its determinant.

**Part 1: The determinant of $`A`$.** Here $`a=1`$, $`b=2`$, $`c=0`$, $`d=0`$, $`e=3`$, $`f=1`$, $`g=2`$, $`h=1`$, $`i=1`$. The positive terms are

```math
aei = 1\cdot 3\cdot 1 = 3, \qquad bfg = 2\cdot 1\cdot 2 = 4, \qquad cdh = 0\cdot 0\cdot 1 = 0,
```

and the negative terms are

```math
ceg = 0\cdot 3\cdot 2 = 0, \qquad bdi = 2\cdot 0\cdot 1 = 0, \qquad afh = 1\cdot 1\cdot 1 = 1.
```

Therefore

```math
\det A = (3 + 4 + 0) - (0 + 0 + 1) = 7 - 1 = 6.
```

**Part 2: The matrix $`B`$ and the prediction.** Swapping the first and second rows of $`A`$ gives

```math
B=\begin{pmatrix} 0 & 3 & 1 \\ 1 & 2 & 0 \\ 2 & 1 & 1 \end{pmatrix}.
```

Since a row swap changes the sign of the determinant, we predict

```math
\det B = -\det A = -6.
```

**Part 3: Verification by calculation.** For $`B`$ we have $`a=0`$, $`b=3`$, $`c=1`$, $`d=1`$, $`e=2`$, $`f=0`$, $`g=2`$, $`h=1`$, $`i=1`$. The positive terms are

```math
aei = 0\cdot 2\cdot 1 = 0, \qquad bfg = 3\cdot 0\cdot 2 = 0, \qquad cdh = 1\cdot 1\cdot 1 = 1,
```

and the negative terms are

```math
ceg = 1\cdot 2\cdot 2 = 4, \qquad bdi = 3\cdot 1\cdot 1 = 3, \qquad afh = 0\cdot 0\cdot 1 = 0.
```

Therefore

```math
\det B = (0 + 0 + 1) - (4 + 3 + 0) = 1 - 7 = -6.
```

**Conclusion.** We found $`\det A = 6`$ and $`\det B = -6`$. The calculation agrees with the prediction, so swapping two rows changes the sign of the determinant.