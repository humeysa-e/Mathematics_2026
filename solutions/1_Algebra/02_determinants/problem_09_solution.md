# Exercise 9. Area and the Determinant

## Question

The vectors

```math
u=\begin{pmatrix} 3 \\ 1 \end{pmatrix},\qquad v=\begin{pmatrix} 1 \\ 4 \end{pmatrix}
```

span a parallelogram. Compute its area using a determinant. Then reverse the order of the vectors and explain what changes in the determinant and what does not change in the area.

> **Why this exercise:** gives the determinant a geometric interpretation and distinguishes its sign from the value of the area.

## Solution

**Rule.** For two vectors $`u, v`$ in the plane, the area of the parallelogram spanned by them is the absolute value of the determinant of the matrix whose columns are $`u`$ and $`v`$:

```math
\text{Area} = \left|\det\begin{pmatrix} u & v \end{pmatrix}\right|.
```

The sign of the determinant depends on the order of the vectors, but the area is never negative.

**Part 1: The determinant for the order $`u, v`$.** We put $`u`$ and $`v`$ as columns:

```math
\det\begin{pmatrix} u & v \end{pmatrix}=\det\begin{pmatrix} 3 & 1 \\ 1 & 4 \end{pmatrix}=3\cdot 4 - 1\cdot 1 = 12 - 1 = 11.
```

**Part 2: The area.**

```math
\text{Area} = |11| = 11.
```

**Part 3: Reversing the order.** Now we put $`v`$ first and $`u`$ second:

```math
\det\begin{pmatrix} v & u \end{pmatrix}=\det\begin{pmatrix} 1 & 3 \\ 4 & 1 \end{pmatrix}=1\cdot 1 - 3\cdot 4 = 1 - 12 = -11.
```

The matrix $`\begin{pmatrix} v & u \end{pmatrix}`$ is obtained from $`\begin{pmatrix} u & v \end{pmatrix}`$ by swapping two columns, so the determinant changes its sign. The area is

```math
\text{Area} = |-11| = 11.
```

**Conclusion.** The parallelogram spanned by $`u`$ and $`v`$ has area $`11`$. When the order of the vectors is reversed, the determinant changes from $`11`$ to $`-11`$ (the sign changes because the orientation is reversed), but the area stays $`11`$, because the parallelogram is the same figure and the area is the absolute value of the determinant.

**Verification.** We compute the area in a different way, with the shoelace formula. The vertices of the parallelogram are $`(0,0)`$, $`u=(3,1)`$, $`u+v=(4,5)`$ and $`v=(1,4)`$. For vertices $`(x_1,y_1),\dots,(x_4,y_4)`$ listed in order around the figure, the area is $`\tfrac12\left|\sum (x_i y_{i+1} - x_{i+1} y_i)\right|`$, where after the last vertex we return to the first one. The four terms are

```math
0\cdot 1 - 3\cdot 0 = 0,\qquad 3\cdot 5 - 4\cdot 1 = 11,\qquad 4\cdot 4 - 1\cdot 5 = 11,\qquad 1\cdot 0 - 0\cdot 4 = 0.
```

Their sum is $`22`$, so the area is $`\tfrac12\cdot 22 = 11`$. This agrees with the determinant.