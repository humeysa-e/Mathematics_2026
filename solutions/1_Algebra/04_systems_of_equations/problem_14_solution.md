# Exercise 14. A Small Change in the Right-Hand Side

## Question

Compare the systems

```math
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3
\end{cases}
```

and

```math
\begin{cases}
x+y=2, \\
2x-y=1, \\
3x=3.1.
\end{cases}
```

Check the consistency of each system and explain why a small change in one number can change the type of the system.

> **Why this exercise:** shows the difference between a consistent and an inconsistent system without introducing new theory.

## Solution

**Rule.** A system is consistent if it has at least one solution. After elimination, a row $`(0,0\mid c)`$ with $`c\neq 0`$ means that the system is inconsistent.

**Part 1: The first system.** The augmented matrix is

```math
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 2 & -1 & 1 \\ 3 & 0 & 3 \end{array}\right).
```

Replace $`R_2`$ by $`R_2 - 2R_1`$ and $`R_3`$ by $`R_3 - 3R_1`$. Here $`(2,-1\mid 1) - 2\cdot(1,1\mid 2) = (0,-3\mid -3)`$ and $`(3,0\mid 3) - 3\cdot(1,1\mid 2) = (0,-3\mid -3)`$:

```math
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & -3 & -3 \\ 0 & -3 & -3 \end{array}\right).
```

Then replace $`R_3`$ by $`R_3 - R_2`$:

```math
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & -3 & -3 \\ 0 & 0 & 0 \end{array}\right).
```

The last row is $`0=0`$, so the system is consistent. The second row gives $`y=1`$, and the first row gives $`x=2-1=1`$. The solution is $`(x,y)=(1,1)`$.

**Part 2: The second system.** The first two equations are the same, so the same operations give

```math
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & -3 & -3 \\ 0 & -3 & -3.1 \end{array}\right)
\longrightarrow
\left(\begin{array}{cc|c} 1 & 1 & 2 \\ 0 & -3 & -3 \\ 0 & 0 & -0.1 \end{array}\right),
```

where the last step is $`R_3\leftarrow R_3-R_2`$, and $`(0,-3\mid -3.1)-(0,-3\mid -3)=(0,0\mid -0.1)`$. The last row says $`0=-0.1`$, which is a contradiction. The system is inconsistent and has no solution.

**Part 3: Why a small change matters.** In the first system the third equation is the sum of the first two: $`(x+y)+(2x-y)=3x`$ and $`2+1=3`$. So the third equation gives no new condition, and the three equations hold at the same time for the point $`(1,1)`$. In the second system the first two equations still force $`3x=3`$, but the third equation requires $`3x=3.1`$. These two requirements contradict each other. Geometrically, the three lines of the first system pass through the common point $`(1,1)`$. In the second system the third line is $`x=\tfrac{3.1}{3}\approx 1.033`$, which does not pass through $`(1,1)`$, so there is no point common to all three lines. The system has more equations than unknowns, so the right-hand sides must satisfy a consistency condition, and a small change can break it.

**Conclusion.** The first system is consistent with the unique solution $`(x,y)=(1,1)`$. The second system is inconsistent and has no solution. A small change in one number changed the type of the system because it broke the exact relation between the right-hand sides.

**Verification.** For the first system: $`1+1=2`$, $`2\cdot1-1=1`$ and $`3\cdot1=3`$. All three hold. For the second system, the first two equations give $`x=1`$, and then $`3x=3\neq 3.1`$, so the third equation fails.