# Problem 03: When Does the Inverse Not Exist?

## Question
### Given
Consider the matrix

$$
A=
\begin{pmatrix}
2 & 4 \\
1 & 2 \\
\end{pmatrix}.
$$

### Find
Explain in two distinct ways why $A^{-1}$ does not exist:
1. Using the determinant.
2. Using linear dependence between the rows.

## Solution

### Method 1: Determinant Criterion
A square matrix $A$ is invertible if and only if $\det(A) \neq 0$. Compute the determinant of $A$:
$$
\det(A) = (2)(2) - (4)(1) = 4 - 4 = 0.
$$
Because $\det(A) = 0$, the scalar factor $\frac{1}{\det(A)} = \frac{1}{0}$ in the inverse formula is undefined, proving that $A$ is singular and $A^{-1}$ does not exist.

---

### Method 2: Linear Dependence Between the Rows
Let $R_1 = \begin{pmatrix} 2 & 4 \end{pmatrix}$ and $R_2 = \begin{pmatrix} 1 & 2 \end{pmatrix}$ be the rows of $A$. Notice that the first row is twice the second row:
$$
R_1 = 2R_2 \quad \Longleftrightarrow \quad R_1 - 2R_2 = \begin{pmatrix} 0 & 0 \end{pmatrix}.
$$
Thus, the rows of $A$ are **linearly dependent** (so $\operatorname{rank}(A) = 1 < 2$). Geometrically, the linear transformation $x \mapsto Ax$ maps every vector $\begin{pmatrix} x_1 \\ x_2 \end{pmatrix} \in \mathbb{R}^2$ onto the single line spanned by $\begin{pmatrix} 2 \\ 1 \end{pmatrix}$:
$$
\begin{pmatrix} 2 & 4 \\ 1 & 2 \end{pmatrix} \begin{pmatrix} x_1 \\ x_2 \end{pmatrix} = (x_1 + 2x_2) \begin{pmatrix} 2 \\ 1 \end{pmatrix}.
$$
Since infinitely many distinct input vectors (for example $\begin{pmatrix} 2 \\ 0 \end{pmatrix}$ and $\begin{pmatrix} 0 \\ 1 \end{pmatrix}$) map to the exact same output $\begin{pmatrix} 4 \\ 2 \end{pmatrix}$, the transformation is not one-to-one and cannot be inverted.

### Final Result
- $A^{-1}$ does not exist because $\det(A) = 0$ and its rows are linearly dependent ($R_1 = 2R_2$).