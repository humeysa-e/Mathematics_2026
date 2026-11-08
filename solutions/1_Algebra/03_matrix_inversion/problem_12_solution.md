# Exercise 12. Finding Inverses Without Starting from Scratch

## Question

It is known that

```math
A^{-1}=\begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix}.
```

Without finding $`A`$, compute $`(3A)^{-1}`$, $`(A^T)^{-1}`$, and $`(A^2)^{-1}`$. Justify each result using the appropriate property.

> **Why this exercise:** teaches how to use inverse properties instead of carrying out unnecessary full calculations.

## Solution

**Properties.** For an invertible matrix $`A`$ and a nonzero number $`k`$:

1. $`(kA)^{-1} = \dfrac{1}{k}A^{-1}`$, because $`(kA)\left(\dfrac1k A^{-1}\right) = AA^{-1} = I`$;
2. $`(A^T)^{-1} = (A^{-1})^T`$, because $`A^T(A^{-1})^T = (A^{-1}A)^T = I^T = I`$;
3. $`(A^2)^{-1} = (A^{-1})^2`$, because $`(AA)(A^{-1}A^{-1}) = A(AA^{-1})A^{-1} = AA^{-1} = I`$.

**Part 1: $`(3A)^{-1}`$.** By property 1 with $`k=3`$,

```math
(3A)^{-1}=\frac13 A^{-1}=\frac13\begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix}=\begin{pmatrix} \frac23 & -\frac13 \\ -1 & \frac23 \end{pmatrix}.
```

**Part 2: $`(A^T)^{-1}`$.** By property 2 we transpose $`A^{-1}`$:

```math
(A^T)^{-1}=(A^{-1})^T=\begin{pmatrix} 2 & -3 \\ -1 & 2 \end{pmatrix}.
```

**Part 3: $`(A^2)^{-1}`$.** By property 3 we square $`A^{-1}`$:

```math
(A^2)^{-1}=(A^{-1})^2=\begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix}\begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix}=\begin{pmatrix} 2\cdot2+(-1)(-3) & 2\cdot(-1)+(-1)\cdot2 \\ (-3)\cdot2+2\cdot(-3) & (-3)(-1)+2\cdot2 \end{pmatrix}=\begin{pmatrix} 7 & -4 \\ -12 & 7 \end{pmatrix}.
```

**Conclusion.**

```math
(3A)^{-1}=\begin{pmatrix} \frac23 & -\frac13 \\ -1 & \frac23 \end{pmatrix},\qquad
(A^T)^{-1}=\begin{pmatrix} 2 & -3 \\ -1 & 2 \end{pmatrix},\qquad
(A^2)^{-1}=\begin{pmatrix} 7 & -4 \\ -12 & 7 \end{pmatrix}.
```

**Verification.** The solution above did not need $`A`$. Only to check the answers, we recover $`A`$ from $`A^{-1}`$. Since $`\det A^{-1} = 2\cdot2-(-1)(-3) = 1`$, the $`2\times2`$ formula gives

```math
A=\begin{pmatrix} 2 & 1 \\ 3 & 2 \end{pmatrix}.
```

Then $`3A=\begin{pmatrix} 6 & 3 \\ 9 & 6 \end{pmatrix}`$, $`A^T=\begin{pmatrix} 2 & 3 \\ 1 & 2 \end{pmatrix}`$ and $`A^2=\begin{pmatrix} 7 & 4 \\ 12 & 7 \end{pmatrix}`$. We multiply each matrix by the corresponding result:

```math
\begin{pmatrix} 6 & 3 \\ 9 & 6 \end{pmatrix}\begin{pmatrix} \frac23 & -\frac13 \\ -1 & \frac23 \end{pmatrix}=\begin{pmatrix} 4-3 & -2+2 \\ 6-6 & -3+4 \end{pmatrix}=I,
```

```math
\begin{pmatrix} 2 & 3 \\ 1 & 2 \end{pmatrix}\begin{pmatrix} 2 & -3 \\ -1 & 2 \end{pmatrix}=\begin{pmatrix} 4-3 & -6+6 \\ 2-2 & -3+4 \end{pmatrix}=I,
```

```math
\begin{pmatrix} 7 & 4 \\ 12 & 7 \end{pmatrix}\begin{pmatrix} 7 & -4 \\ -12 & 7 \end{pmatrix}=\begin{pmatrix} 49-48 & -28+28 \\ 84-84 & -48+49 \end{pmatrix}=I.
```

All three products are the identity matrix, so all three results are correct.