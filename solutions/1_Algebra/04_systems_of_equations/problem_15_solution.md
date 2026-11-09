# Exercise 15. Classifying Three Systems

## Question

For each of the following systems, perform only as much elimination as necessary to recognize its type:

**System 1**

```math
\begin{cases}
x+y=2, \\
x-y=0,
\end{cases}
```

**System 2**

```math
\begin{cases}
x+y=2, \\
2x+2y=4,
\end{cases}
```

**System 3**

```math
\begin{cases}
x+y=2, \\
2x+2y=5.
\end{cases}
```

For each, justify the classification: one solution, infinitely many solutions, or no solution.

> **Why this exercise:** brings together the three basic cases and requires recognizing them from the structure after elimination.

## Solution

**Rule.** After one elimination step on a system of two equations in two unknowns:

- two pivots mean exactly one solution;
- one pivot and a last row $`(0,0\mid 0)`$ mean infinitely many solutions;
- a last row $`(0,0\mid c)`$ with $`c\neq 0`$ means no solution.

**System 1.** Replace $`R_2`$ by $`R_2 - R_1`$. Here $`(1,-1\mid 0) - (1,1\mid 2) = (0,-2\mid -2)`$:

```math
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & -2 & -2 \end{array}\right).
```

There are two pivots, so the system has **exactly one solution**. The second row gives $`y=1`$, and the first row gives $`x=1`$.

**System 2.** Replace $`R_2`$ by $`R_2 - 2R_1`$. Here $`(2,2\mid 4) - 2\cdot(1,1\mid 2) = (0,0\mid 0)`$:

```math
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 0 & 0 \end{array}\right).
```

There is one pivot and the last row is $`0=0`$, so the system is consistent with one free variable. It has **infinitely many solutions**: with $`y=t`$ we get $`(x,y)=(2-t,\ t)`$.

**System 3.** Replace $`R_2`$ by $`R_2 - 2R_1`$. Here $`(2,2\mid 5) - 2\cdot(1,1\mid 2) = (0,0\mid 1)`$:

```math
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & 0 & 1 \end{array}\right).
```

The last row says $`0=1`$, which is a contradiction. The system has **no solution**.

**Conclusion.**

- System 1: exactly one solution, $`(x,y)=(1,1)`$;
- System 2: infinitely many solutions, $`(x,y)=(2-t,\ t)`$;
- System 3: no solution.

**Verification.** For System 1: $`1+1=2`$ and $`1-1=0`$. For System 2, take $`t=0`$, so $`(x,y)=(2,0)`$: $`2+0=2`$ and $`2\cdot2+0=4`$. For System 3, the left side of the second equation is twice the left side of the first, so $`2x+2y=2\cdot2=4`$ whenever $`x+y=2`$. This is never equal to $`5`$, which agrees with the result.