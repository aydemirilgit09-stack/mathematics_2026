# Problem 02: Formula for a 2×2 Matrix

## Question
### Given
Consider the matrix

$$
A=
\begin{pmatrix}
3 & 2 \\
5 & 4 \\
\end{pmatrix}.
$$

### Find
Find the inverse $A^{-1}$ using the formula for a $2 \times 2$ matrix. At the end, verify the result by computing one product with $A$.

## Solution

### Method ($2 \times 2$ Inverse Formula)
For a $2 \times 2$ matrix $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, its inverse exists if and only if $\det(A) = ad - bc \neq 0$, and is given by:
$$
A^{-1} = \frac{1}{ad - bc} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}.
$$

---

### Step 1: Compute the Determinant of $A$
Here $a = 3$, $b = 2$, $c = 5$, and $d = 4$:
$$
\det(A) = (3)(4) - (2)(5) = 12 - 10 = 2.
$$
Since $\det(A) = 2 \neq 0$, $A^{-1}$ exists.

---

### Step 2: Apply the Inverse Formula
Swap the main diagonal entries ($3$ and $4$), negate the off-diagonal entries ($2$ and $5$), and divide by $\det(A) = 2$:
$$
A^{-1} = \frac{1}{2} \begin{pmatrix} 4 & -2 \\ -5 & 3 \end{pmatrix} = \begin{pmatrix} 2 & -1 \\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}.
$$

---

### Verification
Multiply $A$ by $A^{-1}$ to confirm that the product equals the identity matrix $I_2$:
$$
AA^{-1} = \begin{pmatrix} 3 & 2 \\ 5 & 4 \end{pmatrix} \begin{pmatrix} 2 & -1 \\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix} = \begin{pmatrix} 3(2) + 2\left(-\frac{5}{2}\right) & 3(-1) + 2\left(\frac{3}{2}\right) \\ 5(2) + 4\left(-\frac{5}{2}\right) & 5(-1) + 4\left(\frac{3}{2}\right) \end{pmatrix} = \begin{pmatrix} 6 - 5 & -3 + 3 \\ 10 - 10 & -5 + 6 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2.
$$

### Final Result
$$
A^{-1} = \begin{pmatrix} 2 & -1 \\ -\frac{5}{2} & \frac{3}{2} \end{pmatrix}
$$