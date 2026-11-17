## Question

For

$$
A=
\begin{pmatrix}
1 & 2 \\
-1 & 3 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
4 & -2 \\
0 & 5 \\
\end{pmatrix}
$$

compute

$$
A+B,\qquad A-B,\qquad 3A-2B.
$$

Explain why matrix addition is possible only for matrices of the same size.

## Solution

### Method and Dimension Compatibility Condition
Matrix addition and subtraction are defined **entry-by-entry** (element-wise). If $A = [a_{ij}]$ and $B = [b_{ij}]$ both have dimensions $m \times n$, then their sum $C = A + B$ also has dimensions $m \times n$ with entries $c_{ij} = a_{ij} + b_{ij}$. 

**Why the same size is required:** Every entry $a_{ij}$ in row $i$ and column $j$ of the first matrix must pair with a corresponding entry $b_{ij}$ at the exact same position $(i, j)$ in the second matrix. If the matrices had different numbers of rows or columns, at least one entry would lack a counterpart to add to or subtract from, leaving the operation undefined. Here, both $A$ and $B$ are $2 \times 2$ matrices, so all operations are valid.

---

### Step-by-Step Computations

1. **Compute $A + B$:**
   $$
   A + B = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} + \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 1+4 & 2+(-2) \\ -1+0 & 3+5 \end{pmatrix} = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix}
   $$

2. **Compute $A - B$:**
   $$
   A - B = \begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} - \begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 1-4 & 2-(-2) \\ -1-0 & 3-5 \end{pmatrix} = \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix}
   $$

3. **Compute $3A - 2B$:**
   First, multiply each matrix by its respective scalar:
   $$
   3A = 3\begin{pmatrix} 1 & 2 \\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix}, \qquad 2B = 2\begin{pmatrix} 4 & -2 \\ 0 & 5 \end{pmatrix} = \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix}
   $$
   Next, subtract $2B$ from $3A$:
   $$
   3A - 2B = \begin{pmatrix} 3 & 6 \\ -3 & 9 \end{pmatrix} - \begin{pmatrix} 8 & -4 \\ 0 & 10 \end{pmatrix} = \begin{pmatrix} 3-8 & 6-(-4) \\ -3-0 & 9-10 \end{pmatrix} = \begin{pmatrix} -5 & 10 \\ -3 & -1 \end{pmatrix}
   $$

### Verification
We can verify $A + B$ and $A - B$ by adding them together, which must yield $2A$:
$$
(A + B) + (A - B) = \begin{pmatrix} 5 & 0 \\ -1 & 8 \end{pmatrix} + \begin{pmatrix} -3 & 4 \\ -1 & -2 \end{pmatrix} = \begin{pmatrix} 2 & 4 \\ -2 & 6 \end{pmatrix} = 2A.
$$