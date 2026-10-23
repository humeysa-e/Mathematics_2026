# Exercise 8. Row Operations and Their Reversibility: Solution

For

$$
A=\begin{pmatrix}1 & 2 & -1 \cr 2 & 4 & 1 \cr -1 & 1 & 3\end{pmatrix}
$$

we perform the operations in order.

## 1. $R_2\leftarrow R_2-2R_1$

$$
\begin{pmatrix}1 & 2 & -1 \cr 2 & 4 & 1 \cr -1 & 1 & 3\end{pmatrix}\longrightarrow\begin{pmatrix}1 & 2 & -1 \cr 0 & 0 & 3 \cr -1 & 1 & 3\end{pmatrix}.
$$

## 2. $R_3\leftarrow R_3+R_1$

$$
\begin{pmatrix}1 & 2 & -1 \cr 0 & 0 & 3 \cr -1 & 1 & 3\end{pmatrix}\longrightarrow\begin{pmatrix}1 & 2 & -1 \cr 0 & 0 & 3 \cr 0 & 3 & 2\end{pmatrix}.
$$

## 3. Interchange $R_2$ and $R_3$

$$
\begin{pmatrix}1 & 2 & -1 \cr 0 & 0 & 3 \cr 0 & 3 & 2\end{pmatrix}\longrightarrow\begin{pmatrix}1 & 2 & -1 \cr 0 & 3 & 2 \cr 0 & 0 & 3\end{pmatrix}.
$$

The final matrix is upper triangular.

## 4. Reversing each operation

| Operation | Reverse operation |
|---|---|
| $R_2\leftarrow R_2-2R_1$ | $R_2\leftarrow R_2+2R_1$ |
| $R_3\leftarrow R_3+R_1$ | $R_3\leftarrow R_3-R_1$ |
| Interchange $R_2$ and $R_3$ | Interchange $R_2$ and $R_3$ again |

For example, applying $R_2\leftarrow R_2+2R_1$ to the result of step 1 gives back $(0,0,3)+2(1,2,-1)=(2,4,1)$, which is the original second row.

> **Takeaway:** every row operation can be undone by another row operation, so row operations transform a matrix in a controlled and reversible way.