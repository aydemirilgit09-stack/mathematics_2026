# Problem 07: Using Properties Instead of Recomputing

## Question
### Given
Suppose that for a $3 \times 3$ matrix $A$, $\det(A) = -4$.

### Find
Compute:
$$
\det(2A), \quad \det(A^T), \quad \det(A^2), \quad \det(-A).
$$
Justify each answer using the appropriate determinant property.

## Solution

### 1. Compute $\det(2A)$
**Property (Scalar Multiplication):** For an $n \times n$ matrix $A$ and scalar $k$, multiplying every row of $A$ by $k$ multiplies the determinant by $k^n$:
$$
\det(kA) = k^n \det(A).
$$
Here $n = 3$ and $k = 2$:
$$
\det(2A) = 2^3 \det(A) = 8 \cdot (-4) = -32.
$$

---

### 2. Compute $\det(A^T)$
**Property (Transpose):** Transposing a square matrix leaves its determinant unchanged:
$$
\det(A^T) = \det(A).
$$
Therefore:
$$
\det(A^T) = -4.
$$

---

### 3. Compute $\det(A^2)$
**Property (Multiplicativity of Determinants):** For any two square matrices $X$ and $Y$ of the same size, $\det(XY) = \det(X)\det(Y)$. In particular, $\det(A^2) = \det(AA) = (\det(A))^2$:
$$
\det(A^2) = (-4)^2 = 16.
$$

---

### 4. Compute $\det(-A)$
**Property (Scalar Multiplication with $k = -1$):** Since $-A = (-1)A$ and $n = 3$:
$$
\det(-A) = (-1)^3 \det(A) = (-1) \cdot (-4) = 4.
$$

### Verification
Using the diagonal matrix $A = \operatorname{diag}(-4, 1, 1)$ (which is $3 \times 3$ with $\det(A) = -4$):
* $\det(2A) = \det(\operatorname{diag}(-8, 2, 2)) = (-8)(2)(2) = -32$.
* $\det(A^T) = \det(A) = -4$.
* $\det(A^2) = \det(\operatorname{diag}(16, 1, 1)) = 16$.
* $\det(-A) = \det(\operatorname{diag}(4, -1, -1)) = 4$.

### Final Results
- $\det(2A) = -32$
- $\det(A^T) = -4$
- $\det(A^2) = 16$
- $\det(-A) = 4$