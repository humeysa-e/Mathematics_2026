# Exercise 14. A Matrix That Is Its Own Inverse

## Question

Assume that a square matrix $`A`$ satisfies

```math
A^2=I.
```

Show that

```math
A^{-1}=A.
```

Then give an example of a $`2\times 2`$ matrix different from $`I`$ and $`-I`$ that satisfies this condition, and verify it by multiplication.

> **Why this exercise:** requires using the definition of the inverse in a short argument and constructing an example independently, without introducing a new topic.

## Solution

**Definition.** A square matrix $`B`$ is the inverse of a square matrix $`A`$ if $`AB = I`$ and $`BA = I`$. In that case we write $`B = A^{-1}`$.

**Part 1: The proof.** Assume $`A^2 = I`$, that is, $`A\cdot A = I`$. Take $`B = A`$. Then

```math
AB = A\cdot A = I \qquad\text{and}\qquad BA = A\cdot A = I.
```

Both conditions of the definition hold for $`B=A`$, so $`A`$ is invertible and $`A^{-1} = A`$.

**Part 2: An example.** We look for a $`2\times 2`$ matrix with $`A^2=I`$ that is neither $`I`$ nor $`-I`$. Take

```math
A=\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}.
```

This matrix swaps the two coordinates of a vector. It is different from $`I`$ and from $`-I`$.

**Part 3: Verification of the example.**

```math
A^2=\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}=\begin{pmatrix} 0\cdot0+1\cdot1 & 0\cdot1+1\cdot0 \\ 1\cdot0+0\cdot1 & 1\cdot1+0\cdot0 \end{pmatrix}=\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}=I.
```

**Conclusion.** If $`A^2=I`$, then $`A^{-1}=A`$. The matrix $`A=\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}`$ is an example different from $`I`$ and $`-I`$.

**Verification.** We check the statement $`A^{-1}=A`$ for this example with the $`2\times2`$ formula. Here $`\det A = 0\cdot0 - 1\cdot1 = -1`$, so

```math
A^{-1}=\frac{1}{-1}\begin{pmatrix} 0 & -1 \\ -1 & 0 \end{pmatrix}=\begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}=A.
```

The inverse computed by the formula is equal to $`A`$, as the proof says.