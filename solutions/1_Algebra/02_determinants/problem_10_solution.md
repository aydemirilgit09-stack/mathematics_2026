# Problem 10: Detecting Dependence

## Question
### Given
The given matrix is:

$$
A=
\begin{pmatrix}
1 & 2 & 3\\
2 & 4 & 6\\
0 & 1 & 5
\end{pmatrix}.
$$

### Find
1. Identify a specific linear dependence between the rows.
2. Explain why the rows are linearly dependent.
3. Connect this dependence to the determinant being zero.
4. Explain why the matrix is not invertible.

## Solution

### 1. Specific Dependence Between the Rows
Let $R_1, R_2, R_3$ denote the rows of $A$:
$$
R_1 = \begin{pmatrix} 1 & 2 & 3 \end{pmatrix}, \qquad R_2 = \begin{pmatrix} 2 & 4 & 6 \end{pmatrix}, \qquad R_3 = \begin{pmatrix} 0 & 1 & 5 \end{pmatrix}.
$$
Notice that the second row is exactly twice the first row:
$$
R_2 = 2R_1 \quad \Longleftrightarrow \quad 2R_1 - R_2 + 0R_3 = \begin{pmatrix} 0 & 0 & 0 \end{pmatrix}.
$$

---

### 2. Why the Rows Are Linearly Dependent
A set of vectors (rows) $\{R_1, R_2, R_3\}$ is **linearly dependent** if there exist scalars $c_1, c_2, c_3$, not all zero, such that $c_1 R_1 + c_2 R_2 + c_3 R_3 = 0$. Here, choosing $(c_1, c_2, c_3) = (2, -1, 0) \neq (0, 0, 0)$ satisfies $2R_1 - R_2 + 0R_3 = 0$, proving linear dependence.

---

### 3. Connection to $\det(A) = 0$
Performing the determinant-preserving row operation $R_2 \leftarrow R_2 - 2R_1$ produces an entire row of zeros:
$$
\det(A) = \begin{vmatrix} 1 & 2 & 3 \\ 2 & 4 & 6 \\ 0 & 1 & 5 \end{vmatrix} = \begin{vmatrix} 1 & 2 & 3 \\ 0 & 0 & 0 \\ 0 & 1 & 5 \end{vmatrix} = 0.
$$
Because a matrix with a zero row has determinant $0$, any square matrix with linearly dependent rows has $\det(A) = 0$.

---

### 4. Why the Matrix Is Not Invertible
By the Invertible Matrix Theorem, a square matrix $A$ is invertible if and only if $\det(A) \neq 0$ (equivalently, its rows are linearly independent and $\operatorname{rank}(A) = 3$). Since $\det(A) = 0$ and $\operatorname{rank}(A) = 2 < 3$, the linear map $x \mapsto Ax$ collapses $\mathbb{R}^3$ onto a 2-dimensional plane, so no inverse matrix $A^{-1}$ exists.

### Final Results
- Row dependence: $R_2 = 2R_1$ (linearly dependent rows)
- $\det(A) = 0$
- Matrix $A$ is singular (not invertible).