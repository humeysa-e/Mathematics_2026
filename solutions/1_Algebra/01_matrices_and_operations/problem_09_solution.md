# Exercise 9. Composing Transformations: Solution

Let

$$
S=\begin{pmatrix}2 & 0 \cr 0 & 1\end{pmatrix},\qquad R=\begin{pmatrix}0 & -1 \cr 1 & 0\end{pmatrix},\qquad x=\begin{pmatrix}1 \cr 2\end{pmatrix}.
$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation.

## 1. Computing $RSx$

In the product $RSx$, the matrix $S$ acts first and $R$ acts second:

$$
RS=\begin{pmatrix}0 & -1 \cr 1 & 0\end{pmatrix}\begin{pmatrix}2 & 0 \cr 0 & 1\end{pmatrix}=\begin{pmatrix}0 & -1 \cr 2 & 0\end{pmatrix},
$$

$$
RSx=\begin{pmatrix}0 & -1 \cr 2 & 0\end{pmatrix}\begin{pmatrix}1 \cr 2\end{pmatrix}=\begin{pmatrix}-2 \cr 2\end{pmatrix}.
$$

Step by step:

$$
\begin{pmatrix}1 \cr 2\end{pmatrix}\xrightarrow{S}\begin{pmatrix}2 \cr 2\end{pmatrix}\xrightarrow{R}\begin{pmatrix}-2 \cr 2\end{pmatrix}.
$$

## 2. Computing $SRx$

In the product $SRx$, the matrix $R$ acts first and $S$ acts second:

$$
SR=\begin{pmatrix}2 & 0 \cr 0 & 1\end{pmatrix}\begin{pmatrix}0 & -1 \cr 1 & 0\end{pmatrix}=\begin{pmatrix}0 & -2 \cr 1 & 0\end{pmatrix},
$$

$$
SRx=\begin{pmatrix}0 & -2 \cr 1 & 0\end{pmatrix}\begin{pmatrix}1 \cr 2\end{pmatrix}=\begin{pmatrix}-4 \cr 1\end{pmatrix}.
$$

Step by step:

$$
\begin{pmatrix}1 \cr 2\end{pmatrix}\xrightarrow{R}\begin{pmatrix}-2 \cr 1\end{pmatrix}\xrightarrow{S}\begin{pmatrix}-4 \cr 1\end{pmatrix}.
$$

## 3. Comparison

$$
RSx=\begin{pmatrix}-2 \cr 2\end{pmatrix}\neq\begin{pmatrix}-4 \cr 1\end{pmatrix}=SRx.
$$

The results are different, so $RS\neq SR$.

## 4. Why the order matters

The matrix $S$ stretches only the horizontal component of a vector, by a factor of $2$. The two orders stretch different components:

- In $RSx$, we scale first. The original horizontal component $1$ is doubled to $2$, and then the rotation turns $(2,2)$ into $(-2,2)$.
- In $SRx$, we rotate first. The rotation turns $(1,2)$ into $(-2,1)$, so the horizontal component is now $-2$ (it came from the original vertical component). Scaling then doubles it to $-4$.

In general, a product of matrices applies the transformations from right to left, and since matrix multiplication is not commutative, changing the order changes the transformation.

> **Takeaway:** matrix multiplication is composition of transformations, and the order of composition matters.