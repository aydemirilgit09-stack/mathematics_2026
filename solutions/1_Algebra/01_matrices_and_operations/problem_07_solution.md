## Question

For

$$
A=
\begin{pmatrix}
2 & 1 \\
0 & 2 \\
\end{pmatrix}
$$

compute

$$
AI,\qquad IA,\qquad A+0,\qquad A^2,\qquad A^3.
$$

Explain the roles of the matrices $I$ and $0$, and describe the pattern you observe in successive powers of $A$.

## Solution

### Definitions and Roles of $I$ and $0$
For $2 \times 2$ matrices, the identity matrix is $I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$ and the zero matrix is $0 = \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix}$.
* **Role of $I$:** $I$ is the **multiplicative identity** (neutral element for matrix multiplication), meaning $AI = IA = A$ for any square matrix $A$.
* **Role of $0$:** $0$ is the **additive identity** (neutral element for matrix addition), meaning $A + 0 = 0 + A = A$.

---

### Step-by-Step Computations

1. **Compute $AI$ and $IA$:**
   $$
   AI = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 2(1)+1(0) & 2(0)+1(1) \\ 0(1)+2(0) & 0(0)+2(1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = A
   $$
   $$
   IA = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 1(2)+0(0) & 1(1)+0(2) \\ 0(2)+1(0) & 0(1)+1(2) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = A
   $$

2. **Compute $A + 0$:**
   $$
   A + 0 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} + \begin{pmatrix} 0 & 0 \\ 0 & 0 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = A
   $$

3. **Compute $A^2$:**
   $$
   A^2 = AA = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 2(2)+1(0) & 2(1)+1(2) \\ 0(2)+2(0) & 0(1)+2(2) \end{pmatrix} = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}
   $$

4. **Compute $A^3$:**
   $$
   A^3 = A^2 A = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} 4(2)+4(0) & 4(1)+4(2) \\ 0(2)+4(0) & 0(1)+4(2) \end{pmatrix} = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}
   $$

---

### Pattern in Successive Powers of $A$
Looking at $A^1 = \begin{pmatrix} 2 & 1 \\ 0 & 2 \end{pmatrix}$, $A^2 = \begin{pmatrix} 4 & 4 \\ 0 & 4 \end{pmatrix}$, and $A^3 = \begin{pmatrix} 8 & 12 \\ 0 & 8 \end{pmatrix}$, we observe:
* The matrix remains upper triangular with $0$ in the bottom-left entry.
* The diagonal entries equal $2^n$ (for $n=1,2,3$: $2, 4, 8$).
* The top-right entry equals $n \cdot 2^{n-1}$ (for $n=1$: $1 \cdot 2^0 = 1$; for $n=2$: $2 \cdot 2^1 = 4$; for $n=3$: $3 \cdot 2^2 = 12$).

In general:
$$
A^n = \begin{pmatrix} 2^n & n \cdot 2^{n-1} \\ 0 & 2^n \end{pmatrix}.
$$