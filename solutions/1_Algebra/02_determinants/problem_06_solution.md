# Exercise 6. Parameter and Invertibility

## Question

For

```math
A(t)=\begin{pmatrix} t & 1 \\ 2 & t \end{pmatrix}
```

find all values of $`t`$ for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

> **Why this exercise:** shows how the determinant can be used to study a family of matrices depending on a parameter.

## Solution

**Rule.** A square matrix is invertible exactly when its determinant is not zero. Equivalently, it is not invertible exactly when its determinant is zero. For a $`2 \times 2`$ matrix

```math
M=\begin{pmatrix} a & b \\ c & d \end{pmatrix}
```

the determinant is $`\det M = ad - bc`$.

**Part 1: The determinant of $`A(t)`$.** Here $`a=t`$, $`b=1`$, $`c=2`$, $`d=t`$, so

```math
\det A(t) = t\cdot t - 1\cdot 2 = t^2 - 2.
```

**Part 2: When the determinant is zero.** We solve $`\det A(t) = 0`$:

```math
t^2 - 2 = 0 \quad\Longleftrightarrow\quad t^2 = 2 \quad\Longleftrightarrow\quad t = \sqrt{2} \ \text{ or } \ t = -\sqrt{2}.
```

**Part 3: The relation with invertibility.** For every $`t`$ with $`t^2 \neq 2`$ we have $`\det A(t) \neq 0`$, so $`A(t)`$ is invertible. Only for $`t = \sqrt{2}`$ and $`t = -\sqrt{2}`$ the determinant is zero, and exactly for these two values the matrix is not invertible.

**Conclusion.** The matrix $`A(t)`$ is not invertible exactly for

```math
t = \sqrt{2} \quad\text{and}\quad t = -\sqrt{2}.
```

This is because the invertibility condition $`\det A(t) \neq 0`$ fails exactly when $`t^2 - 2 = 0`$.

**Verification.** We check both values by looking at the rows. For $`t=\sqrt{2}`$ the rows are $`(\sqrt{2}, 1)`$ and $`(2, \sqrt{2})`$. The second row is $`\sqrt{2}`$ times the first row, because $`\sqrt{2}\cdot\sqrt{2} = 2`$ and $`\sqrt{2}\cdot 1 = \sqrt{2}`$. For $`t=-\sqrt{2}`$ the rows are $`(-\sqrt{2}, 1)`$ and $`(2, -\sqrt{2})`$. The second row is $`-\sqrt{2}`$ times the first row, because $`(-\sqrt{2})\cdot(-\sqrt{2}) = 2`$ and $`(-\sqrt{2})\cdot 1 = -\sqrt{2}`$. In both cases the rows are dependent, so the matrix is not invertible, which agrees with $`\det A(t) = 0`$.