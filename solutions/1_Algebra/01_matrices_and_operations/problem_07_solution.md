# Exercise 7. Identity Matrix, Zero Matrix, and Powers: Solution

For

$$
A=\begin{pmatrix}2 & 1 \cr 0 & 2\end{pmatrix}
$$

Let

$$
I=\begin{pmatrix}1 & 0 \cr 0 & 1\end{pmatrix},\qquad 0=\begin{pmatrix}0 & 0 \cr 0 & 0\end{pmatrix}.
$$

## 1. Roles of $I$ and $0$

The identity matrix $I$ is the neutral element for multiplication, and the zero matrix $0$ is the neutral element for addition:

$$
AI=\begin{pmatrix}2 & 1 \cr 0 & 2\end{pmatrix}\begin{pmatrix}1 & 0 \cr 0 & 1\end{pmatrix}=\begin{pmatrix}2 & 1 \cr 0 & 2\end{pmatrix}=A,
$$

$$
IA=\begin{pmatrix}1 & 0 \cr 0 & 1\end{pmatrix}\begin{pmatrix}2 & 1 \cr 0 & 2\end{pmatrix}=\begin{pmatrix}2 & 1 \cr 0 & 2\end{pmatrix}=A,
$$

$$
A+0=\begin{pmatrix}2 & 1 \cr 0 & 2\end{pmatrix}+\begin{pmatrix}0 & 0 \cr 0 & 0\end{pmatrix}=\begin{pmatrix}2 & 1 \cr 0 & 2\end{pmatrix}=A.
$$

## 2. Powers of $A$

$$
A^2=\begin{pmatrix}2 & 1 \cr 0 & 2\end{pmatrix}\begin{pmatrix}2 & 1 \cr 0 & 2\end{pmatrix}=\begin{pmatrix}4 & 4 \cr 0 & 4\end{pmatrix},
$$

$$
A^3=A^2A=\begin{pmatrix}4 & 4 \cr 0 & 4\end{pmatrix}\begin{pmatrix}2 & 1 \cr 0 & 2\end{pmatrix}=\begin{pmatrix}8 & 12 \cr 0 & 8\end{pmatrix}.
$$

## 3. Pattern

The diagonal entries are powers of $2$, and the upper-right entry is $n\cdot 2^{n-1}$:

$$
A^n=\begin{pmatrix}2^n & n\cdot 2^{n-1} \cr 0 & 2^n\end{pmatrix}.
$$

This matches $A^1$, $A^2$ and $A^3$ above. It can also be seen by writing $A=2I+N$ with

$$
N=\begin{pmatrix}0 & 1 \cr 0 & 0\end{pmatrix}.
$$

Since $N^2=0$, we get $A^n=2^nI+n\cdot 2^{n-1}N$.

> **Takeaway:** $I$ and $0$ are the neutral elements of multiplication and addition, and powers of a matrix can follow a regular pattern.