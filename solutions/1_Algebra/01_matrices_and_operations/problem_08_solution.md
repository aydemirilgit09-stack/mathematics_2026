## Question

For

$$
A=
\begin{pmatrix}
1 & 2 & -1 \\
2 & 4 & 1 \\
-1 & 1 & 3 \\
\end{pmatrix}
$$

perform, in order:

1. $R_2\leftarrow R_2-2R_1$,
2. $R_3\leftarrow R_3+R_1$,
3. interchange $R_2$ and $R_3$.

Write the matrix after each step. Then, for each of the three operations, state an operation that reverses it.

## Solution

### Method
Elementary row operations transform a matrix without changing the solution set of the corresponding linear system. Every elementary row operation is invertible via a unique inverse elementary row operation.

---

### Step-by-Step Row Operations

Starting matrix:
$$
A = \begin{pmatrix} 1 & 2 & -1 \\ 2 & 4 & 1 \\ -1 & 1 & 3 \end{pmatrix}
$$

1. **Apply $R_2 \leftarrow R_2 - 2R_1$:**
   Subtract $2 \times (1, 2, -1) = (2, 4, -2)$ from row 2:
   $$
   A_1 = \begin{pmatrix} 1 & 2 & -1 \\ 2-2 & 4-4 & 1-(-2) \\ -1 & 1 & 3 \end{pmatrix} = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix}
   $$

2. **Apply $R_3 \leftarrow R_3 + R_1$:**
   Add $(1, 2, -1)$ to row 3 of $A_1$:
   $$
   A_2 = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1+1 & 1+2 & 3+(-1) \end{pmatrix} = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix}
   $$

3. **Interchange $R_2$ and $R_3$ ($R_2 \leftrightarrow R_3$):**
   Swap row 2 and row 3 of $A_2$:
   $$
   A_3 = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 3 & 2 \\ 0 & 0 & 3 \end{pmatrix}
   $$

---

### Inverse (Reversing) Operations
To return from $A_3$ back to $A$, each step is reversed by:
1. **Reverse of Step 1 ($R_2 \leftarrow R_2 - 2R_1$):** Add $2R_1$ back to $R_2$:
   $$
   R_2 \leftarrow R_2 + 2R_1
   $$
2. **Reverse of Step 2 ($R_3 \leftarrow R_3 + R_1$):** Subtract $R_1$ from $R_3$:
   $$
   R_3 \leftarrow R_3 - R_1
   $$
3. **Reverse of Step 3 (interchange $R_2$ and $R_3$):** Swap $R_2$ and $R_3$ again (a swap is its own inverse):
   $$
   \text{interchange } R_2 \text{ and } R_3 \quad (R_2 \leftrightarrow R_3)
   $$

### Verification
Applying the reverse operations to $A_3$ in reverse order (3, then 2, then 1):
* Swap $R_2 \leftrightarrow R_3$ gives $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ 0 & 3 & 2 \end{pmatrix} = A_2$.
* $R_3 \leftarrow R_3 - R_1$ gives $\begin{pmatrix} 1 & 2 & -1 \\ 0 & 0 & 3 \\ -1 & 1 & 3 \end{pmatrix} = A_1$.
* $R_2 \leftarrow R_2 + 2R_1$ gives $\begin{pmatrix} 1 & 2 & -1 \\ 2 & 4 & 1 \\ -1 & 1 & 3 \end{pmatrix} = A$, recovering the original matrix.