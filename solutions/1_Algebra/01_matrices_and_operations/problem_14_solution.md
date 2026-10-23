# Exercise 14. Rotation Matrices: Solution

The matrix for a rotation through an angle $\theta$ is

$$
R(\theta)=\begin{pmatrix}\cos\theta & -\sin\theta \cr \sin\theta & \cos\theta\end{pmatrix}.
$$

## 1. Computing $R(\alpha)R(\beta)$

$$
R(\alpha)R(\beta)=\begin{pmatrix}\cos\alpha & -\sin\alpha \cr \sin\alpha & \cos\alpha\end{pmatrix}\begin{pmatrix}\cos\beta & -\sin\beta \cr \sin\beta & \cos\beta\end{pmatrix}.
$$

Multiplying entry by entry:

$$
R(\alpha)R(\beta)=\begin{pmatrix}\cos\alpha\cos\beta-\sin\alpha\sin\beta & -\cos\alpha\sin\beta-\sin\alpha\cos\beta \cr \sin\alpha\cos\beta+\cos\alpha\sin\beta & -\sin\alpha\sin\beta+\cos\alpha\cos\beta\end{pmatrix}.
$$

## 2. Using the angle-sum formulas

The angle-sum formulas are

$$
\cos(\alpha+\beta)=\cos\alpha\cos\beta-\sin\alpha\sin\beta,
$$

$$
\sin(\alpha+\beta)=\sin\alpha\cos\beta+\cos\alpha\sin\beta.
$$

Applying them to each entry:

- Entry $(1,1)$: $\cos\alpha\cos\beta-\sin\alpha\sin\beta=\cos(\alpha+\beta)$.
- Entry $(1,2)$: $-(\cos\alpha\sin\beta+\sin\alpha\cos\beta)=-\sin(\alpha+\beta)$.
- Entry $(2,1)$: $\sin\alpha\cos\beta+\cos\alpha\sin\beta=\sin(\alpha+\beta)$.
- Entry $(2,2)$: $\cos\alpha\cos\beta-\sin\alpha\sin\beta=\cos(\alpha+\beta)$.

Therefore

$$
R(\alpha)R(\beta)=\begin{pmatrix}\cos(\alpha+\beta) & -\sin(\alpha+\beta) \cr \sin(\alpha+\beta) & \cos(\alpha+\beta)\end{pmatrix}=R(\alpha+\beta).
$$

## 3. Geometric explanation

The matrix $R(\beta)$ rotates a vector by the angle $\beta$, and then $R(\alpha)$ rotates the result by the angle $\alpha$. Rotating first by $\beta$ and then by $\alpha$ turns the vector through a total angle of $\alpha+\beta$, which is exactly what $R(\alpha+\beta)$ does.

So multiplying rotation matrices corresponds to adding the angles of rotation. Since $\alpha+\beta=\beta+\alpha$, we also get

$$
R(\alpha)R(\beta)=R(\beta)R(\alpha).
$$

Rotation matrices in the plane therefore commute, unlike matrices in general.

> **Takeaway:** the algebra of matrix multiplication agrees with the geometry of composing rotations: multiplying the matrices adds the angles.