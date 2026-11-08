# Exercise 5. Row Echelon Form and Number of Solutions

## Question

For the augmented matrix

```math
\begin{pmatrix}
1 & 2 & -1 & \mid & 3 \\
0 & 1 & 2 & \mid & 1 \\
0 & 0 & 0 & \mid & 0 \\
\end{pmatrix}
```

determine the number of solutions and write them in parametric form. Explain how you know how many variables may be chosen freely.

> **Why this exercise:** teaches how to read information about solutions directly from row echelon form.

## Solution

**Rule.** For a system with $`n`$ unknowns in row echelon form:

- if there is a row $`(0,\dots,0\mid c)`$ with $`c\neq 0`$, the system has no solution;
- otherwise, the number of free variables is $`n`$ minus the number of pivots (nonzero rows). If this number is $`0`$ the solution is unique, and if it is positive there are infinitely many solutions.

**Part 1: The system.** The matrix has three unknowns, $`x`$, $`y`$, $`z`$. Its rows represent the equations

```math
\begin{cases}
x+2y-z=3, \\
y+2z=1, \\
0=0.
\end{cases}
```

**Part 2: Consistency and the number of free variables.** The last row is $`0=0`$, which is always true, so there is no contradiction and the system is consistent. There are two nonzero rows, so there are two pivots (in columns $`1`$ and $`2`$). The number of free variables is $`3-2=1`$. The column of $`z`$ has no pivot, so $`z`$ is the free variable, and the system has infinitely many solutions.

**Part 3: The parametric form.** We set $`z=t`$. The second equation gives

```math
y=1-2z=1-2t.
```

The first equation gives

```math
x=3-2y+z=3-2(1-2t)+t=3-2+4t+t=1+5t.
```

**Conclusion.** The system has infinitely many solutions:

```math
(x,y,z)=(1+5t,\ 1-2t,\ t),\qquad t\in\mathbb{R}.
```

Exactly one variable can be chosen freely, because there are $`3`$ unknowns and only $`2`$ pivots.

**Verification.** We choose $`t=1`$. Then $`(x,y,z)=(6,-1,1)`$. We substitute it into the equations of the matrix:

```math
\begin{aligned}
6+2\cdot(-1)-1 &= 3, \\
-1+2\cdot1 &= 1.
\end{aligned}
```

Both equations hold, and the third equation $`0=0`$ holds automatically. So the point satisfies the system.