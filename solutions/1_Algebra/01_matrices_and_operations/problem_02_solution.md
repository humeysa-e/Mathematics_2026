# Exercise 2. Addition and Scalar Multiplication

## Question

For

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3
\end{pmatrix}, \qquad
B=
\begin{pmatrix}
4 & -2 \\
0 & 5
\end{pmatrix}
$$

compute

$$
A+B, \qquad A-B, \qquad 3A-2B.
$$

Explain why matrix addition is possible only for matrices of the same size.

> **Why this exercise:** reinforces entry-by-entry operations and the importance of compatible dimensions.

## Solution

**Part 1: Sum $A+B$.** Matrices of the same size are added entry by entry, that is, $(A+B)_{ij} = a_{ij} + b_{ij}$. Both $A$ and $B$ are $2 \times 2$, so

$$
A+B =
\begin{pmatrix}
1+4 & 2+(-2) \\
-1+0 & 3+5
\end{pmatrix}
=
\begin{pmatrix}
5 & 0 \\
-1 & 8
\end{pmatrix}.
$$

**Part 2: Difference $A-B$.** Subtraction also works entry by entry, $(A-B)_{ij} = a_{ij} - b_{ij}$, so

$$
A-B =
\begin{pmatrix}
1-4 & 2-(-2) \\
-1-0 & 3-5
\end{pmatrix}
=
\begin{pmatrix}
-3 & 4 \\
-1 & -2
\end{pmatrix}.
$$

**Part 3: Combination $3A-2B$.** Multiplying a matrix by a scalar $c$ multiplies every entry by $c$, that is, $(cA)_{ij} = c\,a_{ij}$. First we compute $3A$ and $2B$:

$$
3A =
\begin{pmatrix}
3 & 6 \\
-3 & 9
\end{pmatrix}, \qquad
2B =
\begin{pmatrix}
8 & -4 \\
0 & 10
\end{pmatrix}.
$$

Then we subtract entry by entry:

$$
3A-2B =
\begin{pmatrix}
3-8 & 6-(-4) \\
-3-0 & 9-10
\end{pmatrix}
=
\begin{pmatrix}
-5 & 10 \\
-3 & -1
\end{pmatrix}.
$$

**Part 4: Why the sizes must be equal.** Addition is defined entry by entry: each entry $a_{ij}$ of $A$ is paired with the entry $b_{ij}$ in the same position of $B$. If $A$ and $B$ have different sizes, some entries of one matrix have no partner in the other matrix. For example, a $2 \times 3$ matrix has an entry $a_{23}$, but a $2 \times 2$ matrix has no entry $b_{23}$, so $a_{23} + b_{23}$ cannot be formed. Therefore $A+B$ is defined only when $A$ and $B$ have the same number of rows and the same number of columns.

**Verification.** We check one entry of $3A-2B$ in a different way. The entry in row 2, column 2 is $3a_{22} - 2b_{22} = 3 \cdot 3 - 2 \cdot 5 = 9 - 10 = -1$, which matches the result above.