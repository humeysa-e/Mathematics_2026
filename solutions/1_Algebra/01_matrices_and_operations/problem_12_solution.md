# Exercise 12. Formula for a Matrix Power: Solution

Let

$$
A=\begin{pmatrix}1 & 1 \cr 0 & 1\end{pmatrix}.
$$

## 1. Computing $A^2$, $A^3$ and $A^4$

$$
A^2=A\cdot A=\begin{pmatrix}1 & 1 \cr 0 & 1\end{pmatrix}\begin{pmatrix}1 & 1 \cr 0 & 1\end{pmatrix}=\begin{pmatrix}1 & 2 \cr 0 & 1\end{pmatrix},
$$

$$
A^3=A^2A=\begin{pmatrix}1 & 2 \cr 0 & 1\end{pmatrix}\begin{pmatrix}1 & 1 \cr 0 & 1\end{pmatrix}=\begin{pmatrix}1 & 3 \cr 0 & 1\end{pmatrix},
$$

$$
A^4=A^3A=\begin{pmatrix}1 & 3 \cr 0 & 1\end{pmatrix}\begin{pmatrix}1 & 1 \cr 0 & 1\end{pmatrix}=\begin{pmatrix}1 & 4 \cr 0 & 1\end{pmatrix}.
$$

## 2. Conjecture

The diagonal entries stay equal to $1$, the lower-left entry stays $0$, and the upper-right entry equals the exponent. We conjecture that for every positive integer $n$,

$$
A^n=\begin{pmatrix}1 & n \cr 0 & 1\end{pmatrix}.
$$

## 3. Proof by induction

**Base case.** For $n=1$, the formula gives

$$
A^1=\begin{pmatrix}1 & 1 \cr 0 & 1\end{pmatrix}=A,
$$

which is true.

**Inductive step.** Assume the formula holds for some $n$, that is,

$$
A^n=\begin{pmatrix}1 & n \cr 0 & 1\end{pmatrix}.
$$

Multiplying by $A$ gives

$$
A^{n+1}=A^nA=\begin{pmatrix}1 & n \cr 0 & 1\end{pmatrix}\begin{pmatrix}1 & 1 \cr 0 & 1\end{pmatrix}=\begin{pmatrix}1\cdot 1+n\cdot 0 & 1\cdot 1+n\cdot 1 \cr 0\cdot 1+1\cdot 0 & 0\cdot 1+1\cdot 1\end{pmatrix}=\begin{pmatrix}1 & n+1 \cr 0 & 1\end{pmatrix}.
$$

This is exactly the formula for $n+1$.

By induction, the formula holds for every positive integer $n$:

$$
A^n=\begin{pmatrix}1 & n \cr 0 & 1\end{pmatrix}.
$$

## 4. Why this works

Multiplying by $A$ adds the second row to the first row. Each multiplication by $A$ therefore adds exactly $1$ to the upper-right entry, while all other entries stay unchanged.

> **Takeaway:** a pattern found from a few computations is only a conjecture until it is proved. Induction proves the formula for all $n$ by checking the first case and showing that each case implies the next.