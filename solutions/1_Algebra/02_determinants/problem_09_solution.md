# Problem 09: Area and the Determinant

## Question
### Given
The given vectors are:

$$
u=\begin{pmatrix}3\\1\end{pmatrix},
\qquad
v=\begin{pmatrix}1\\4\end{pmatrix}.
$$

These two vectors span a parallelogram in $\mathbb{R}^2$.

### Find
1. Compute the area of the parallelogram using the determinant.
2. Reverse the order of the vectors and compute the new determinant.
3. Explain how reversing the order changes the determinant and why the area remains unchanged.

## Solution

### 1. Compute the Determinant and Area of the Parallelogram
Form the $2 \times 2$ matrix with columns $u$ and $v$:
$$
\det\begin{pmatrix} u & v \end{pmatrix} = \begin{vmatrix} 3 & 1 \\ 1 & 4 \end{vmatrix} = (3)(4) - (1)(1) = 12 - 1 = 11.
$$
The area of the parallelogram spanned by $u$ and $v$ is the absolute value of this determinant:
$$
\text{Area} = \left|\det\begin{pmatrix} u & v \end{pmatrix}\right| = |11| = 11.
$$

---

### 2. Reverse the Order of the Vectors
Form the $2 \times 2$ matrix with columns $v$ and $u$:
$$
\det\begin{pmatrix} v & u \end{pmatrix} = \begin{vmatrix} 1 & 3 \\ 4 & 1 \end{vmatrix} = (1)(1) - (3)(4) = 1 - 12 = -11.
$$
The area computed from the reversed order is:
$$
\text{Area} = \left|\det\begin{pmatrix} v & u \end{pmatrix}\right| = |-11| = 11.
$$

---

### 3. Geometric Explanation
* **Effect on the determinant:** Swapping the two columns $u$ and $v$ multiplies the determinant by $-1$ (changing $11$ to $-11$). Geometrically, the sign of a $2 \times 2$ determinant encodes **orientation**: $(u, v)$ is positively oriented (counterclockwise from $u$ to $v$), whereas $(v, u)$ is negatively oriented (clockwise from $v$ to $u$).
* **Why area is unchanged:** Reversing the order of the two spanning vectors does not change the geometric shape or size of the parallelogram itself; it only reverses the orientation. Because area is a non-negative geometric measure given by $|\det|$, we have $|-11| = |11| = 11$.

### Final Results
- $\det(u, v) = 11$, $\det(v, u) = -11$
- Area of the parallelogram $= 11$