# Problem 12: A Parameter Revealed by a Row Operation

## Question
### Given
For

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

### Find
1. Perform the row operation $R_2 \leftarrow R_2 - 2R_1$ before computing the determinant.
2. Find all values of $t$ for which the matrix $A(t)$ is not invertible.
3. Explain what special structural property occurs in the rows of $A(t)$ for the value of $t$ found.

## Solution

### 1. Perform the Row Operation $R_2 \leftarrow R_2 - 2R_1$
Adding a multiple of one row to another preserves the determinant ($\det(A_1(t)) = \det(A(t))$):
$$
A(t) =
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1
\end{pmatrix}
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
A_1(t) =
\begin{pmatrix}
1 & 2 & 3 \\
0 & 0 & t - 6 \\
0 & 1 & 1
\end{pmatrix}.
$$

---

### 2. Compute $\det(A(t))$ and Find Non-Invertible Values
Expanding $\det(A_1(t))$ along the first column (which has only one nonzero entry):
$$
\det(A(t)) = \det(A_1(t)) = 1 \cdot \begin{vmatrix} 0 & t - 6 \\ 1 & 1 \end{vmatrix} = 0 \cdot 1 - (t - 6) \cdot 1 = 6 - t.
$$

A square matrix is **not invertible** if and only if its determinant equals zero:
$$
6 - t = 0 \implies t = 6.
$$

---

### 3. Structural Explanation at $t = 6$
When $t = 6$, the entry $t - 6$ becomes $0$, turning the second row of $A_1(6)$ into an **entirely zero row** $\begin{pmatrix} 0 & 0 & 0 \end{pmatrix}$. In the original matrix $A(6)$, this means:
$$
R_2 = \begin{pmatrix} 2 & 4 & 6 \end{pmatrix} = 2 \begin{pmatrix} 1 & 2 & 3 \end{pmatrix} = 2R_1,
$$
so the second row is an exact scalar multiple of the first row (the rows are linearly dependent), causing the determinant to vanish.

### Final Results
- Not invertible for: $t = 6$
- At $t = 6$, $R_2 = 2R_1$ (linearly dependent rows; $R_2$ reduces to a zero row).