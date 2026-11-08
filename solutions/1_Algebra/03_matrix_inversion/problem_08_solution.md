# Exercise 8. Inverse of a Transformation

## Question

The matrix

```math
S=\begin{pmatrix} 2 & 0 \\ 0 & \frac12 \end{pmatrix}
```

describes a scaling of the plane. Find $`S^{-1}`$ and explain geometrically what the inverse transformation does. Check the action of the pair $`S,S^{-1}`$ on one simple vector.

> **Why this exercise:** gives the inverse the interpretation of undoing a transformation.

## Solution

**Rule.** For a $`2 \times 2`$ matrix

```math
M=\begin{pmatrix} a & b \\ c & d \end{pmatrix}
```

with $`\det M = ad-bc \neq 0`$, the inverse is

```math
M^{-1}=\frac{1}{ad-bc}\begin{pmatrix} d & -b \\ -c & a \end{pmatrix}.
```

**Part 1: The inverse.** Here $`\det S = 2\cdot\frac12 - 0\cdot 0 = 1 \neq 0`$, so $`S`$ is invertible and

```math
S^{-1}=\frac{1}{1}\begin{pmatrix} \frac12 & 0 \\ 0 & 2 \end{pmatrix}=\begin{pmatrix} \frac12 & 0 \\ 0 & 2 \end{pmatrix}.
```

**Part 2: The geometric meaning.** The matrix $`S`$ sends $`(x,y)`$ to $`(2x,\ \tfrac12 y)`$. It stretches the plane by the factor $`2`$ in the $`x`$ direction and shrinks it by the factor $`\tfrac12`$ in the $`y`$ direction. The inverse $`S^{-1}`$ sends $`(x,y)`$ to $`(\tfrac12 x,\ 2y)`$. It shrinks the plane by the factor $`\tfrac12`$ in the $`x`$ direction and stretches it by the factor $`2`$ in the $`y`$ direction, so it undoes the scaling done by $`S`$ and returns every point to its original position.

**Conclusion.**

```math
S^{-1}=\begin{pmatrix} \frac12 & 0 \\ 0 & 2 \end{pmatrix}.
```

The inverse transformation undoes the scaling: it shrinks by $`\tfrac12`$ in the $`x`$ direction and stretches by $`2`$ in the $`y`$ direction.

**Verification.** We take the vector $`v=\begin{pmatrix} 1 \\ 1 \end{pmatrix}`$. First we apply $`S`$:

```math
Sv=\begin{pmatrix} 2 & 0 \\ 0 & \frac12 \end{pmatrix}\begin{pmatrix} 1 \\ 1 \end{pmatrix}=\begin{pmatrix} 2 \\ \frac12 \end{pmatrix}.
```

Then we apply $`S^{-1}`$ to the result:

```math
S^{-1}(Sv)=\begin{pmatrix} \frac12 & 0 \\ 0 & 2 \end{pmatrix}\begin{pmatrix} 2 \\ \frac12 \end{pmatrix}=\begin{pmatrix} \frac12\cdot2 \\ 2\cdot\frac12 \end{pmatrix}=\begin{pmatrix} 1 \\ 1 \end{pmatrix}=v.
```

We returned to the original vector, so $`S^{-1}`$ undoes $`S`$.