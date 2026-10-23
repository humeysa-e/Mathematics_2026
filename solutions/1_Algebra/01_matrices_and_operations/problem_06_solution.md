# Exercise 6. Transpose: Solution

For

$$
A=\begin{pmatrix}1 & 2 & 3 \cr 4 & 5 & 6\end{pmatrix},\qquad B=\begin{pmatrix}1 & 0 \cr 2 & 1 \cr -1 & 3\end{pmatrix}.
$$

## 1. Computing $A^T$ and $B^T$

The transpose swaps rows and columns:

$$
A^T=\begin{pmatrix}1 & 4 \cr 2 & 5 \cr 3 & 6\end{pmatrix},\qquad B^T=\begin{pmatrix}1 & 2 & -1 \cr 0 & 1 & 3\end{pmatrix}.
$$

## 2. Computing $AB$

Since $A$ is $2\times 3$ and $B$ is $3\times 2$, the product $AB$ is $2\times 2$:

$$
AB=\begin{pmatrix}1\cdot 1+2\cdot 2+3\cdot(-1) & 1\cdot 0+2\cdot 1+3\cdot 3 \cr 4\cdot 1+5\cdot 2+6\cdot(-1) & 4\cdot 0+5\cdot 1+6\cdot 3\end{pmatrix}=\begin{pmatrix}2 & 11 \cr 8 & 23\end{pmatrix}.
$$

## 3. Verifying $(AB)^T=B^TA^T$

Left-hand side:

$$
(AB)^T=\begin{pmatrix}2 & 8 \cr 11 & 23\end{pmatrix}.
$$

Right-hand side:

$$
B^TA^T=\begin{pmatrix}1 & 2 & -1 \cr 0 & 1 & 3\end{pmatrix}\begin{pmatrix}1 & 4 \cr 2 & 5 \cr 3 & 6\end{pmatrix}=\begin{pmatrix}1+4-3 & 4+10-6 \cr 0+2+9 & 0+5+18\end{pmatrix}=\begin{pmatrix}2 & 8 \cr 11 & 23\end{pmatrix}.
$$

Both sides are equal, so

$$
(AB)^T=B^TA^T.
$$

> **Takeaway:** the transpose of a product is the product of the transposes in reversed order.