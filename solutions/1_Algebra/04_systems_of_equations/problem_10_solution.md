# Exercise 10. A Polynomial Through Three Points

## Question

Find a polynomial $`p(x)=ax^2+bx+c`$ whose graph passes through $`(0,1)`$, $`(1,3)`$, and $`(2,9)`$. Reduce the problem to a system of equations and check the result by substituting all three points.

> **Why this exercise:** shows that finding unknown coefficients can be reduced to solving a linear system.

## Solution

**Method.** The graph passes through a point $`(x_0,y_0)`$ exactly when $`p(x_0)=y_0`$. Each point gives one linear equation in the unknowns $`a`$, $`b`$, $`c`$.

**Part 1: The system.** We substitute the three points into $`p(x)=ax^2+bx+c`$:

```math
\begin{aligned}
p(0)=1 &:\quad c = 1, \\
p(1)=3 &:\quad a+b+c = 3, \\
p(2)=9 &:\quad 4a+2b+c = 9.
\end{aligned}
```

**Part 2: Elimination.** The augmented matrix for the unknowns $`(a,b,c)`$ is

```math
\left(\begin{array}{ccc|c} 0 & 0 & 1 & 1 \\ 1 & 1 & 1 & 3 \\ 4 & 2 & 1 & 9 \end{array}\right).
```

Step 1: swap $`R_1`$ and $`R_2`$:

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 3 \\ 0 & 0 & 1 & 1 \\ 4 & 2 & 1 & 9 \end{array}\right).
```

Step 2: replace $`R_3`$ by $`R_3 - 4R_1`$. Here $`(4,2,1\mid 9) - 4\cdot(1,1,1\mid 3) = (0,-2,-3\mid -3)`$:

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 3 \\ 0 & 0 & 1 & 1 \\ 0 & -2 & -3 & -3 \end{array}\right).
```

Step 3: swap $`R_2`$ and $`R_3`$:

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 3 \\ 0 & -2 & -3 & -3 \\ 0 & 0 & 1 & 1 \end{array}\right).
```

**Part 3: Back substitution.** The third row gives $`c=1`$. The second row gives $`-2b-3c=-3`$, so $`-2b=-3+3=0`$ and $`b=0`$. The first row gives $`a+b+c=3`$, so $`a=3-0-1=2`$.

**Conclusion.** The polynomial is

```math
p(x)=2x^2+1.
```

**Verification.** We substitute all three points:

```math
\begin{aligned}
p(0) &= 2\cdot0^2+1 = 1, \\
p(1) &= 2\cdot1^2+1 = 3, \\
p(2) &= 2\cdot2^2+1 = 9.
\end{aligned}
```

All three values agree with the given points.