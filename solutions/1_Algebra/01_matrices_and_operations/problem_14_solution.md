# Problem 14: Rotation Matrices

## Question
### Given
The matrix for a rotation through an angle $\theta$ is

$$
R(\theta)=
\begin{pmatrix}
\cos\theta & -\sin\theta \\
\sin\theta & \cos\theta \\
\end{pmatrix}.
$$

### Find
1. Compute $R(\alpha)R(\beta)$.
2. Using the angle-sum formulas for sine and cosine, show that $R(\alpha)R(\beta) = R(\alpha + \beta)$.
3. Explain the result geometrically.

## Solution

### 1. Compute the Product $R(\alpha)R(\beta)$
Write out the matrices for angles $\alpha$ and $\beta$ and multiply them row-by-column:
$$
\begin{aligned}
R(\alpha)R(\beta) &= \begin{pmatrix} \cos\alpha & -\sin\alpha \\ \sin\alpha & \cos\alpha \end{pmatrix} \begin{pmatrix} \cos\beta & -\sin\beta \\ \sin\beta & \cos\beta \end{pmatrix} \\
&= \begin{pmatrix} \cos\alpha\cos\beta + (-\sin\alpha)\sin\beta & \cos\alpha(-\sin\beta) + (-\sin\alpha)\cos\beta \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & \sin\alpha(-\sin\beta) + \cos\alpha\cos\beta \end{pmatrix} \\
&= \begin{pmatrix} \cos\alpha\cos\beta - \sin\alpha\sin\beta & -(\sin\alpha\cos\beta + \cos\alpha\sin\beta) \\ \sin\alpha\cos\beta + \cos\alpha\sin\beta & \cos\alpha\cos\beta - \sin\alpha\sin\beta \end{pmatrix}.
\end{aligned}
$$

---

### 2. Apply Trigonometric Angle-Sum Identities
Recall the standard angle-sum formulas:
$$
\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta
$$
$$
\sin(\alpha + \beta) = \sin\alpha\cos\beta + \cos\alpha\sin\beta
$$

Substituting these identities into the four entries of the product matrix gives:
$$
R(\alpha)R(\beta) = \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \end{pmatrix} = R(\alpha + \beta).
$$

---

### 3. Geometric Explanation
In the 2D plane, applying $R(\beta)$ to a vector rotates it counterclockwise around the origin by an angle $\beta$. Subsequently applying $R(\alpha)$ rotates that image counterclockwise around the origin by an additional angle $\alpha$. Performing a rotation by $\beta$ followed by a rotation by $\alpha$ around the same center is geometrically identical to a single counterclockwise rotation through the combined angle $\alpha + \beta$, which is represented by $R(\alpha + \beta)$.

### Verification
Testing with $\alpha = 90^\circ$ ($\frac{\pi}{2}$) and $\beta = 90^\circ$ ($\frac{\pi}{2}$):
$$
R(90^\circ)R(90^\circ) = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix} = \begin{pmatrix} \cos 180^\circ & -\sin 180^\circ \\ \sin 180^\circ & \cos 180^\circ \end{pmatrix} = R(180^\circ).
$$

### Final Result
$$
R(\alpha)R(\beta) = \begin{pmatrix} \cos(\alpha+\beta) & -\sin(\alpha+\beta) \\ \sin(\alpha+\beta) & \cos(\alpha+\beta) \end{pmatrix} = R(\alpha + \beta).
$$