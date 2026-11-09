# Exercise 9. A System from a Sum Condition

## Question

Find numbers $`x,y`$ satisfying

```math
x+y=10,\qquad 2x+5y=32.
```

Solve the system and explain geometrically why the solution is unique.

> **Why this exercise:** reinforces the transition from two linear conditions to the intersection point of two lines.

## Solution

**Method.** We use Gaussian elimination on the augmented matrix.

**Part 1: Elimination.** The augmented matrix is

```math
\left(\begin{array}{cc|c} 1 & 1 & 10 \\ 2 & 5 & 32 \end{array}\right).
```

Replace $`R_2`$ by $`R_2 - 2R_1`$. Here $`(2,5\mid 32) - 2\cdot(1,1\mid 10) = (0,3\mid 12)`$:

```math
\left(\begin{array}{cc|c} 1 & 1 & 10 \\ 0 & 3 & 12 \end{array}\right).
```

**Part 2: Back substitution.** The second row gives $`3y=12`$, so $`y=4`$. The first row gives $`x+y=10`$, so $`x=6`$.

**Part 3: Geometric explanation.** Each equation describes a line in the plane. The first line, $`x+y=10`$, can be written as $`y=-x+10`$, with slope $`-1`$. The second line, $`2x+5y=32`$, can be written as $`y=-\tfrac25x+\tfrac{32}{5}`$, with slope $`-\tfrac25`$. The slopes are different, so the lines are not parallel, and two non-parallel lines in the plane meet in exactly one point. This is the unique solution. In terms of the matrix, $`\det\begin{pmatrix} 1 & 1 \\ 2 & 5 \end{pmatrix} = 1\cdot5-1\cdot2=3\neq 0`$, so the coefficient matrix is invertible.

**Conclusion.** The system has exactly one solution:

```math
(x,y)=(6,4).
```

**Verification.** We substitute into both equations: $`6+4=10`$ and $`2\cdot6+5\cdot4=12+20=32`$. Both equations hold.