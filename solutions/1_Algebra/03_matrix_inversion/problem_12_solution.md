# Problem 12: Finding Inverses Without Starting from Scratch

## Question
### Given
It is known that

$$
A^{-1}=
\begin{pmatrix}
2 & -1 \\
-3 & 2 \\
\end{pmatrix}.
$$

### Find
Without finding the matrix $A$ itself, compute:
$$
(3A)^{-1}, \qquad (A^T)^{-1}, \qquad (A^2)^{-1}.
$$
Justify each calculation using the appropriate matrix inverse property.

## Solution

### 1. Compute $(3A)^{-1}$
**Property (Inverse of a Scalar Multiple):** For any invertible matrix $A$ and nonzero scalar $k$, $(kA)^{-1} = \frac{1}{k} A^{-1}$ (since $(kA)\left(\frac{1}{k}A^{-1}\right) = \left(k \cdot \frac{1}{k}\right)(AA^{-1}) = 1 \cdot I = I$).

Applying this with $k = 3$:
$$
(3A)^{-1} = \frac{1}{3} A^{-1} = \frac{1}{3} \begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix} = \begin{pmatrix} \frac{2}{3} & -\frac{1}{3} \\ -1 & \frac{2}{3} \end{pmatrix}.
$$

---

### 2. Compute $(A^T)^{-1}$
**Property (Inverse of a Transpose):** The inverse of the transpose equals the transpose of the inverse:
$$
(A^T)^{-1} = (A^{-1})^T
$$
(since $A^T (A^{-1})^T = (A^{-1}A)^T = I^T = I$).

Transposing the given matrix $A^{-1}$:
$$
(A^T)^{-1} = \begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix}^T = \begin{pmatrix} 2 & -3 \\ -1 & 2 \end{pmatrix}.
$$

---

### 3. Compute $(A^2)^{-1}$
**Property (Inverse of a Power):** For any invertible matrix $A$ and positive integer $n$, $(A^n)^{-1} = (A^{-1})^n$. In particular, for $n = 2$, $(A^2)^{-1} = (AA)^{-1} = A^{-1}A^{-1} = (A^{-1})^2$:
$$
(A^2)^{-1} = (A^{-1})^2 = \begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix} \begin{pmatrix} 2 & -1 \\ -3 & 2 \end{pmatrix} = \begin{pmatrix} 2(2) + (-1)(-3) & 2(-1) + (-1)(2) \\ (-3)(2) + 2(-3) & (-3)(-1) + 2(2) \end{pmatrix} = \begin{pmatrix} 4 + 3 & -2 - 2 \\ -6 - 6 & 3 + 4 \end{pmatrix} = \begin{pmatrix} 7 & -4 \\ -12 & 7 \end{pmatrix}.
$$

### Verification
Noting that $A = (A^{-1})^{-1} = \frac{1}{4 - 3}\begin{pmatrix} 2 & 1 \\ 3 & 2 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 3 & 2 \end{pmatrix}$, we verify:
$$
A^2 = \begin{pmatrix} 2 & 1 \\ 3 & 2 \end{pmatrix}\begin{pmatrix} 2 & 1 \\ 3 & 2 \end{pmatrix} = \begin{pmatrix} 7 & 4 \\ 12 & 7 \end{pmatrix} \implies (A^2)^{-1} = \frac{1}{49 - 48}\begin{pmatrix} 7 & -4 \\ -12 & 7 \end{pmatrix} = \begin{pmatrix} 7 & -4 \\ -12 & 7 \end{pmatrix}.
$$

### Final Results
- $(3A)^{-1} = \begin{pmatrix} \frac{2}{3} & -\frac{1}{3} \\ -1 & \frac{2}{3} \end{pmatrix}$
- $(A^T)^{-1} = \begin{pmatrix} 2 & -3 \\ -1 & 2 \end{pmatrix}$
- $(A^2)^{-1} = \begin{pmatrix} 7 & -4 \\ -12 & 7 \end{pmatrix}$