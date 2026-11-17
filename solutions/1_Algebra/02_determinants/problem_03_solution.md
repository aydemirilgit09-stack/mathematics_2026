# Problem 03: Swapping Two Rows

## Question
### Given
Consider the following matrix:

$$
A =
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1
\end{pmatrix}.
$$

### Find
1. Compute the determinant of $A$.
2. Form a matrix $B$ by swapping the first and second rows of $A$.
3. First predict the determinant of $B$ using the determinant row-swap property, and then verify the prediction by direct calculation.

## Solution

### 1. Compute $\det(A)$
Expanding along the first row of $A$:
$$
\begin{aligned}
\det(A) &= 1 \cdot \begin{vmatrix} 3 & 1 \\ 1 & 1 \end{vmatrix} - 2 \cdot \begin{vmatrix} 0 & 1 \\ 2 & 1 \end{vmatrix} + 0 \cdot \begin{vmatrix} 0 & 3 \\ 2 & 1 \end{vmatrix} \\
&= 1(3 \cdot 1 - 1 \cdot 1) - 2(0 \cdot 1 - 1 \cdot 2) + 0 \\
&= 1(2) - 2(-2) \\
&= 2 + 4 = 6.
\end{aligned}
$$

---

### 2. Form Matrix $B$ and Predict $\det(B)$
Swapping row 1 and row 2 of $A$ ($R_1 \leftrightarrow R_2$) gives:
$$
B =
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1
\end{pmatrix}.
$$

**Prediction (Row-Swap Property):** Interchanging two rows of a square matrix multiplies its determinant by $-1$. Therefore:
$$
\det(B) = -\det(A) = -6.
$$

---

### 3. Verify $\det(B)$ by Direct Calculation
Expanding $\det(B)$ along its first row:
$$
\begin{aligned}
\det(B) &= 0 \cdot \begin{vmatrix} 2 & 0 \\ 1 & 1 \end{vmatrix} - 3 \cdot \begin{vmatrix} 1 & 0 \\ 2 & 1 \end{vmatrix} + 1 \cdot \begin{vmatrix} 1 & 2 \\ 2 & 1 \end{vmatrix} \\
&= 0 - 3(1 \cdot 1 - 0 \cdot 2) + 1(1 \cdot 1 - 2 \cdot 2) \\
&= -3(1) + 1(1 - 4) \\
&= -3 - 3 = -6.
\end{aligned}
$$

The direct calculation gives $\det(B) = -6$, confirming our prediction.

### Final Results
- $\det(A) = 6$
- $\det(B) = -6$