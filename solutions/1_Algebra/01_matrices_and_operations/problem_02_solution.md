### Exercise 2. Addition and Scalar Multiplication - Solutions

**Result:**

$$
A+B=\begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix},\qquad
A-B=\begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix},\qquad
3A-2B=\begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}
$$

**Main steps:**

Matrices are added and subtracted entry by entry. For scalar multiplication, every entry is multiplied by the scalar.

$$
3A=\begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix},\qquad
2B=\begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}
$$

Then $3A-2B$ is computed entry by entry: $3-8=-5$, $6-(-4)=10$, $-3-0=-3$, $9-10=-1$.

**Property/method used:**

$$
(A\pm B)_{ij}=a_{ij}\pm b_{ij},\qquad (cA)_{ij}=c\,a_{ij}
$$

Matrix addition is possible only for matrices of the same size, because each entry $a_{ij}$ needs a partner entry $b_{ij}$ in the same position. If the sizes differ, some entries have no partner, so the sum is not defined.

**Verification:**

$(A+B)+(A-B)$ should equal $2A$:

$$
\begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}+\begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}
=\begin{pmatrix} 2 & 4 \\ -2 & 6 \end{pmatrix}=2A
$$