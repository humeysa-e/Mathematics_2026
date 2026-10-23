# Exercise 11. When Do Matrices Commute?: Solution

Given

$$
A=\begin{pmatrix}1 & 1 \cr 0 & 1\end{pmatrix},\qquad B=\begin{pmatrix}a & b \cr c & d\end{pmatrix}.
$$

## 1. Computing $AB$ and $BA$

$$
AB=\begin{pmatrix}1 & 1 \cr 0 & 1\end{pmatrix}\begin{pmatrix}a & b \cr c & d\end{pmatrix}=\begin{pmatrix}a+c & b+d \cr c & d\end{pmatrix},
$$

$$
BA=\begin{pmatrix}a & b \cr c & d\end{pmatrix}\begin{pmatrix}1 & 1 \cr 0 & 1\end{pmatrix}=\begin{pmatrix}a & a+b \cr c & c+d\end{pmatrix}.
$$

## 2. Conditions for $AB=BA$

Two matrices are equal exactly when all their entries are equal. Comparing entry by entry:

- Entry $(1,1)$: $a+c=a$, so $c=0$.
- Entry $(1,2)$: $b+d=a+b$, so $d=a$.
- Entry $(2,1)$: $c=c$, which always holds.
- Entry $(2,2)$: $d=c+d$, so $c=0$.

Therefore $AB=BA$ if and only if

$$
c=0\quad\text{and}\quad d=a,
$$

while $a$ and $b$ can be arbitrary.

## 3. General form of $B$

$$
B=\begin{pmatrix}a & b \cr 0 & a\end{pmatrix},\qquad a,b\in\mathbb{R}.
$$

This can also be written as

$$
B=aI+bN,\qquad N=\begin{pmatrix}0 & 1 \cr 0 & 0\end{pmatrix}.
$$

## 4. Check

Take

$$
B=\begin{pmatrix}a & b \cr 0 & a\end{pmatrix}.
$$

Then

$$
AB=\begin{pmatrix}a & a+b \cr 0 & a\end{pmatrix}=BA.
$$

The matrices that commute with $A$ are exactly the upper triangular matrices with equal diagonal entries.

> **Takeaway:** matrix multiplication is not commutative in general, but for a given matrix $A$ the matrices that commute with it can be found by comparing entries of $AB$ and $BA$.