# Exercise 13. A Recurrence Written in Matrix Form: Solution

Let

$$
F=\begin{pmatrix}1 & 1 \cr 1 & 0\end{pmatrix}.
$$

## 1. Computing $F^2$, $F^3$, $F^4$ and $F^5$

$$
F^2=F\cdot F=\begin{pmatrix}1 & 1 \cr 1 & 0\end{pmatrix}\begin{pmatrix}1 & 1 \cr 1 & 0\end{pmatrix}=\begin{pmatrix}2 & 1 \cr 1 & 1\end{pmatrix},
$$

$$
F^3=F^2F=\begin{pmatrix}2 & 1 \cr 1 & 1\end{pmatrix}\begin{pmatrix}1 & 1 \cr 1 & 0\end{pmatrix}=\begin{pmatrix}3 & 2 \cr 2 & 1\end{pmatrix},
$$

$$
F^4=F^3F=\begin{pmatrix}3 & 2 \cr 2 & 1\end{pmatrix}\begin{pmatrix}1 & 1 \cr 1 & 0\end{pmatrix}=\begin{pmatrix}5 & 3 \cr 3 & 2\end{pmatrix},
$$

$$
F^5=F^4F=\begin{pmatrix}5 & 3 \cr 3 & 2\end{pmatrix}\begin{pmatrix}1 & 1 \cr 1 & 0\end{pmatrix}=\begin{pmatrix}8 & 5 \cr 5 & 3\end{pmatrix}.
$$

## 2. Comparison with the Fibonacci sequence

The sequence is

$$
0,1,1,2,3,5,8,\ldots
$$

Let $F_0=0$, $F_1=1$, $F_2=1$, $F_3=2$, $F_4=3$, $F_5=5$, $F_6=8$ denote its terms. The computed powers have the form

$$
F^n=\begin{pmatrix}F_{n+1} & F_n \cr F_n & F_{n-1}\end{pmatrix}.
$$

For example,

$$
F^5=\begin{pmatrix}F_6 & F_5 \cr F_5 & F_4\end{pmatrix}=\begin{pmatrix}8 & 5 \cr 5 & 3\end{pmatrix}.
$$

So the entries of the powers of $F$ are exactly the Fibonacci numbers.

## 3. One recurrence step

For a vector with entries $a$ and $b$, we compute

$$
F\begin{pmatrix}a \cr b\end{pmatrix}=\begin{pmatrix}1 & 1 \cr 1 & 0\end{pmatrix}\begin{pmatrix}a \cr b\end{pmatrix}=\begin{pmatrix}a+b \cr a\end{pmatrix}.
$$

The first entry of the result is the sum of the two numbers, and the second entry keeps the first number for the next step.

If $a=F_{n+1}$ and $b=F_n$, then

$$
F\begin{pmatrix}F_{n+1} \cr F_n\end{pmatrix}=\begin{pmatrix}F_{n+1}+F_n \cr F_{n+1}\end{pmatrix}=\begin{pmatrix}F_{n+2} \cr F_{n+1}\end{pmatrix}.
$$

So one multiplication by $F$ moves a pair of consecutive Fibonacci numbers one step forward in the sequence.

> **Takeaway:** the Fibonacci recurrence can be written as multiplication by the matrix $F$, so computing the $n$-th term corresponds to computing a power of $F$.