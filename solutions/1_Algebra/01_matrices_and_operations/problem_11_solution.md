# Exercise 11. When Do Matrices Commute?

## Question

Given

```math
A=\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}, \qquad B=\begin{pmatrix} a & b \\ c & d \end{pmatrix}.
```

Find the conditions on $`a,b,c,d`$ under which $`AB=BA`$. Describe the general form of all such matrices $`B`$.

> **Why this exercise:** deepens the idea of noncommutativity by finding the conditions under which commutativity does hold.

## Solution

**Rule.** Two matrices are equal only if all their corresponding entries are equal. So we compute $`AB`$ and $`BA`$ for the general matrix $`B`$, and then compare the four entries one by one. Both products are defined and are $`2 \times 2`$ matrices.

**Part 1: The product $`AB`$.** We multiply rows of $`A`$ by columns of $`B`$:

```math
AB=\begin{pmatrix} 1\cdot a+1\cdot c & 1\cdot b+1\cdot d \\ 0\cdot a+1\cdot c & 0\cdot b+1\cdot d \end{pmatrix}=\begin{pmatrix} a+c & b+d \\ c & d \end{pmatrix}.
```

**Part 2: The product $`BA`$.** We multiply rows of $`B`$ by columns of $`A`$:

```math
BA=\begin{pmatrix} a\cdot1+b\cdot0 & a\cdot1+b\cdot1 \\ c\cdot1+d\cdot0 & c\cdot1+d\cdot1 \end{pmatrix}=\begin{pmatrix} a & a+b \\ c & c+d \end{pmatrix}.
```

**Part 3: Comparing the entries.** The condition $`AB=BA`$ means that all four entries are equal:

- Row 1, column 1: $`a+c=a`$, so $`c=0`$.
- Row 1, column 2: $`b+d=a+b`$, so $`d=a`$.
- Row 2, column 1: $`c=c`$, which is always true.
- Row 2, column 2: $`d=c+d`$, so $`c=0`$.

The second and fourth conditions do not give anything new beyond $`c=0`$ and $`d=a`$. So $`AB=BA`$ holds exactly when

```math
c=0 \quad \text{and} \quad d=a,
```

while $`a`$ and $`b`$ can be any numbers.

**Part 4: The general form of $`B`$.** Substituting $`c=0`$ and $`d=a`$ into $`B`$, we get

```math
B=\begin{pmatrix} a & b \\ 0 & a \end{pmatrix}, \qquad a,b \in \mathbb{R}.
```

Such a matrix can also be written as $`B=aI+bN`$, where $`N=\begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}`$. Since $`A=I+N`$, the matrices that commute with $`A`$ are exactly the matrices built from $`I`$ and $`N`$ in this way.

**Verification.** We check that every matrix of this form really commutes with $`A`$:

```math
AB=\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} a & b \\ 0 & a \end{pmatrix}=\begin{pmatrix} a & a+b \\ 0 & a \end{pmatrix}, \qquad BA=\begin{pmatrix} a & b \\ 0 & a \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}=\begin{pmatrix} a & a+b \\ 0 & a \end{pmatrix}.
```

The two products are equal, so the condition is also sufficient. For example, $`B=\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}`$ ($`a=1,\ b=0`$) commutes with $`A`$, but $`B=\begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}`$ does not ($`c=3\neq0`$).