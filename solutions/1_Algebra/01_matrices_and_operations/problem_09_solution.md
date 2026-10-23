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
\begin{pmatrix}1 \cr 2\end{pmatrix}\xrightarrow{\;S\;}\begin{pmatrix}2 \cr 2\end{pmatrix}\xrightarrow{\;R\;}\begin{pmatrix}-2 \cr 2\end{pmatrix}.
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
\begin{pmatrix}1 \cr 2\end{pmatrix}\xrightarrow{\;R\;}\begin{pmatrix}-2 \cr 1\end{pmatrix}\xrightarrow{\;S\;}\begin{pmatrix}-4 \cr 1\end{pmatrix}.
$$

## 3. Comparison

$$
RSx=\begin{pmatrix}-2 \cr 2\end{pmatrix}\neq\begin{pmatrix}-4 \cr 1\end{pmatrix}=SRx.
$$

The results are different, so $RS\neq SR$.

## 4. Why the order matters

The matrix $S$ stretches only the horizontal direction, by a factor of $2$. If we scale first, the stretching happens along the original $x$-axis, and the rotation then turns the stretched vector. If we rotate first, the horizontal direction is no longer the direction of the original vector's components, so the stretching is applied to different components and the final vector differs.

In general, a product of matrices applies the transformations from right to left, and since matrix multiplication is not commutative, changing the order changes the transformation.

> **Takeaway:** matrix multiplication is composition of transformations, and the order of composition matters.