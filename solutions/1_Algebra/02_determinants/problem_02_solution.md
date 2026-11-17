# Problem 02: Determinant of a 3×3 Matrix

## Question
### Given
Consider the following $3 \times 3$ matrix:

$$
A =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5
\end{pmatrix}.
$$

### Find
1. Calculate the determinant of matrix $A$ using Sarrus' rule.
2. Verify the result using cofactor expansion along the first row.

## Solution

### 1. Calculate $\det(A)$ Using Sarrus' Rule
Sarrus' rule sums the products of the three downward-right diagonals and subtracts the products of the three upward-right diagonals:
$$
\begin{aligned}
\det(A) &= \big[(1 \cdot 3 \cdot 5) + (2 \cdot 4 \cdot 2) + (-1 \cdot 0 \cdot 1)\big] - \big[(2 \cdot 3 \cdot (-1)) + (1 \cdot 4 \cdot 1) + (5 \cdot 0 \cdot 2)\big] \\
&= \big[15 + 16 + 0\big] - \big[-6 + 4 + 0\big] \\
&= 31 - (-2) \\
&= 31 + 2 = 33.
\end{aligned}
$$

---

### 2. Verification Using Cofactor Expansion Along the First Row
Expanding $\det(A)$ along row 1 using $\det(A) = a_{11}C_{11} + a_{12}C_{12} + a_{13}C_{13}$ where $C_{1j} = (-1)^{1+j}M_{1j}$:
$$
\begin{aligned}
\det(A) &= 1 \cdot \begin{vmatrix} 3 & 4 \\ 1 & 5 \end{vmatrix} - 2 \cdot \begin{vmatrix} 0 & 4 \\ 2 & 5 \end{vmatrix} + (-1) \cdot \begin{vmatrix} 0 & 3 \\ 2 & 1 \end{vmatrix} \\
&= 1(3 \cdot 5 - 4 \cdot 1) - 2(0 \cdot 5 - 4 \cdot 2) - 1(0 \cdot 1 - 3 \cdot 2) \\
&= 1(15 - 4) - 2(0 - 8) - 1(0 - 6) \\
&= 1(11) - 2(-8) - 1(-6) \\
&= 11 + 16 + 6 = 33.
\end{aligned}
$$

Both Sarrus' rule and cofactor expansion along the first row yield $\det(A) = 33$, confirming the result.

### Final Result
- $\det(A) = 33$