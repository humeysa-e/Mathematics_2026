# Exercise 9. Composing Transformations

## Question

Let

```math
S=\begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}, \qquad R=\begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}.
```

The matrix $`S`$ describes nonuniform scaling, while $`R`$ describes a $`90^\circ`$ counterclockwise rotation. For

```math
x=\begin{pmatrix} 1 \\ 2 \end{pmatrix}
```

compute $`RSx`$ and $`SRx`$. Compare the results and explain geometrically why the order of these transformations matters.

> **Why this exercise:** interprets matrix multiplication as composition of transformations.

## Solution

**Rule.** A product of matrices acts on a vector from right to left, that is, $`RSx=R(Sx)`$ means that we first apply $`S`$ to $`x`$ and then apply $`R`$ to the result. Similarly, $`SRx=S(Rx)`$ means that we first rotate and then scale. The matrix $`S`$ multiplies the first coordinate by $`2`$ and leaves the second coordinate unchanged. The matrix $`R`$ sends $`(a,b)^T`$ to $`(-b,a)^T`$.

**Part 1: Computing $`RSx`$.** First we apply $`S`$ to $`x`$:

```math
Sx=\begin{pmatrix} 2\cdot1+0\cdot2 \\ 0\cdot1+1\cdot2 \end{pmatrix}=\begin{pmatrix} 2 \\ 2 \end{pmatrix}.
```

Then we apply $`R`$ to this vector:

```math
RSx=R\begin{pmatrix} 2 \\ 2 \end{pmatrix}=\begin{pmatrix} 0\cdot2+(-1)\cdot2 \\ 1\cdot2+0\cdot2 \end{pmatrix}=\begin{pmatrix} -2 \\ 2 \end{pmatrix}.
```

**Part 2: Computing $`SRx`$.** First we apply $`R`$ to $`x`$:

```math
Rx=\begin{pmatrix} 0\cdot1+(-1)\cdot2 \\ 1\cdot1+0\cdot2 \end{pmatrix}=\begin{pmatrix} -2 \\ 1 \end{pmatrix}.
```

Then we apply $`S`$ to this vector:

```math
SRx=S\begin{pmatrix} -2 \\ 1 \end{pmatrix}=\begin{pmatrix} 2\cdot(-2)+0\cdot1 \\ 0\cdot(-2)+1\cdot1 \end{pmatrix}=\begin{pmatrix} -4 \\ 1 \end{pmatrix}.
```

**Part 3: Comparison.** We obtained

```math
RSx=\begin{pmatrix} -2 \\ 2 \end{pmatrix}, \qquad SRx=\begin{pmatrix} -4 \\ 1 \end{pmatrix}.
```

These vectors are different, so $`RSx\neq SRx`$. Therefore the order of the transformations matters, and this is another example of noncommutativity: in general $`RS\neq SR`$.

**Part 4: Geometric explanation.** The scaling $`S`$ stretches vectors only in the direction of the $`x`$-axis, so its effect depends on how the vector is positioned relative to the axes. The rotation $`R`$ changes this position.

- In $`RSx`$ we stretch first. The vector $`(1,2)^T`$ becomes $`(2,2)^T`$, and then the rotation turns it by $`90^\circ`$ without changing its length. So $`RSx`$ has length $`\sqrt{8}`$.
- In $`SRx`$ we rotate first. The vector $`(1,2)^T`$ becomes $`(-2,1)^T`$, which now points mostly along the $`x`$-axis. The scaling then stretches this horizontal part by a factor of $`2`$, which gives $`(-4,1)^T`$ of length $`\sqrt{17}`$.

In the first case the stretch is applied to the original horizontal direction, and in the second case it is applied to the horizontal direction of the rotated vector. These are different directions in the vector, so the final results are different.

**Verification.** We check the result using the product matrices. By multiplying rows by columns,

```math
RS=\begin{pmatrix} 0 & -1 \\ 2 & 0 \end{pmatrix}, \qquad SR=\begin{pmatrix} 0 & -2 \\ 1 & 0 \end{pmatrix}.
```

Then

```math
RSx=\begin{pmatrix} 0\cdot1+(-1)\cdot2 \\ 2\cdot1+0\cdot2 \end{pmatrix}=\begin{pmatrix} -2 \\ 2 \end{pmatrix}, \qquad SRx=\begin{pmatrix} 0\cdot1+(-2)\cdot2 \\ 1\cdot1+0\cdot2 \end{pmatrix}=\begin{pmatrix} -4 \\ 1 \end{pmatrix}.
```

Both results match the step-by-step computation above, and the matrices $`RS`$ and $`SR`$ are different.