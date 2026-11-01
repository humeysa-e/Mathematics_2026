# Exercise 12. Formula for a Matrix Power

## Question

Let

```math
A=\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}.
```

Compute $`A^2`$, $`A^3`$, and $`A^4`$, and use them to formulate a conjecture for $`A^n`$. Then do not stop after checking one more case: assume the formula is true for $`n`$, multiply by $`A`$, and explain why you obtain exactly the formula for $`n+1`$.

> **Why this exercise:** teaches how to recognize a pattern and formulate a generalization from several computations.

## Solution

**Rule.** The power $`A^n`$ means multiplying $`A`$ by itself $`n`$ times, so $`A^{k+1}=A^kA`$. We compute the first powers by multiplying rows by columns, look for a pattern, and then justify the pattern for all $`n`$.

**Part 1: Computing $`A^2`$, $`A^3`$, and $`A^4`$.** First,

```math
A^2=AA=\begin{pmatrix} 1\cdot1+1\cdot0 & 1\cdot1+1\cdot1 \\ 0\cdot1+1\cdot0 & 0\cdot1+1\cdot1 \end{pmatrix}=\begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}.
```

Then we multiply by $`A`$ again:

```math
A^3=A^2A=\begin{pmatrix} 1\cdot1+2\cdot0 & 1\cdot1+2\cdot1 \\ 0\cdot1+1\cdot0 & 0\cdot1+1\cdot1 \end{pmatrix}=\begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix},
```

```math
A^4=A^3A=\begin{pmatrix} 1\cdot1+3\cdot0 & 1\cdot1+3\cdot1 \\ 0\cdot1+1\cdot0 & 0\cdot1+1\cdot1 \end{pmatrix}=\begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}.
```

**Part 2: The conjecture.** Together with $`A^1=A`$, the results are

```math
A^1=\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}, \quad A^2=\begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}, \quad A^3=\begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}, \quad A^4=\begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}.
```

The diagonal entries stay $`1`$, the lower left entry stays $`0`$, and the upper right entry equals the exponent. So we conjecture that for every positive integer $`n`$

```math
A^n=\begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}.
```

**Part 3: Why the formula passes from $`n`$ to $`n+1`$.** Assume that the formula is true for some $`n`$, that is, $`A^n=\begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}`$. Since $`A^{n+1}=A^nA`$, we get

```math
A^{n+1}=A^nA=\begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}=\begin{pmatrix} 1\cdot1+n\cdot0 & 1\cdot1+n\cdot1 \\ 0\cdot1+1\cdot0 & 0\cdot1+1\cdot1 \end{pmatrix}=\begin{pmatrix} 1 & n+1 \\ 0 & 1 \end{pmatrix}.
```

This is exactly the formula for $`n+1`$: the only entry that changes is the upper right one, and it changes from $`n`$ to $`n+1`$, because multiplying by $`A`$ adds the $`1`$ from the lower right entry of $`A^n`$ to the upper right entry.

**Conclusion.** The formula is true for $`n=1`$ (it gives $`A`$), and whenever it is true for $`n`$, it is also true for $`n+1`$. Therefore, by induction, it is true for all positive integers $`n`$:

```math
A^n=\begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}.
```

**Verification.** For $`n=4`$ the formula gives $`\begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}`$, which matches $`A^4`$ computed in Part 1. We can also check $`A^4`$ in a different way as $`A^2A^2`$: the upper right entry is $`1\cdot2+2\cdot1=4`$, and the other entries are $`1`$, $`0`$, $`1`$.