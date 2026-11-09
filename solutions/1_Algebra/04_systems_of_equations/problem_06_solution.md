# Exercise 6. A System with a Parameter — Which Cases Actually Occur?

## Question

Analyze, depending on the parameter $`a`$, the system

```math
\begin{cases}
x+y=2, \\
ax+ay=4.
\end{cases}
```

Among the three possibilities — exactly one solution, infinitely many solutions, no solution — determine which actually occur and for which values of $`a`$. If one type cannot occur, explain why.

> **Why this exercise:** teaches how to analyze a parameter without assuming in advance that all theoretically possible cases must occur in a specific system.

## Solution

**Rule.** After elimination, a row of the form $`(0,0\mid c)`$ with $`c\neq 0`$ means that the system has no solution. If the system is consistent, then the number of free variables is the number of unknowns minus the number of pivots. A positive number of free variables means infinitely many solutions.

**Part 1: Elimination.** The augmented matrix is

```math
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ a & a & 4 \end{array}\right).
```

Replace $`R_2`$ by $`R_2 - aR_1`$. Here $`(a,a\mid 4) - a\cdot(1,1\mid 2) = (0,0\mid 4-2a)`$:

```math
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 0 & 4-2a \end{array}\right).
```

**Part 2: The case $`a\neq 2`$.** Then $`4-2a\neq 0`$, and the second row says $`0 = 4-2a`$, which is a contradiction. The system has no solution.

**Part 3: The case $`a=2`$.** Then $`4-2a=0`$, and the second row is $`0=0`$. The system is consistent and has only one pivot, so there is $`2-1=1`$ free variable. We set $`y=t`$, and the first equation gives $`x=2-t`$. The system has infinitely many solutions:

```math
(x,y)=(2-t,\ t),\qquad t\in\mathbb{R}.
```

**Part 4: Why exactly one solution never occurs.** The second row of the coefficient matrix, $`(a,a)`$, is $`a`$ times the first row $`(1,1)`$, for every value of $`a`$. So after elimination the second row of the coefficient part is always $`(0,0)`$, there is at most one pivot, and the second unknown is always free (when the system is consistent). Equivalently, $`\det\begin{pmatrix} 1 & 1 \\ a & a \end{pmatrix} = a - a = 0`$ for every $`a`$, so the coefficient matrix is never invertible.

**Conclusion.**

- $`a\neq 2`$: no solution;
- $`a=2`$: infinitely many solutions, $`(x,y)=(2-t,\ t)`$;
- exactly one solution occurs for no value of $`a`$.

**Verification.** For $`a=2`$ take $`t=1`$, so $`(x,y)=(1,1)`$: $`1+1=2`$ and $`2\cdot1+2\cdot1=4`$. Take $`t=2`$, so $`(x,y)=(0,2)`$: $`0+2=2`$ and $`2\cdot0+2\cdot2=4`$. Both points satisfy the system. For $`a=1`$ the equations are $`x+y=2`$ and $`x+y=4`$, which contradict each other, in agreement with $`4-2a=2\neq 0`$.