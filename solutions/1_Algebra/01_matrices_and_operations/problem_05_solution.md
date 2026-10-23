# Exercise 5. Matrix Times Vector: Solution

Let

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3
\end{pmatrix},\qquad x=
\begin{pmatrix}
4 \\
2
\end{pmatrix}.
$$

## 1. Computing $Ax$

Each entry of $Ax$ is the dot product of a row of $A$ with $x$:

$$
Ax=
\begin{pmatrix}
2\cdot 4+(-1)\cdot 2 \\
1\cdot 4+3\cdot 2
\end{pmatrix}
=
\begin{pmatrix}
6 \\
10
\end{pmatrix}.
$$

## 2. $Ax$ as a linear combination of the columns of $A$

The coefficients are the entries of $x$ ($4$ and $2$):

$$
Ax = 4
\begin{pmatrix}
2 \\
1
\end{pmatrix}
+2
\begin{pmatrix}
-1 \\
3
\end{pmatrix}
=
\begin{pmatrix}
8 \\
4
\end{pmatrix}
+
\begin{pmatrix}
-2 \\
6
\end{pmatrix}
=
\begin{pmatrix}
6 \\
10
\end{pmatrix}.
$$

Both methods give the same result:

$$
Ax=
\begin{pmatrix}
6 \\
10
\end{pmatrix}.
$$

> **Takeaway:** multiplying a matrix by a vector produces a linear combination of the matrix columns, with the entries of the vector as coefficients.