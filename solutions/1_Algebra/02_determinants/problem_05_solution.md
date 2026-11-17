# Problem 05: Row Operations

## Question
### Given
Consider the following matrix:

$$
A =
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2
\end{pmatrix}.
$$

### Find
Find the determinant of $A$ by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

## Solution

### Method (Effect of Row Operations on Determinants)
Adding a scalar multiple of one row to another row ($R_i \leftarrow R_i + kR_j$ for $i \neq j$) **leaves the determinant unchanged**. Once reduced to upper triangular form, the determinant is the product of the diagonal entries.

---

### Step-by-Step Reduction

Start with:
$$
A =
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2
\end{pmatrix}
$$

1. **Eliminate the entries below $a_{11} = 1$:**
   Apply $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 + R_1$:
   $$
   A_1 =
   \begin{pmatrix}
   1 & 2 & 3 \\
   0 & -3 & -6 \\
   0 & 6 & 5
   \end{pmatrix}
   $$
   *Effect on determinant:* **Unchanged** ($\det(A_1) = \det(A)$), because both operations add multiples of $R_1$ to other rows.

2. **Eliminate the entry below $a_{22} = -3$:**
   Apply $R_3 \leftarrow R_3 + 2R_2$:
   $$
   A_2 =
   \begin{pmatrix}
   1 & 2 & 3 \\
   0 & -3 & -6 \\
   0 & 0 & -7
   \end{pmatrix}
   $$
   *Effect on determinant:* **Unchanged** ($\det(A_2) = \det(A_1) = \det(A)$), because adding $2R_2$ to $R_3$ preserves the determinant.

3. **Compute the determinant of the upper triangular matrix $A_2$:**
   $$
   \det(A) = \det(A_2) = 1 \cdot (-3) \cdot (-7) = 21.
   $$

### Verification
Expanding the original matrix $A$ along the first row confirms the result:
$$
\det(A) = 1(2 - 0) - 2(4 - 0) + 3(8 - (-1)) = 2 - 8 + 27 = 21.
$$

### Final Result
- $\det(A) = 21$