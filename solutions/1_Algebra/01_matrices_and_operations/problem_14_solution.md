# Exercise 14. Rotation Matrices

## Question

The matrix for a rotation through an angle $`\theta`$ is

```math
R(\theta)=\begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix}.
```

Compute $`R(\alpha)R(\beta)`$ and, using the angle-sum formulas for sine and cosine, show that

```math
R(\alpha)R(\beta)=R(\alpha+\beta).
```

Explain the result geometrically.

> **Why this exercise:** shows the consistency between matrix algebra and the geometry of composing rotations.

## Solution

**Rule.** We multiply rows by columns, and then we use the angle-sum formulas

```math
\cos(\alpha+\beta)=\cos\alpha\cos\beta-\sin\alpha\sin\beta, \qquad \sin(\alpha+\beta)=\sin\alpha\cos\beta+\cos\alpha\sin\beta.
```

**Part 1: Computing $`R(\alpha)R(\beta)`$.** Each entry is the dot product of a row of $`R(\alpha)`$ with a column of $`R(\beta)`$:

```math
R(\alpha)R(\beta)=\begin{pmatrix} \cos\alpha\cos\beta-\sin\alpha\sin\beta & -\cos\alpha\sin\beta-\sin\alpha\cos\beta \\ \sin\alpha\cos\beta+\cos\alpha\sin\beta & -\sin\alpha\sin\beta+\cos\alpha\cos\beta \end{pmatrix}.
```

**Part 2: Using the angle-sum formulas.** We recognize each entry:

- Row 1, column 1: $`\cos\alpha\cos\beta-\sin\alpha\sin\beta=\cos(\alpha+\beta)`$.
- Row 1, column 2: $`-\cos\alpha\sin\beta-\sin\alpha\cos\beta=-(\sin\alpha\cos\beta+\cos\alpha\sin\beta)=-\sin(\alpha+\beta)`$.
- Row 2, column 1: $`\sin\alpha\cos\beta+\cos\alpha\sin\beta=\sin(\alpha+\beta)`$.
- Row 2, column 2: $`\cos\alpha\cos\beta-\sin\alpha\sin\beta=\cos(\alpha+\beta)`$.

Therefore

```math
R(\alpha)R(\beta)=\begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \end{pmatrix}=R(\alpha+\beta).
```

**Part 3: Geometric explanation.** The matrix $`R(\theta)`$ rotates every vector counterclockwise by the angle $`\theta`$ around the origin. The product $`R(\alpha)R(\beta)x`$ means that we first rotate $`x`$ by $`\beta`$ and then rotate the result by $`\alpha`$. Two rotations around the same point, one after the other, give a single rotation by the total angle $`\alpha+\beta`$. So the algebraic result $`R(\alpha)R(\beta)=R(\alpha+\beta)`$ agrees with the geometry: composing rotations adds their angles.

Since $`\alpha+\beta=\beta+\alpha`$, we also get $`R(\beta)R(\alpha)=R(\alpha+\beta)`$, so rotations in the plane commute, unlike the products in Exercise 4 and Exercise 9.

**Verification.** We check a special case, $`\alpha=\beta=90^\circ`$. Here $`R(90^\circ)=\begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}`$, so

```math
R(90^\circ)R(90^\circ)=\begin{pmatrix} 0\cdot0+(-1)\cdot1 & 0\cdot(-1)+(-1)\cdot0 \\ 1\cdot0+0\cdot1 & 1\cdot(-1)+0\cdot0 \end{pmatrix}=\begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix}=R(180^\circ).
```

This matches the formula, because $`\cos180^\circ=-1`$ and $`\sin180^\circ=0`$.