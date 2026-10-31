# Exercise 1. Matrix Size and Entries

## Question

Given

$$
A=
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5
\end{pmatrix}, \qquad
B=
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1
\end{pmatrix}.
$$

1. State the sizes of matrices $A$ and $B$.
2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.
3. Write the second row of $A$ and the first column of $B$ as vectors.

> **Why this exercise:** builds basic fluency with matrix notation, indices, rows, and columns.

## Solution

**Part 1: Sizes.** A matrix with $m$ rows and $n$ columns has size $m \times n$. Matrix $A$ has 2 rows and 3 columns, and matrix $B$ has 3 rows and 2 columns, so

$$
A \text{ is } 2 \times 3, \qquad B \text{ is } 3 \times 2.
$$

**Part 2: Entries.** The entry $a_{ij}$ is located in row $i$ and column $j$. We go to the given row, then move along it to the given column:

- $a_{12}$: row 1, column 2 of $A$, so $a_{12} = -1$.
- $a_{23}$: row 2, column 3 of $A$, so $a_{23} = 5$.
- $b_{21}$: row 2, column 1 of $B$, so $b_{21} = -2$.
- $b_{32}$: row 3, column 2 of $B$, so $b_{32} = 1$.

**Part 3: Row and column vectors.** A row of a matrix is read from left to right, and a column from top to bottom. The second row of $A$ is

$$
(0,\ 4,\ 5),
$$

and the first column of $B$, written as a column vector, is

$$
\begin{pmatrix} 1 \\ -2 \\ 4 \end{pmatrix}.
$$

**Verification.** A matrix of size $m \times n$ has $m \cdot n$ entries. For $A$: $2 \cdot 3 = 6$ entries, and for $B$: $3 \cdot 2 = 6$ entries. Both counts match the entries written in the matrices.