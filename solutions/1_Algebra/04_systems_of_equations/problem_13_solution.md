# Exercise 13. Does Every Equation Add New Information?

## Question

Consider the system

```math
x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.
```

Solve it and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

> **Why this exercise:** teaches how to recognize redundant equations within a system.

## Solution

**Rule.** An equation is redundant if it can be obtained from the other equations by adding multiples of them. During elimination, a redundant equation becomes the row $`(0,0,0\mid 0)`$.

**Start.**

```math
\left(\begin{array}{ccc|c} 1 & 1 & 0 & 10 \\ 0 & 1 & 1 & 8 \\ 1 & 0 & -1 & 2 \end{array}\right).
```

**Step 1.** Replace $`R_3`$ by $`R_3 - R_1`$. Here $`(1,0,-1\mid 2) - (1,1,0\mid 10) = (0,-1,-1\mid -8)`$.

**Step 2.** Replace $`R_3`$ by $`R_3 + R_2`$. Here $`(0,-1,-1\mid -8) + (0,1,1\mid 8) = (0,0,0\mid 0)`$:

```math
\left(\begin{array}{ccc|c} 1 & 1 & 0 & 10 \\ 0 & 1 & 1 & 8 \\ 0 & 0 & 0 & 0 \end{array}\right).
```

**Step 3: Reading the solution.** The pivots are in columns $`1`$ and $`2`$, so $`x_3`$ is a free variable. We set $`x_3=t`$. The second row gives $`x_2=8-t`$. The first row gives $`x_1=10-x_2=2+t`$.

**Part 1: The redundant equation.** The zero row shows that the third equation follows from the other two. Indeed, subtracting the second equation from the first gives

```math
(x_1+x_2)-(x_2+x_3)=10-8 \quad\Longrightarrow\quad x_1-x_3=2,
```

which is exactly the third equation. So the third equation adds no new information: it is a consequence of the first two. The same relation can be written as $`x_1+x_2 = (x_2+x_3)+(x_1-x_3)`$, so any one of the three equations follows from the other two. The solution set is described by any two of the three equations, and only two are independently necessary.

**Conclusion.** The system has infinitely many solutions:

```math
(x_1,x_2,x_3)=(2+t,\ 8-t,\ t),\qquad t\in\mathbb{R}.
```

Not all three equations are independently necessary, because the third is the first minus the second.

**Verification.** We choose $`t=0`$, so $`(x_1,x_2,x_3)=(2,8,0)`$. We substitute it into all three original equations: $`2+8=10`$, $`8+0=8`$ and $`2-0=2`$. All three hold. We also check the general solution in the third equation: $`x_1-x_3=(2+t)-t=2`$.