# Problem 11: Shortening the Calculation with Row Operations

## Question
### Given
Compute

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

## Solution

### Method (Determinant-Preserving Row Operations)
Adding a scalar multiple of one row to another row ($R_i \leftarrow R_i + kR_j$ for $i \neq j$) **does not change the value of the determinant**. By using these operations to reduce the matrix to upper triangular form, the determinant becomes the product of its main diagonal entries.

---

### Step-by-Step Reduction

Start with:
$$
A =
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6
\end{pmatrix}
$$

1. **Create zeros in the first column below $a_{11} = 1$:**
   Perform $R_2 \leftarrow R_2 - R_1$ and $R_3 \leftarrow R_3 - R_1$:
   $$
   A_1 =
   \begin{pmatrix}
   1 & 2 & 3 \\
   0 & 1 & 1 \\
   0 & 2 & 3
   \end{pmatrix}
   $$
   *Effect on determinant:* **Unchanged** ($\det(A_1) = \det(A)$), because both operations add a multiple of $R_1$ to another row.

2. **Create a zero in the second column below $a_{22} = 1$:**
   Perform $R_3 \leftarrow R_3 - 2R_2$:
   $$
   A_2 =
   \begin{pmatrix}
   1 & 2 & 3 \\
   0 & 1 & 1 \\
   0 & 0 & 1
   \end{pmatrix}
   $$
   *Effect on determinant:* **Unchanged** ($\det(A_2) = \det(A_1) = \det(A)$), because adding $-2R_2$ to $R_3$ preserves the determinant.

3. **Compute the determinant of the upper triangular matrix $A_2$:**
   $$
   \det(A) = \det(A_2) = 1 \cdot 1 \cdot 1 = 1.
   $$

### Verification
Expanding the original matrix $A$ along the first row confirms the result:
$$
\det(A) = 1(18 - 16) - 2(6 - 4) + 3(4 - 3) = 2 - 4 + 3 = 1.
$$

### Final Result
- $\det(A) = 1$