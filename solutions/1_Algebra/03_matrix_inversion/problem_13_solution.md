# Exercise 13. Undoing a Composite Transformation

## Question

The matrices

```math
S=\begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix},\qquad H=\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}
```

describe nonuniform scaling and shear. For $`T=HS`$, find $`T^{-1}`$ in two ways:

1. first compute $`T`$, then its inverse,
2. use $`(HS)^{-1}=S^{-1}H^{-1}`$.

Compare the results. Additionally compute $`H^{-1}S^{-1}`$ and verify that the incorrect order gives a different matrix. Explain the rule: "when undoing a composition of operations, we undo them from the end."

> **Why this exercise:** reinforces the inverse of a product in a less direct configuration.

## Solution

**Rule.** For a $`2 \times 2`$ matrix

```math
M=\begin{pmatrix} a & b \\ c & d \end{pmatrix}
```

with $`\det M = ad-bc \neq 0`$, the inverse is

```math
M^{-1}=\frac{1}{ad-bc}\begin{pmatrix} d & -b \\ -c & a \end{pmatrix}.
```

**Part 1: The matrix $`T`$.**

```math
T=HS=\begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}=\begin{pmatrix} 1\cdot2+1\cdot0 & 1\cdot0+1\cdot1 \\ 0\cdot2+1\cdot0 & 0\cdot0+1\cdot1 \end{pmatrix}=\begin{pmatrix} 2 & 1 \\ 0 & 1 \end{pmatrix}.
```

**Part 2: Method 1, the inverse of $`T`$ directly.** Here $`\det T = 2\cdot1 - 1\cdot0 = 2`$, so

```math
T^{-1}=\frac12\begin{pmatrix} 1 & -1 \\ 0 & 2 \end{pmatrix}=\begin{pmatrix} \frac12 & -\frac12 \\ 0 & 1 \end{pmatrix}.
```

**Part 3: Method 2, using $`(HS)^{-1}=S^{-1}H^{-1}`$.** We have $`\det S = 2`$ and $`\det H = 1`$, so

```math
S^{-1}=\begin{pmatrix} \frac12 & 0 \\ 0 & 1 \end{pmatrix},\qquad H^{-1}=\begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}.
```

Then

```math
S^{-1}H^{-1}=\begin{pmatrix} \frac12 & 0 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}=\begin{pmatrix} \frac12\cdot1+0\cdot0 & \frac12\cdot(-1)+0\cdot1 \\ 0\cdot1+1\cdot0 & 0\cdot(-1)+1\cdot1 \end{pmatrix}=\begin{pmatrix} \frac12 & -\frac12 \\ 0 & 1 \end{pmatrix}.
```

**Part 4: Comparison.** Both methods give the same matrix:

```math
T^{-1}=S^{-1}H^{-1}=\begin{pmatrix} \frac12 & -\frac12 \\ 0 & 1 \end{pmatrix}.
```

**Part 5: The incorrect order.**

```math
H^{-1}S^{-1}=\begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} \frac12 & 0 \\ 0 & 1 \end{pmatrix}=\begin{pmatrix} \frac12 & -1 \\ 0 & 1 \end{pmatrix}.
```

This is different from $`T^{-1}`$: the entry in row 1, column 2 is $`-1`$ instead of $`-\frac12`$. So the order matters.

**Part 6: The rule.** The matrix $`T=HS`$ means: first apply $`S`$ (scaling), then apply $`H`$ (shear). To undo this composition, we must undo the last operation first. So we first apply $`H^{-1}`$, which undoes the shear, and then $`S^{-1}`$, which undoes the scaling. In matrix form this is $`S^{-1}H^{-1}`$, because the operation applied first stands on the right. This is the rule "when undoing a composition of operations, we undo them from the end."

**Conclusion.** $`T^{-1}=\begin{pmatrix} \frac12 & -\frac12 \\ 0 & 1 \end{pmatrix}`$, and the reversed product $`H^{-1}S^{-1}=\begin{pmatrix} \frac12 & -1 \\ 0 & 1 \end{pmatrix}`$ is not the inverse of $`T`$.

**Verification.** We check by multiplication:

```math
TT^{-1}=\begin{pmatrix} 2 & 1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} \frac12 & -\frac12 \\ 0 & 1 \end{pmatrix}=\begin{pmatrix} 1 & -1+1 \\ 0 & 1 \end{pmatrix}=I,
```

while for the incorrect order

```math
T\,(H^{-1}S^{-1})=\begin{pmatrix} 2 & 1 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} \frac12 & -1 \\ 0 & 1 \end{pmatrix}=\begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}\neq I.
```