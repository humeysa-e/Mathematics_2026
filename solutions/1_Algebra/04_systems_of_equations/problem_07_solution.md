# Exercise 7. Choosing a Method Deliberately

## Question

Do not solve all of the following systems completely. For each situation, choose the method that best uses its structure and justify your choice:

1. one system with a triangular coefficient matrix

```math
\begin{cases}
2x-y=3, \\
4y=8;
\end{cases}
```

2. three systems $`Ax=b_i`$ with the same invertible matrix $`A`$, when $`A^{-1}`$ is already known;
3. one $`3\times 3`$ system for which the inverse matrix is not given and the goal is only to find one solution vector.

For case 1, carry out the chosen method completely. For cases 2 and 3, describe the plan and indicate which part of the computation would be reusable or unnecessary. Do not judge a method by its name alone — refer to the number of right-hand sides and the structure of the matrix.

> **Why this exercise:** practices choosing a method based on the structure of the problem instead of solving another small system by two methods.

## Solution

**Principle.** The best method depends on the structure of the matrix and on the number of right-hand sides. Work that depends only on the matrix $`A`$ can be reused for several right-hand sides, and work that is not needed for the goal should be skipped.

**Case 1: A triangular system.** The coefficient matrix is already upper triangular, so no elimination is needed. The best method is back substitution, starting from the last equation.

The second equation gives $`4y=8`$, so $`y=2`$. The first equation gives $`2x-y=3`$, so $`2x=3+2=5`$ and $`x=\dfrac52`$.

The solution is $`(x,y)=\left(\dfrac52,\ 2\right)`$. Computing an inverse or running elimination would only repeat work that the triangular structure has already done.

**Case 2: Three right-hand sides and a known inverse.** The inverse $`A^{-1}`$ is already known, so the expensive part of the work is done. The plan is to compute

```math
x_i = A^{-1}b_i,\qquad i=1,2,3,
```

that is, three matrix–vector products (or one product $`A^{-1}B`$, where the columns of $`B`$ are $`b_1,b_2,b_3`$). The reusable part is $`A^{-1}`$, which serves all three systems. The unnecessary part is any new elimination: repeating Gaussian elimination three times would redo work that depends only on $`A`$.

**Case 3: One $`3\times 3`$ system, no inverse given.** There is only one right-hand side and we need only one solution vector. The plan is Gaussian elimination on the augmented matrix $`[A\mid b]`$, followed by back substitution. Computing $`A^{-1}`$ is unnecessary here: it would require reducing a matrix with three extra columns, $`[A\mid I]`$, instead of one column $`b`$, and then still multiplying $`A^{-1}b`$. Nothing from that extra work would be reused, because there is no second right-hand side.

**Conclusion.**

- Case 1: back substitution, with solution $`(x,y)=\left(\tfrac52,\ 2\right)`$.
- Case 2: use the known inverse, $`x_i=A^{-1}b_i`$; the reusable part is $`A^{-1}`$, and repeated elimination is unnecessary.
- Case 3: Gaussian elimination on $`[A\mid b]`$; finding the inverse is unnecessary.

**Verification.** We check case 1 by substituting $`x=\tfrac52`$, $`y=2`$ into both equations: $`2\cdot\tfrac52-2=5-2=3`$ and $`4\cdot2=8`$. Both equations hold.