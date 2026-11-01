# Exercise 7. Identity Matrix, Zero Matrix, and Powers

## Question

For

```math
A=\begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}
```

compute

```math
AI, \qquad IA, \qquad A+0, \qquad A^2, \qquad A^3.
```

Explain the roles of the matrices $`I`$ and $`0`$, and describe the pattern you observe in successive powers of $`A`$.

> **Why this exercise:** organizes the roles of neutral elements and reveals regularity in successive powers of a matrix.

## Solution

**Rule.** The identity matrix $`I`$ has $`1`$ on the main diagonal and $`0`$ elsewhere, and the zero matrix $`0`$ has all entries equal to $`0`$. Since $`A`$ is $`2 \times 2`$, we use the $`2 \times 2`$ versions:

```math
I=\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}, \qquad 0=\begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}.
```

The power $`A^n`$ means multiplying $`A`$ by itself $`n`$ times, so $`A^2=AA`$ and $`A^3=A^2A`$.

**Part 1: The products $`AI`$ and $`IA`$.** We multiply rows by columns:

```math
AI=\begin{pmatrix} 2\cdot1+1\cdot0 & 2\cdot0+1\cdot1 \\ 0\cdot1+2\cdot0 & 0\cdot0+2\cdot1 \end{pmatrix}=\begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}=A,
```

```math
IA=\begin{pmatrix} 1\cdot2+0\cdot0 & 1\cdot1+0\cdot2 \\ 0\cdot2+1\cdot0 & 0\cdot1+1\cdot2 \end{pmatrix}=\begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}=A.
```

**Part 2: The sum $`A+0`$.** Adding the zero matrix adds $`0`$ to every entry:

```math
A+0=\begin{pmatrix} 2+0 & 1+0 \\ 0+0 & 2+0 \end{pmatrix}=\begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}=A.
```

**Part 3: The power $`A^2`$.**

```math
A^2=AA=\begin{pmatrix} 2\cdot2+1\cdot0 & 2\cdot1+1\cdot2 \\ 0\cdot2+2\cdot0 & 0\cdot1+2\cdot2 \end{pmatrix}=\begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}.
```

**Part 4: The power $`A^3`$.** We multiply $`A^2`$ by $`A`$:

```math
A^3=A^2A=\begin{pmatrix} 4\cdot2+4\cdot0 & 4\cdot1+4\cdot2 \\ 0\cdot2+4\cdot0 & 0\cdot1+4\cdot2 \end{pmatrix}=\begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}.
```

**Part 5: The roles of $`I`$ and $`0`$.** Parts 1 and 2 show that $`AI=IA=A`$ and $`A+0=A`$. The identity matrix $`I`$ is the neutral element for matrix multiplication, like the number $`1`$ for numbers, because multiplying by it does not change the matrix. The zero matrix $`0`$ is the neutral element for matrix addition, like the number $`0`$ for numbers, because adding it does not change the matrix.

**Part 6: The pattern in the powers.** We list the results:

```math
A^1=\begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}, \qquad A^2=\begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}, \qquad A^3=\begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}.
```

The diagonal entries are $`2, 4, 8`$, that is, $`2^n`$. The entry in the lower left corner stays $`0`$. The entry in the upper right corner is $`1, 4, 12`$, which equals $`n\cdot2^{n-1}`$ for $`n=1,2,3`$. This suggests the pattern

```math
A^n=\begin{pmatrix} 2^n & n\cdot2^{n-1} \\ 0 & 2^n \end{pmatrix}.
```

In this exercise we observed the pattern for $`n=1,2,3`$ only, and we did not prove it for all $`n`$.

**Verification.** We compute $`A^3`$ in a different order, as $`AA^2`$:

```math
AA^2=\begin{pmatrix} 2\cdot4+1\cdot0 & 2\cdot4+1\cdot4 \\ 0\cdot4+2\cdot0 & 0\cdot4+2\cdot4 \end{pmatrix}=\begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}.
```

This matches $`A^2A`$ from Part 4.