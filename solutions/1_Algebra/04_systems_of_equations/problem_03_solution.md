# Exercise 3. Inconsistent System

## Question

Solve or show that the system is inconsistent:

```math
\begin{cases}
x+2y=3, \\
2x+4y=7.
\end{cases}
```

Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

> **Why this exercise:** teaches how to recognize that a system has no solution without guessing.

## Solution

**Rule.** A system is inconsistent (has no solution) exactly when, after elimination, the augmented matrix contains a row of the form

```math
\left(\begin{array}{cc|c} 0 & 0 & c \end{array}\right)\qquad\text{with } c\neq 0,
```

because this row represents the equation $`0=c`$, which is impossible.

**Part 1: The augmented matrix.**

```math
\left(\begin{array}{cc|c} 1 & 2 & 3 \\ 2 & 4 & 7 \end{array}\right).
```

**Part 2: Elimination.** Replace $`R_2`$ by $`R_2 - 2R_1`$. Here $`(2,4\mid 7) - 2\cdot(1,2\mid 3) = (0,0\mid 1)`$:

```math
\left(\begin{array}{cc|c} 1 & 2 & 3 \\ 0 & 0 & 1 \end{array}\right).
```

**Part 3: Interpretation.** The second row represents the equation

```math
0\cdot x + 0\cdot y = 1, \qquad\text{that is,}\qquad 0 = 1.
```

This is a contradiction, and no values of $`x`$ and $`y`$ can satisfy it. In terms of the original equations: if $`x+2y=3`$, then doubling gives $`2x+4y=6`$, but the second equation requires $`2x+4y=7`$.

**Conclusion.** The system is inconsistent, so it has no solution.

**Verification.** We check the conclusion in a different way. The left sides of the two equations are proportional: $`2x+4y = 2\cdot(x+2y)`$. So the equations say $`x+2y=3`$ and $`x+2y=\tfrac72`$. A number cannot be equal to both $`3`$ and $`\tfrac72`$, which agrees with the contradiction found in the matrix. Geometrically, these are two distinct parallel lines, which never meet.