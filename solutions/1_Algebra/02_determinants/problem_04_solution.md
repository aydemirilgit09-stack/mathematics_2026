# Problem 04: Triangular Matrix

## Question
### Given
Consider the following upper triangular matrix:

$$
A =
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7
\end{pmatrix}.
$$

### Find
1. Calculate the determinant of $A$ without expanding it.
2. State the general rule for finding the determinant of a triangular matrix and explain why it applies here.

## Solution

### 1. General Rule and Explanation
**Rule:** The determinant of any triangular matrix (upper triangular, lower triangular, or diagonal) is equal to the **product of its main diagonal entries**:
$$
\det(A) = a_{11} \cdot a_{22} \cdots a_{nn}.
$$

**Why it applies here:** Matrix $A$ is upper triangular because all entries below its main diagonal are zero ($a_{21} = 0$, $a_{31} = 0$, $a_{32} = 0$). If we repeatedly apply cofactor expansion down the first column, each step leaves only a single nonzero term on the diagonal, reducing the determinant directly to the product of the diagonal elements.

---

### 2. Calculate $\det(A)$
The main diagonal entries of $A$ are $a_{11} = 2$, $a_{22} = -3$, and $a_{33} = 7$. Multiplying them together:
$$
\det(A) = 2 \cdot (-3) \cdot 7 = (-6) \cdot 7 = -42.
$$

### Verification
Expanding along the first column confirms the formula:
$$
\det(A) = 2 \begin{vmatrix} -3 & 5 \\ 0 & 7 \end{vmatrix} - 0 + 0 = 2((-3)(7) - (5)(0)) = 2(-21) = -42.
$$

### Final Result
- $\det(A) = -42$