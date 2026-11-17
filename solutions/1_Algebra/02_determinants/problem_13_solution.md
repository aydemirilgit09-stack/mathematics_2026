# Problem 13: Determinant by Elimination

## Question
### Given
Compute the determinant of

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

using Gaussian elimination. Record the effect of every row operation used on the value of the determinant.

## Solution

### Method
Adding a scalar multiple of one row to another row ($R_i \leftarrow R_i + kR_j$, $i \neq j$) leaves the determinant unchanged. Reducing $A$ to an upper triangular matrix $U$ allows us to compute $\det(A) = \det(U) = u_{11} u_{22} u_{33}$.

---

### Step-by-Step Elimination

Start with:
$$
A =
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2
\end{pmatrix}
$$

1. **Eliminate the entries below the first pivot $a_{11} = 1$:**
   * Apply $R_2 \leftarrow R_2 - 2R_1$ (adds $-2R_1$ to $R_2$; **determinant unchanged**).
   * Apply $R_3 \leftarrow R_3 - R_1$ (adds $-R_1$ to $R_3$; **determinant unchanged**).
   $$
   A_1 =
   \begin{pmatrix}
   1 & 2 & 3 \\
   0 & 1 & 1 \\
   0 & -2 & -1
   \end{pmatrix}, \qquad \det(A_1) = \det(A).
   $$

2. **Eliminate the entry below the second pivot $a_{22} = 1$:**
   * Apply $R_3 \leftarrow R_3 + 2R_2$ (adds $2R_2$ to $R_3$; **determinant unchanged**).
   $$
   U =
   \begin{pmatrix}
   1 & 2 & 3 \\
   0 & 1 & 1 \\
   0 & 0 & 1
   \end{pmatrix}, \qquad \det(U) = \det(A_1) = \det(A).
   $$

3. **Compute the determinant of $U$:**
   Since $U$ is upper triangular, its determinant is the product of its diagonal entries:
   $$
   \det(A) = \det(U) = 1 \cdot 1 \cdot 1 = 1.
   $$

### Verification
Expanding $A$ along the first row confirms the result:
$$
\det(A) = 1(10 - 0) - 2(4 - 7) + 3(0 - 5) = 10 + 6 - 15 = 1.
$$

### Final Result
- $\det(A) = 1$