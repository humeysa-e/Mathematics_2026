# Exercise 8. Row Operations and Their Reversibility

## Question

For

```math
A=\begin{pmatrix} 1 & 2 & -1 \\ 2 & 4 & 1 \\ -1 & 1 & 3 \end{pmatrix}
```

perform, in order:

1. $`R_2\leftarrow R_2-2R_1`$,
2. $`R_3\leftarrow R_3+R_1`$,
3. interchange $`R_2`$ and $`R_3`$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

> **Why this exercise:** prepares for elimination by showing that row operations are controlled and reversible transformations of a matrix.

## Solution

**Rule.** An elementary row operation changes one row at a time: it either adds a multiple of one row to another row, or interchanges two rows. All other rows stay unchanged. Each such operation can be undone by another row operation, which we find in Part 4.

**Part 1: Step 1, $`R_2\leftarrow R_2-2R_1`$.** We subtract twice the first row from the second row. The new second row is $`(2-2\cdot1,\ 4-2\cdot2,\ 1-2\cdot(-1))=(0,\ 0,\ 3)`$, and the other rows stay the same:

```math
A_1=\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix}.
```

**Part 2: Step 2, $`R_3\leftarrow R_3+R_1`$.** We add the first row to the third row. The new third row is $`(-1+1,\ 1+2,\ 3+(-1))=(0,\ 3,\ 2)`$:

```math
A_2=\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix}.
```

**Part 3: Step 3, interchange $`R_2`$ and $`R_3`$.** We swap the second and third rows:

```math
A_3=\begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix}.
```

**Part 4: Reversing each operation.** To undo an operation, we do the opposite action on the same rows:

- $`R_2\leftarrow R_2-2R_1`$ is reversed by $`R_2\leftarrow R_2+2R_1`$, because adding back what was subtracted restores the row.
- $`R_3\leftarrow R_3+R_1`$ is reversed by $`R_3\leftarrow R_3-R_1`$, for the same reason.
- Interchanging $`R_2`$ and $`R_3`$ is reversed by interchanging $`R_2`$ and $`R_3`$ again, because swapping twice puts the rows back.

**Verification.** We apply the reversing operations to $`A_3`$ in the opposite order. First we interchange $`R_2`$ and $`R_3`$, which gives $`A_2`$. Then $`R_3\leftarrow R_3-R_1`$ gives the third row $`(0-1,\ 3-2,\ 2-(-1))=(-1,\ 1,\ 3)`$, which gives $`A_1`$. Finally $`R_2\leftarrow R_2+2R_1`$ gives the second row $`(0+2,\ 0+4,\ 3-2)=(2,\ 4,\ 1)`$, and we get

```math
\begin{pmatrix} 1 & 2 & -1 \\ 2 & 4 & 1 \\ -1 & 1 & 3 \end{pmatrix}=A.
```

So the original matrix is restored.