# Problem 01: Definition of the Inverse

## Question
### Given
For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & -1 \\
-1 & 2 \\
\end{pmatrix}.
$$

### Find
Check, without using an inverse formula, whether $B = A^{-1}$. Compute $AB$ and $BA$ and relate the result to the definition of the inverse.

## Solution

### Definition of the Inverse Matrix
A square matrix $B$ of size $n \times n$ is the **inverse** of an $n \times n$ matrix $A$ (denoted $B = A^{-1}$) if and only if multiplying them in both orders produces the $n \times n$ identity matrix $I$:
$$
AB = I \quad \text{and} \quad BA = I.
$$

---

### 1. Compute $AB$
$$
AB = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix} = \begin{pmatrix} 2(1) + 1(-1) & 2(-1) + 1(2) \\ 1(1) + 1(-1) & 1(-1) + 1(2) \end{pmatrix} = \begin{pmatrix} 2 - 1 & -2 + 2 \\ 1 - 1 & -1 + 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2.
$$

---

### 2. Compute $BA$
$$
BA = \begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} = \begin{pmatrix} 1(2) + (-1)(1) & 1(1) + (-1)(1) \\ (-1)(2) + 2(1) & (-1)(1) + 2(1) \end{pmatrix} = \begin{pmatrix} 2 - 1 & 1 - 1 \\ -2 + 2 & -1 + 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2.
$$

---

### Conclusion
Since both $AB = I_2$ and $BA = I_2$ hold, $B$ satisfies the exact definition of the multiplicative inverse of $A$. Therefore, $B = A^{-1}$ (and equivalently $A = B^{-1}$).

### Final Results
- $AB = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I$, $BA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I$
- Yes, $B = A^{-1}$.