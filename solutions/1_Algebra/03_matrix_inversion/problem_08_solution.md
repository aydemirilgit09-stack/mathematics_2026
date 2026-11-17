# Problem 08: Inverse of a Transformation

## Question
### Given
The matrix

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & \frac{1}{2} \\
\end{pmatrix}
$$

describes a scaling transformation of the plane $\mathbb{R}^2$.

### Find
1. Find $S^{-1}$.
2. Explain geometrically what the inverse transformation $S^{-1}$ does.
3. Check the action of the pair $S, S^{-1}$ on a simple vector.

## Solution

### 1. Find $S^{-1}$
Since $S$ is a diagonal matrix with nonzero diagonal entries ($\det(S) = 2 \cdot \frac{1}{2} = 1 \neq 0$), its inverse is obtained by taking the reciprocals of the diagonal entries:
$$
S^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix}.
$$

---

### 2. Geometric Explanation
* The original matrix $S$ stretches vectors horizontally (along the $x$-axis) by a factor of $2$ and compresses them vertically (along the $y$-axis) by a factor of $\frac{1}{2}$: $S\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 2x \\ \frac{1}{2}y \end{pmatrix}$.
* The inverse matrix $S^{-1}$ **reverses** both scalings: it compresses vectors horizontally by a factor of $\frac{1}{2}$ and stretches them vertically by a factor of $2$, restoring every transformed point back to its original coordinates.

---

### 3. Check the Action on a Vector
Let $v = \begin{pmatrix} 3 \\ 4 \end{pmatrix}$.
1. Apply $S$:
   $$
   Sv = \begin{pmatrix} 2 & 0 \\ 0 & \frac{1}{2} \end{pmatrix} \begin{pmatrix} 3 \\ 4 \end{pmatrix} = \begin{pmatrix} 6 \\ 2 \end{pmatrix}.
   $$
2. Apply $S^{-1}$ to the result $Sv$:
   $$
   S^{-1}(Sv) = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 6 \\ 2 \end{pmatrix} = \begin{pmatrix} 3 \\ 4 \end{pmatrix} = v.
   $$

### Final Result
$$
S^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 2 \end{pmatrix}
$$