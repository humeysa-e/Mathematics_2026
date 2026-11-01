# Exercise 13. A Recurrence Written in Matrix Form

## Question

Let

```math
F=\begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix}.
```

Compute $`F^2`$, $`F^3`$, $`F^4`$, and $`F^5`$. Compare the numbers obtained with the sequence

```math
0,1,1,2,3,5,8,\ldots
```

and describe the relationship you observe. Then compute

```math
F\begin{pmatrix} a \\ b \end{pmatrix}
```

and explain how this multiplication performs one recurrence step: it creates the sum of two consecutive terms and keeps one of them for the next step.

> **Why this exercise:** shows the connection between matrix powers and a simple numerical recurrence.

## Solution

**Rule.** The power $`F^n`$ means multiplying $`F`$ by itself $`n`$ times, so $`F^{k+1}=F^kF`$. We denote the terms of the sequence by $`F_0=0,\ F_1=1,\ F_2=1,\ F_3=2,\ F_4=3,\ F_5=5,\ F_6=8,\ldots`$, where each term is the sum of the two previous ones, $`F_{k+1}=F_k+F_{k-1}`$.

**Part 1: Computing the powers.** We multiply rows by columns:

```math
F^2=FF=\begin{pmatrix} 1\cdot1+1\cdot1 & 1\cdot1+1\cdot0 \\ 1\cdot1+0\cdot1 & 1\cdot1+0\cdot0 \end{pmatrix}=\begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix},
```

```math
F^3=F^2F=\begin{pmatrix} 2\cdot1+1\cdot1 & 2\cdot1+1\cdot0 \\ 1\cdot1+1\cdot1 & 1\cdot1+1\cdot0 \end{pmatrix}=\begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix},
```

```math
F^4=F^3F=\begin{pmatrix} 3\cdot1+2\cdot1 & 3\cdot1+2\cdot0 \\ 2\cdot1+1\cdot1 & 2\cdot1+1\cdot0 \end{pmatrix}=\begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix},
```

```math
F^5=F^4F=\begin{pmatrix} 5\cdot1+3\cdot1 & 5\cdot1+3\cdot0 \\ 3\cdot1+2\cdot1 & 3\cdot1+2\cdot0 \end{pmatrix}=\begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}.
```

**Part 2: Comparison with the sequence.** The entries of the powers are exactly the numbers $`0,1,1,2,3,5,8`$ of the sequence. For example, $`F^5`$ contains $`8=F_6`$, $`5=F_5`$ and $`3=F_4`$. The same pattern holds for the other powers we computed, and also for $`F^1=F`$, so we observe

```math
F^n=\begin{pmatrix} F_{n+1} & F_n \\ F_n & F_{n-1} \end{pmatrix}, \qquad n=1,2,3,4,5.
```

In this exercise we observed this relationship for $`n=1,\ldots,5`$ only, and we did not prove it for all $`n`$.

**Part 3: One recurrence step.** We multiply $`F`$ by a vector $`(a,b)^T`$:

```math
F\begin{pmatrix} a \\ b \end{pmatrix}=\begin{pmatrix} 1\cdot a+1\cdot b \\ 1\cdot a+0\cdot b \end{pmatrix}=\begin{pmatrix} a+b \\ a \end{pmatrix}.
```

The first entry is the sum $`a+b`$ of the two numbers, and the second entry is $`a`$, one of the old numbers kept for the next step. If the vector contains two consecutive terms, $`a=F_{k+1}`$ and $`b=F_k`$, then

```math
F\begin{pmatrix} F_{k+1} \\ F_k \end{pmatrix}=\begin{pmatrix} F_{k+1}+F_k \\ F_{k+1} \end{pmatrix}=\begin{pmatrix} F_{k+2} \\ F_{k+1} \end{pmatrix}.
```

So one multiplication by $`F`$ moves the pair of consecutive terms one step forward in the sequence. Repeating it $`n`$ times means multiplying by $`F^n`$, which is why the powers of $`F`$ contain the numbers of the sequence.

**Verification.** We compute $`F^5`$ in a different way, as $`F^2F^3`$:

```math
F^2F^3=\begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}\begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}=\begin{pmatrix} 2\cdot3+1\cdot2 & 2\cdot2+1\cdot1 \\ 1\cdot3+1\cdot2 & 1\cdot2+1\cdot1 \end{pmatrix}=\begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}.
```

This matches $`F^4F`$ from Part 1.