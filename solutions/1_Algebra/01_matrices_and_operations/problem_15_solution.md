# Exercise 15. Associativity of Multiplication and Different Calculation Paths: Solution

Given

$$
A=\begin{pmatrix}1 & 2 & 0 \cr 0 & 1 & 1\end{pmatrix},\qquad B=\begin{pmatrix}1 & 0 \cr 2 & 1 \cr -1 & 3\end{pmatrix},\qquad C=\begin{pmatrix}2 & 1 \cr 0 & -1\end{pmatrix}.
$$

The sizes are $A$: $2\times 3$, $B$: $3\times 2$ and $C$: $2\times 2$.

## 1. Computing $(AB)C$

First, $AB$ is $2\times 2$:

$$
AB=\begin{pmatrix}1\cdot 1+2\cdot 2+0\cdot(-1) & 1\cdot 0+2\cdot 1+0\cdot 3 \cr 0\cdot 1+1\cdot 2+1\cdot(-1) & 0\cdot 0+1\cdot 1+1\cdot 3\end{pmatrix}=\begin{pmatrix}5 & 2 \cr 1 & 4\end{pmatrix}.
$$

Then

$$
(AB)C=\begin{pmatrix}5 & 2 \cr 1 & 4\end{pmatrix}\begin{pmatrix}2 & 1 \cr 0 & -1\end{pmatrix}=\begin{pmatrix}5\cdot 2+2\cdot 0 & 5\cdot 1+2\cdot(-1) \cr 1\cdot 2+4\cdot 0 & 1\cdot 1+4\cdot(-1)\end{pmatrix}=\begin{pmatrix}10 & 3 \cr 2 & -3\end{pmatrix}.
$$

## 2. Computing $A(BC)$

First, $BC$ is $3\times 2$:

$$
BC=\begin{pmatrix}1\cdot 2+0\cdot 0 & 1\cdot 1+0\cdot(-1) \cr 2\cdot 2+1\cdot 0 & 2\cdot 1+1\cdot(-1) \cr (-1)\cdot 2+3\cdot 0 & (-1)\cdot 1+3\cdot(-1)\end{pmatrix}=\begin{pmatrix}2 & 1 \cr 4 & 1 \cr -2 & -4\end{pmatrix}.
$$

Then

$$
A(BC)=\begin{pmatrix}1 & 2 & 0 \cr 0 & 1 & 1\end{pmatrix}\begin{pmatrix}2 & 1 \cr 4 & 1 \cr -2 & -4\end{pmatrix}=\begin{pmatrix}1\cdot 2+2\cdot 4+0\cdot(-2) & 1\cdot 1+2\cdot 1+0\cdot(-4) \cr 0\cdot 2+1\cdot 4+1\cdot(-2) & 0\cdot 1+1\cdot 1+1\cdot(-4)\end{pmatrix}=\begin{pmatrix}10 & 3 \cr 2 & -3\end{pmatrix}.
$$

## 3. Comparison of the results

$$
(AB)C=\begin{pmatrix}10 & 3 \cr 2 & -3\end{pmatrix}=A(BC).
$$

Both calculation paths give the same matrix.

## 4. Number of intermediate operations

Multiplying a $p\times q$ matrix by a $q\times r$ matrix takes $p\cdot q\cdot r$ multiplications of numbers.

| Path | First product | Second product | Total |
|---|---|---|---|
| $(AB)C$ | $AB$: $2\cdot 3\cdot 2=12$ | $(AB)C$: $2\cdot 2\cdot 2=8$ | $20$ |
| $A(BC)$ | $BC$: $3\cdot 2\cdot 2=12$ | $A(BC)$: $2\cdot 3\cdot 2=12$ | $24$ |

The path $(AB)C$ needs $20$ multiplications, while $A(BC)$ needs $24$. The intermediate matrices are also different: $AB$ is $2\times 2$, but $BC$ is $3\times 2$.

## 5. What associativity means

Associativity means that the way the factors are grouped does not change the final result:

$$
(AB)C=A(BC).
$$

For this reason the product can be written as $ABC$ without parentheses. Associativity does not allow changing the order of the factors, because matrix multiplication is not commutative. It does allow choosing the grouping, and a good choice can reduce the amount of computation.

> **Takeaway:** two different calculation paths give the same result because matrix multiplication is associative, although the number of operations can differ.