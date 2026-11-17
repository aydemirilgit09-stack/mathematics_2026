# Problem 09: Matrix Equation

## Question
### Given
Given

$$
A=
\begin{pmatrix}
1 & 2 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
3 & 1 \\
2 & 4 \\
\end{pmatrix}.
$$

### Find
Solve the matrix equation $AX = B$ for $X$. Before calculating, decide on which side of the equation $A^{-1}$ must be applied, and then verify the result by computing $AX$.

## Solution

### Step 1: Decide Which Side to Multiply by $A^{-1}$
Because matrix multiplication is **not commutative**, the side on which we multiply matters. In $AX = B$, $A$ appears on the **left** of $X$. Therefore, we must multiply both sides of the equation **on the left** by $A^{-1}$:
$$
A^{-1}(AX) = A^{-1}B \implies (A^{-1}A)X = A^{-1}B \implies IX = A^{-1}B \implies X = A^{-1}B.
$$
*(Multiplying on the right would give $AXA^{-1} = BA^{-1}$, which does not isolate $X$.)*

---

### Step 2: Compute $A^{-1}$ and $X = A^{-1}B$
Compute $A^{-1}$ using the $2 \times 2$ inverse formula ($\det(A) = 1 \cdot 1 - 2 \cdot 0 = 1$):
$$
A^{-1} = \frac{1}{1} \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix}.
$$

Now multiply $A^{-1}$ on the left of $B$:
$$
X = A^{-1}B = \begin{pmatrix} 1 & -2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix} = \begin{pmatrix} 1(3) + (-2)(2) & 1(1) + (-2)(4) \\ 0(3) + 1(2) & 0(1) + 1(4) \end{pmatrix} = \begin{pmatrix} 3 - 4 & 1 - 8 \\ 2 & 4 \end{pmatrix} = \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}.
$$

---

### Verification
Compute $AX$ to verify that it equals $B$:
$$
AX = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix} = \begin{pmatrix} 1(-1) + 2(2) & 1(-7) + 2(4) \\ 0(-1) + 1(2) & 0(-7) + 1(4) \end{pmatrix} = \begin{pmatrix} -1 + 4 & -7 + 8 \\ 2 & 4 \end{pmatrix} = \begin{pmatrix} 3 & 1 \\ 2 & 4 \end{pmatrix} = B.
$$

### Final Result
$$
X = \begin{pmatrix} -1 & -7 \\ 2 & 4 \end{pmatrix}
$$