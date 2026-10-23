### Exercise 1. Matrix Size and Entries - Solutions

**Given:**

$$
A =
\begin{pmatrix}
2 & -1 & 3 \\
0 & 4 & 5
\end{pmatrix}, \qquad
B =
\begin{pmatrix}
1 & 0 \\
-2 & 3 \\
4 & 1
\end{pmatrix}
$$

**1. State the sizes of matrices $A$ and $B$.**
* Size of $A$: $2 \times 3$
* Size of $B$: $3 \times 2$

**2. Read off the entries $a_{12}$, $a_{23}$, $b_{21}$, and $b_{32}$.**
* $a_{12} = -1$
* $a_{23} = 5$
* $b_{21} = -2$
* $b_{32} = 1$

**3. Write the second row of $A$ and the first column of $B$ as vectors.**
* Second row of $A$: $(0,\ 4,\ 5)$
* First column of $B$: $(1,\ -2,\ 4)^{T}$

---

**Main steps:**
Count the rows and columns of each matrix. For $a_{ij}$, go to row $i$ and column $j$.

**Property/method used:**
A matrix with $m$ rows and $n$ columns has size $m \times n$. The entry $a_{ij}$ is in row $i$, column $j$.

**Verification:**
$A$ has 2 rows with 3 entries each, so $2 \cdot 3 = 6$ entries. $B$ has 3 rows with 2 entries each, so $3 \cdot 2 = 6$ entries. Both match the entries listed in the matrices.