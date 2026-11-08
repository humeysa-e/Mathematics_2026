# Exercise 2. Gaussian Elimination — One Solution

## Question

Solve using Gaussian elimination:

```math
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2.
\end{cases}
```

After solving, substitute the result into all equations and check consistency.

> **Why this exercise:** introduces the basic method for solving a system and builds the habit of checking the result.

## Solution

**Method.** We write the augmented matrix $`[A\mid b]`$ and use row operations (swapping two rows, multiplying a row by a nonzero number, adding a multiple of one row to another row). These operations do not change the set of solutions. We reduce the matrix to row echelon form and then solve from the last equation upwards (back substitution).

**Start.**

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 2 & -1 & 1 & 3 \\ 1 & 2 & -1 & 2 \end{array}\right).
```

**Step 1.** Replace $`R_2`$ by $`R_2 - 2R_1`$. Here $`(2,-1,1\mid 3) - 2\cdot(1,1,1\mid 6) = (0,-3,-1\mid -9)`$:

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & -3 & -1 & -9 \\ 1 & 2 & -1 & 2 \end{array}\right).
```

**Step 2.** Replace $`R_3`$ by $`R_3 - R_1`$. Here $`(1,2,-1\mid 2) - (1,1,1\mid 6) = (0,1,-2\mid -4)`$:

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & -3 & -1 & -9 \\ 0 & 1 & -2 & -4 \end{array}\right).
```

**Step 3.** Swap $`R_2`$ and $`R_3`$, so that the second pivot is $`1`$:

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & 1 & -2 & -4 \\ 0 & -3 & -1 & -9 \end{array}\right).
```

**Step 4.** Replace $`R_3`$ by $`R_3 + 3R_2`$. Here $`(0,-3,-1\mid -9) + 3\cdot(0,1,-2\mid -4) = (0,0,-7\mid -21)`$:

```math
\left(\begin{array}{ccc|c} 1 & 1 & 1 & 6 \\ 0 & 1 & -2 & -4 \\ 0 & 0 & -7 & -21 \end{array}\right).
```

**Step 5: Back substitution.** The third row gives $`-7z=-21`$, so $`z=3`$. The second row gives $`y-2z=-4`$, so $`y=-4+2\cdot3=2`$. The first row gives $`x+y+z=6`$, so $`x=6-2-3=1`$.

**Conclusion.** The system has exactly one solution:

```math
(x,y,z)=(1,2,3).
```

**Verification.** We substitute $`x=1`$, $`y=2`$, $`z=3`$ into all three original equations:

```math
\begin{aligned}
1+2+3 &= 6, \\
2\cdot1-2+3 &= 3, \\
1+2\cdot2-3 &= 2.
\end{aligned}
```

All three equations hold, so the solution is consistent with the whole system.