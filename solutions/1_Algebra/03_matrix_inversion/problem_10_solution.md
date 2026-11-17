# Problem 10: Inverse of a Diagonal Matrix

## Question
### Given
Given

$$
D=
\begin{pmatrix}
2 & 0 & 0 \\
0 & -3 & 0 \\
0 & 0 & 5 \\
\end{pmatrix},\qquad E=
\begin{pmatrix}
2 & 0 & 0 \\
0 & 0 & 0 \\
0 & 0 & 5 \\
\end{pmatrix}.
$$

### Find
1. Without using Gauss–Jordan elimination, determine which matrix is invertible.
2. For the invertible matrix, write down its inverse and verify the result by multiplication.

## Solution

### 1. Determine Which Matrix Is Invertible
For any diagonal matrix $\operatorname{diag}(d_1, d_2, \dots, d_n)$, the determinant is the product of its diagonal entries: $\det = d_1 d_2 \cdots d_n$. Thus, a diagonal matrix is invertible if and only if **all of its diagonal entries are nonzero**.

* **Matrix $D$:** Its diagonal entries are $2, -3, 5$ (all nonzero), and $\det(D) = 2 \cdot (-3) \cdot 5 = -30 \neq 0$. Hence, **$D$ is invertible**.
* **Matrix $E$:** Its second diagonal entry is $0$ (an entire zero row/column), so $\det(E) = 2 \cdot 0 \cdot 5 = 0$. Hence, **$E$ is not invertible**.

---

### 2. Inverse of $D$
The inverse of an invertible diagonal matrix is formed by replacing each diagonal entry $d_i$ with its reciprocal $\frac{1}{d_i}$:
$$
D^{-1} = \begin{pmatrix}
\frac{1}{2} & 0 & 0 \\
0 & -\frac{1}{3} & 0 \\
0 & 0 & \frac{1}{5}
\end{pmatrix}.
$$

---

### Verification
Multiply $D$ by $D^{-1}$:
$$
DD^{-1} = \begin{pmatrix} 2 & 0 & 0 \\ 0 & -3 & 0 \\ 0 & 0 & 5 \end{pmatrix} \begin{pmatrix} \frac{1}{2} & 0 & 0 \\ 0 & -\frac{1}{3} & 0 \\ 0 & 0 & \frac{1}{5} \end{pmatrix} = \begin{pmatrix} 2 \cdot \frac{1}{2} & 0 & 0 \\ 0 & (-3)\left(-\frac{1}{3}\right) & 0 \\ 0 & 0 & 5 \cdot \frac{1}{5} \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix} = I_3.
$$

### Final Results
- $D$ is invertible; $E$ is not invertible.
- $D^{-1} = \begin{pmatrix} \frac{1}{2} & 0 & 0 \\ 0 & -\frac{1}{3} & 0 \\ 0 & 0 & \frac{1}{5} \end{pmatrix}$