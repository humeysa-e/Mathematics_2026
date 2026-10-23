### Exercise 3. When Can Matrices Be Multiplied? - Solutions

**Given:**

$$
A_{2\times3},\qquad B_{3\times4},\qquad C_{4\times2},\qquad D_{2\times2}
$$

**Result:**

| Product | Inner dimensions | Defined? | Size of result |
|---|---|---|---|
| $AB$ | $3 = 3$ | Yes | $2\times4$ |
| $BA$ | $4 \neq 2$ | No | n/a |
| $BC$ | $4 = 4$ | Yes | $3\times2$ |
| $CB$ | $2 \neq 3$ | No | n/a |
| $AC$ | $3 \neq 4$ | No | n/a |
| $CA$ | $2 = 2$ | Yes | $4\times3$ |
| $AD$ | $3 \neq 2$ | No | n/a |
| $DA$ | $2 = 2$ | Yes | $2\times3$ |

**Main steps:**

For each product $XY$, write the sizes side by side, $(m\times n)(p\times q)$, and compare the inner numbers $n$ and $p$. If they are equal, the product is defined and has size $m\times q$.

**Property/method used:**

The product of an $m\times n$ matrix and a $p\times q$ matrix is defined only if $n=p$, and then the result is an $m\times q$ matrix. Each entry of $XY$ is the dot product of a row of $X$ with a column of $Y$, which needs both to have the same length.

**Verification:**

Check one defined case and one undefined case. For $AB$: a row of $A$ has 3 entries and a column of $B$ has 3 entries, so the dot product works, and there are 2 rows and 4 columns, giving $2\times4$. For $BA$: a row of $B$ has 4 entries but a column of $A$ has only 2 entries, so the dot product is impossible.