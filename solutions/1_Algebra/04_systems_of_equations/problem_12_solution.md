# Exercise 12. Homogeneous System

## Question

Solve

```math
\begin{cases}
x+2y-z=0, \\
2x+4y-2z=0, \\
x-y+2z=0.
\end{cases}
```

Give all solutions in parametric form and explain why $`(0,0,0)`$ always satisfies a homogeneous system.

> **Why this exercise:** shows the special case of a system with a zero right-hand side without introducing additional theory.

## Solution

**Rule.** A system is called homogeneous if all right-hand sides are $`0`$, that is, if it has the form $`Ax=0`$. After elimination, columns without a pivot correspond to free variables, and each free variable is replaced by a parameter.

**Start.**

```math
\left(\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 2 & 4 & -2 & 0 \\ 1 & -1 & 2 & 0 \end{array}\right).
```

**Step 1.** Replace $`R_2`$ by $`R_2 - 2R_1`$. Here $`(2,4,-2\mid 0) - 2\cdot(1,2,-1\mid 0) = (0,0,0\mid 0)`$.

**Step 2.** Replace $`R_3`$ by $`R_3 - R_1`$. Here $`(1,-1,2\mid 0) - (1,2,-1\mid 0) = (0,-3,3\mid 0)`$:

```math
\left(\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & -3 & 3 & 0 \end{array}\right).
```

**Step 3.** Swap $`R_2`$ and $`R_3`$, and then multiply the new $`R_2`$ by $`-\tfrac13`$:

```math
\left(\begin{array}{ccc|c} 1 & 2 & -1 & 0 \\ 0 & 1 & -1 & 0 \\ 0 & 0 & 0 & 0 \end{array}\right).
```

**Step 4: Reading the solution.** The pivots are in columns $`1`$ and $`2`$, so $`x`$ and $`y`$ are basic variables and $`z`$ is a free variable. We set $`z=t`$. The second row gives $`y-z=0`$, so $`y=t`$. The first row gives $`x+2y-z=0`$, so $`x=-2t+t=-t`$.

**Why $`(0,0,0)`$ always satisfies a homogeneous system.** If we substitute $`x=0`$ into $`Ax=0`$, every entry of $`Ax`$ is a sum of products of coefficients with $`0`$, so $`A\cdot 0=0`$. Thus the zero vector satisfies every equation, whatever the matrix $`A`$ is. For this reason a homogeneous system is never inconsistent. In our solution the zero vector corresponds to $`t=0`$.

**Conclusion.** The system has infinitely many solutions:

```math
(x,y,z)=(-t,\ t,\ t),\qquad t\in\mathbb{R}.
```

**Verification.** We choose $`t=1`$, so $`(x,y,z)=(-1,1,1)`$. We substitute it into all three original equations:

```math
\begin{aligned}
-1+2\cdot1-1 &= 0, \\
2\cdot(-1)+4\cdot1-2\cdot1 &= -2+4-2=0, \\
-1-1+2\cdot1 &= 0.
\end{aligned}
```

All three equations hold.