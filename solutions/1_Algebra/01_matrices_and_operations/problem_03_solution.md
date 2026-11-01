# Exercise 3. When Can Matrices Be Multiplied?

## Question

The matrix sizes are

```math
A_{2\times3}, \qquad B_{3\times4}, \qquad C_{4\times2}, \qquad D_{2\times2}.
```

For the products

```math
AB, \quad BA, \quad BC, \quad CB, \quad AC, \quad CA, \quad AD, \quad DA
```

determine whether they are defined. If so, state the size of the result. Justify each decision using the dimension compatibility condition.

> **Why this exercise:** forces an understanding of dimension compatibility before carrying out any calculation.

## Solution

**Rule.** The product $`XY`$ of an $`m \times n`$ matrix $`X`$ and a $`p \times q`$ matrix $`Y`$ is defined only if $`n = p`$, that is, if the number of columns of $`X`$ equals the number of rows of $`Y`$. In that case the result has size $`m \times q`$. The reason is that each entry of $`XY`$ is the dot product of a row of $`X`$ (with $`n`$ entries) and a column of $`Y`$ (with $`p`$ entries), and a dot product needs both to have the same length.

For each product we write the sizes side by side, $`(m \times n)(p \times q)`$, and compare the inner numbers $`n`$ and $`p`$.

| Product | Sizes | Inner numbers | Defined? | Size of result |
|---|---|---|---|---|
| $`AB`$ | $`(2\times3)(3\times4)`$ | $`3 = 3`$ | Yes | $`2\times4`$ |
| $`BA`$ | $`(3\times4)(2\times3)`$ | $`4 \neq 2`$ | No | none |
| $`BC`$ | $`(3\times4)(4\times2)`$ | $`4 = 4`$ | Yes | $`3\times2`$ |
| $`CB`$ | $`(4\times2)(3\times4)`$ | $`2 \neq 3`$ | No | none |
| $`AC`$ | $`(2\times3)(4\times2)`$ | $`3 \neq 4`$ | No | none |
| $`CA`$ | $`(4\times2)(2\times3)`$ | $`2 = 2`$ | Yes | $`4\times3`$ |
| $`AD`$ | $`(2\times3)(2\times2)`$ | $`3 \neq 2`$ | No | none |
| $`DA`$ | $`(2\times2)(2\times3)`$ | $`2 = 2`$ | Yes | $`2\times3`$ |

**Justification of each decision.**

- $`AB`$: $`A`$ has 3 columns and $`B`$ has 3 rows, so the product is defined and has 2 rows and 4 columns.
- $`BA`$: $`B`$ has 4 columns but $`A`$ has only 2 rows, so the product is not defined.
- $`BC`$: $`B`$ has 4 columns and $`C`$ has 4 rows, so the product is defined and has 3 rows and 2 columns.
- $`CB`$: $`C`$ has 2 columns but $`B`$ has 3 rows, so the product is not defined.
- $`AC`$: $`A`$ has 3 columns but $`C`$ has 4 rows, so the product is not defined.
- $`CA`$: $`C`$ has 2 columns and $`A`$ has 2 rows, so the product is defined and has 4 rows and 3 columns.
- $`AD`$: $`A`$ has 3 columns but $`D`$ has 2 rows, so the product is not defined.
- $`DA`$: $`D`$ has 2 columns and $`A`$ has 2 rows, so the product is defined and has 2 rows and 3 columns.

**Verification.** We check one defined case and one undefined case. For $`AB`$, a row of $`A`$ has 3 entries and a column of $`B`$ has 3 entries, so the dot product works, and since $`A`$ has 2 rows and $`B`$ has 4 columns, the result is $`2\times4`$. For $`BA`$, a row of $`B`$ has 4 entries but a column of $`A`$ has only 2 entries, so the dot product is impossible.