# Exercise 11. A Parameter in a System of Three Equations

## Question

Analyze the number of solutions depending on $`t`$:

```math
\begin{cases}
x+y+z=1, \\
x+ty+z=2, \\
x+y+tz=3.
\end{cases}
```

Use elimination and separately analyze the parameter values for which a standard calculation step ceases to be valid.

> **Why this exercise:** develops parametric analysis while still relying only on elimination.

## Solution

**Rule.** After elimination, a row of the form $`(0,0,0\mid c)`$ with $`c\neq 0`$ means that the system has no solution. If the system is consistent, the number of free variables is the number of unknowns minus the number of pivots. Dividing a row by an expression with a parameter is allowed only when that expression is not zero.

**Start.**

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 1 \\ 1 & t & 1 & 2 \\ 1 & 1 & t & 3 \end{array}\right).
```

**Step 1.** Replace $`R_2`$ by $`R_2 - R_1`$. Here $`(1,t,1\mid 2) - (1,1,1\mid 1) = (0,t-1,0\mid 1)`$.

**Step 2.** Replace $`R_3`$ by $`R_3 - R_1`$. Here $`(1,1,t\mid 3) - (1,1,1\mid 1) = (0,0,t-1\mid 2)`$:

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 1 \\ 0 & t-1 & 0 & 1 \\ 0 & 0 & t-1 & 2 \end{array}\right).
```

**Part 1: The standard step and where it fails.** To solve for $`y`$ and $`z`$ we divide the second and third rows by $`t-1`$. This step is valid only when $`t-1\neq 0`$, that is, $`t\neq 1`$. The value $`t=1`$ must be analyzed separately.

**Part 2: The case $`t\neq 1`$.** The second row gives $`(t-1)y=1`$, so $`y=\dfrac{1}{t-1}`$. The third row gives $`(t-1)z=2`$, so $`z=\dfrac{2}{t-1}`$. The first row gives

```math
x=1-y-z=1-\frac{1}{t-1}-\frac{2}{t-1}=1-\frac{3}{t-1}=\frac{t-4}{t-1}.
```

There are three pivots and no free variables, so the system has exactly one solution.

**Part 3: The case $`t=1`$.** Then $`t-1=0`$, and the matrix becomes

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 1 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 0 & 2 \end{array}\right).
```

The second row says $`0=1`$, which is a contradiction. The system has no solution.

**Conclusion.**

- $`t\neq 1`$: exactly one solution, $`(x,y,z)=\left(\dfrac{t-4}{t-1},\ \dfrac{1}{t-1},\ \dfrac{2}{t-1}\right)`$;
- $`t=1`$: no solution;
- infinitely many solutions occur for no value of $`t`$.

**Verification.** For $`t=2`$ the formula gives $`(x,y,z)=(-2,1,2)`$. We substitute it into the original equations:

```math
\begin{aligned}
-2+1+2 &= 1, \\
-2+2\cdot1+2 &= 2, \\
-2+1+2\cdot2 &= 3.
\end{aligned}
```

All three equations hold. For $`t=1`$ the first two equations become $`x+y+z=1`$ and $`x+y+z=2`$, which contradict each other, in agreement with the result above.