# Exercise 4. Infinitely Many Solutions

## Question

Solve

```math
\begin{cases}
x+y+z=2, \\
2x+2y+2z=4, \\
x-y+z=0.
\end{cases}
```

Give the solution in parametric form, identify a free variable, and for one chosen parameter value check that the resulting point really satisfies the system.

> **Why this exercise:** shows the case of multiple solutions and teaches a simple parametric description.

## Solution

**Rule.** After elimination, columns with a pivot correspond to basic variables, and columns without a pivot correspond to free variables. If the system is consistent and there is at least one free variable, the system has infinitely many solutions. Each free variable is replaced by a parameter.

**Start.**

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 2 & 2 & 2 & 4 \\ 1 & -1 & 1 & 0 \end{array}\right).
```

**Step 1.** Replace $`R_2`$ by $`R_2 - 2R_1`$. Here $`(2,2,2\mid 4) - 2\cdot(1,1,1\mid 2) = (0,0,0\mid 0)`$:

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 0 & 0 & 0 & 0 \\ 1 & -1 & 1 & 0 \end{array}\right).
```

**Step 2.** Replace $`R_3`$ by $`R_3 - R_1`$. Here $`(1,-1,1\mid 0) - (1,1,1\mid 2) = (0,-2,0\mid -2)`$:

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 0 & 0 & 0 & 0 \\ 0 & -2 & 0 & -2 \end{array}\right).
```

**Step 3.** Swap $`R_2`$ and $`R_3`$, and then multiply the new $`R_2`$ by $`-\tfrac12`$:

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 2 \\ 0 & 1 & 0 & 1 \\ 0 & 0 & 0 & 0 \end{array}\right).
```

The last row is $`0=0`$, so there is no contradiction and the system is consistent.

**Step 4: Reading the solution.** The pivots are in columns $`1`$ and $`2`$, so $`x`$ and $`y`$ are basic variables. Column $`3`$ has no pivot, so $`z`$ is a free variable. We set $`z=t`$, where $`t`$ is any real number. The second row gives $`y=1`$. The first row gives $`x+y+z=2`$, so $`x=2-1-t=1-t`$.

**Conclusion.** The system has infinitely many solutions:

```math
(x,y,z)=(1-t,\ 1,\ t),\qquad t\in\mathbb{R},
```

with the free variable $`z=t`$.

**Verification.** We choose $`t=2`$. Then $`(x,y,z)=(-1,1,2)`$. We substitute it into all three original equations:

```math
\begin{aligned}
-1+1+2 &= 2, \\
2\cdot(-1)+2\cdot1+2\cdot2 &= -2+2+4=4, \\
-1-1+2 &= 0.
\end{aligned}
```

All three equations hold, so the point satisfies the system.