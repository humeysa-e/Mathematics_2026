# Exercise 7. Inverse of a Product

## Question

For

```math
A=\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix},\qquad B=\begin{pmatrix} 2 & 0 \\ 0 & 3 \end{pmatrix}
```

compute $`(AB)^{-1}`$ and $`B^{-1}A^{-1}`$. Check that the results are the same and explain the meaning of the reversed order.

> **Why this exercise:** reinforces the inverse-of-a-product property and requires its interpretation.

## Solution

**Rule.** For a $`2 \times 2`$ matrix

```math
M=\begin{pmatrix} a & b \\ c & d \end{pmatrix}
```

with $`\det M = ad-bc \neq 0`$, the inverse is

```math
M^{-1}=\frac{1}{ad-bc}\begin{pmatrix} d & -b \\ -c & a \end{pmatrix}.
```

**Part 1: The product $`AB`$.**

```math
AB=\begin{pmatrix} 1\cdot2+1\cdot0 & 1\cdot0+1\cdot3 \\ 0\cdot2+1\cdot0 & 0\cdot0+1\cdot3 \end{pmatrix}=\begin{pmatrix} 2 & 3 \\ 0 & 3 \end{pmatrix}.
```

**Part 2: The inverse $`(AB)^{-1}`$.** Here $`\det(AB) = 2\cdot3 - 3\cdot0 = 6`$, so

```math
(AB)^{-1}=\frac16\begin{pmatrix} 3 & -3 \\ 0 & 2 \end{pmatrix}=\begin{pmatrix} \frac12 & -\frac12 \\ 0 & \frac13 \end{pmatrix}.
```

**Part 3: The inverses of $`A`$ and $`B`$.** We have $`\det A = 1`$ and $`\det B = 6`$, so

```math
A^{-1}=\begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix},\qquad B^{-1}=\begin{pmatrix} \frac12 & 0 \\ 0 & \frac13 \end{pmatrix}.
```

**Part 4: The product $`B^{-1}A^{-1}`$.**

```math
B^{-1}A^{-1}=\begin{pmatrix} \frac12\cdot1+0\cdot0 & \frac12\cdot(-1)+0\cdot1 \\ 0\cdot1+\frac13\cdot0 & 0\cdot(-1)+\frac13\cdot1 \end{pmatrix}=\begin{pmatrix} \frac12 & -\frac12 \\ 0 & \frac13 \end{pmatrix}.
```

**Conclusion.** The results are the same:

```math
(AB)^{-1}=B^{-1}A^{-1}=\begin{pmatrix} \frac12 & -\frac12 \\ 0 & \frac13 \end{pmatrix}.
```

**Meaning of the reversed order.** The product $`AB`$ means: first apply $`B`$, then apply $`A`$. To undo this, we must undo the last step first, so we first apply $`A^{-1}`$ and then $`B^{-1}`$. This is exactly the matrix $`B^{-1}A^{-1}`$. In general, $`(AB)^{-1}=B^{-1}A^{-1}`$, because

```math
(AB)(B^{-1}A^{-1}) = A(BB^{-1})A^{-1} = AIA^{-1} = AA^{-1} = I.
```

**Verification.** We check that the order really matters. The product in the wrong order is

```math
A^{-1}B^{-1}=\begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} \frac12 & 0 \\ 0 & \frac13 \end{pmatrix}=\begin{pmatrix} \frac12 & -\frac13 \\ 0 & \frac13 \end{pmatrix},
```

which is different from $`(AB)^{-1}`$ (the entry in row 1, column 2 is $`-\frac13`$ instead of $`-\frac12`$). We also check the correct one by multiplication:

```math
(AB)(AB)^{-1}=\begin{pmatrix} 2 & 3 \\ 0 & 3 \end{pmatrix}\begin{pmatrix} \frac12 & -\frac12 \\ 0 & \frac13 \end{pmatrix}=\begin{pmatrix} 1 & -1+1 \\ 0 & 1 \end{pmatrix}=\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}=I.
```