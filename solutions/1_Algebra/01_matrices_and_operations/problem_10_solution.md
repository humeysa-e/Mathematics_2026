# Exercise 10. Columns of a Matrix Product: Solution

Given

$$
A=\begin{pmatrix}1 & 2 & 0 \cr 0 & 1 & 1\end{pmatrix},\qquad B=\begin{pmatrix}1 & 2 \cr -1 & 0 \cr 3 & 1\end{pmatrix}.
$$

The columns of $B$ are

$$
b_1=\begin{pmatrix}1 \cr -1 \cr 3\end{pmatrix},\qquad b_2=\begin{pmatrix}2 \cr 0 \cr 1\end{pmatrix}.
$$

## 1. Computing $Ab_1$ and $Ab_2$

$$
Ab_1=\begin{pmatrix}1 & 2 & 0 \cr 0 & 1 & 1\end{pmatrix}\begin{pmatrix}1 \cr -1 \cr 3\end{pmatrix}=\begin{pmatrix}1\cdot 1+2\cdot(-1)+0\cdot 3 \cr 0\cdot 1+1\cdot(-1)+1\cdot 3\end{pmatrix}=\begin{pmatrix}-1 \cr 2\end{pmatrix},
$$

$$
Ab_2=\begin{pmatrix}1 & 2 & 0 \cr 0 & 1 & 1\end{pmatrix}\begin{pmatrix}2 \cr 0 \cr 1\end{pmatrix}=\begin{pmatrix}1\cdot 2+2\cdot 0+0\cdot 1 \cr 0\cdot 2+1\cdot 0+1\cdot 1\end{pmatrix}=\begin{pmatrix}2 \cr 1\end{pmatrix}.
$$

## 2. Computing $AB$

Since $A$ is $2\times 3$ and $B$ is $3\times 2$, the product $AB$ is $2\times 2$:

$$
AB=\begin{pmatrix}1\cdot 1+2\cdot(-1)+0\cdot 3 & 1\cdot 2+2\cdot 0+0\cdot 1 \cr 0\cdot 1+1\cdot(-1)+1\cdot 3 & 0\cdot 2+1\cdot 0+1\cdot 1\end{pmatrix}=\begin{pmatrix}-1 & 2 \cr 2 & 1\end{pmatrix}.
$$

## 3. Comparison

The first column of $AB$ is $\begin{pmatrix}-1 \cr 2\end{pmatrix}=Ab_1$, and the second column is $\begin{pmatrix}2 \cr 1\end{pmatrix}=Ab_2$. In other words,

$$
AB=\begin{pmatrix}Ab_1 & Ab_2\end{pmatrix}.
$$

## 4. Why this happens

The entry in row $i$ and column $j$ of $AB$ is the dot product of row $i$ of $A$ with column $j$ of $B$. Column $j$ of $AB$ therefore collects these dot products for all rows $i$, and this is exactly the product of $A$ with the single column $b_j$, that is, $Ab_j$. Each column of $B$ is transformed by $A$ independently of the other columns.

> **Takeaway:** the product $AB$ is built column by column, where column $j$ of $AB$ is $A$ times column $j$ of $B$.