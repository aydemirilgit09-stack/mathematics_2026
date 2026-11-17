# Problem 01: Determinant of a 2×2 Matrix

## Question
### Given
Consider the following two matrices:

$$
A = \begin{pmatrix}
3 & -2 \\
5 & 4
\end{pmatrix},
\qquad
B = \begin{pmatrix}
1 & 7 \\
2 & 14
\end{pmatrix}.
$$

### Find
1. Calculate the determinant of each matrix.
2. Determine which matrix is invertible and justify your answer using the determinant criterion.

## Solution

### Method and Invertibility Criterion
For any $2 \times 2$ matrix $M = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, the determinant is defined as:
$$
\det(M) = ad - bc.
$$
**Determinant Criterion for Invertibility:** A square matrix $M$ is invertible if and only if $\det(M) \neq 0$. If $\det(M) = 0$, the matrix is singular (not invertible).

---

### 1. Calculate $\det(A)$ and Check Invertibility
$$
\det(A) = (3)(4) - (-2)(5) = 12 - (-10) = 12 + 10 = 22.
$$
Since $\det(A) = 22 \neq 0$, matrix $A$ **is invertible**.

---

### 2. Calculate $\det(B)$ and Check Invertibility
$$
\det(B) = (1)(14) - (7)(2) = 14 - 14 = 0.
$$
Since $\det(B) = 0$, matrix $B$ **is not invertible** (note that the second row is twice the first row, making the rows linearly dependent).

### Verification
* For $A$, $A^{-1} = \frac{1}{22}\begin{pmatrix} 4 & 2 \\ -5 & 3 \end{pmatrix}$ exists because $\det(A) = 22 \neq 0$, and $AA^{-1} = I$.
* For $B$, the rows satisfy $R_2 = 2R_1$, confirming $\det(B) = 0$ and non-invertibility.

### Final Results
- $\det(A) = 22$ — Matrix $A$ is invertible.
- $\det(B) = 0$ — Matrix $B$ is not invertible.