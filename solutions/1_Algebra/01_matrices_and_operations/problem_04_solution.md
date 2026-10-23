### Exercise 4. Matrix Multiplication and Noncommutativity - Solutions

**Given:**

$$
A=\begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix},\qquad
B=\begin{pmatrix} 2 & 0 \\ 3 & 1 \end{pmatrix}
$$

**Result:**

$$
AB=\begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix},\qquad
BA=\begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix},\qquad
AB\neq BA
$$

**Main steps:**

Each entry of a product is the dot product of a row of the first matrix with a column of the second matrix.

$$
AB=\begin{pmatrix} 1\cdot2+2\cdot3 & 1\cdot0+2\cdot1 \\ 0\cdot2+1\cdot3 & 0\cdot0+1\cdot1 \end{pmatrix}
=\begin{pmatrix} 8 & 2 \\ 3 & 1 \end{pmatrix}
$$

$$
BA=\begin{pmatrix} 2\cdot1+0\cdot0 & 2\cdot2+0\cdot1 \\ 3\cdot1+1\cdot0 & 3\cdot2+1\cdot1 \end{pmatrix}
=\begin{pmatrix} 2 & 4 \\ 3 & 7 \end{pmatrix}
$$

**Property/method used:**

$(XY)_{ij}=\sum_k x_{ik}y_{kj}$ (row times column).

Noncommutativity means that the order of the factors matters: in general $AB\neq BA$, even when both products are defined and have the same size. Here the first entries already differ ($8\neq2$), so $AB\neq BA$. This is different from numbers, where $ab=ba$ always.

**Verification:**

Recompute one entry: $(AB)_{12}$ is row 1 of $A$ times column 2 of $B$: $(1,2)\cdot(0,1)=1\cdot0+2\cdot1=2$, which matches. Also $(BA)_{11}=(2,0)\cdot(1,0)=2$, which matches.