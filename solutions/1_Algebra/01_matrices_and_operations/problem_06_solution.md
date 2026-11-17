## Question

For

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix}
$$

compute $A^T$, $B^T$, and $AB$. Then verify in this example that

$$
(AB)^T=B^TA^T.
$$

## Solution

### Method
The transpose $M^T$ of a matrix $M$ is formed by interchanging its rows and columns (the $(i,j)$-th entry of $M^T$ is the $(j,i)$-th entry of $M$). For matrix multiplication, the transpose of a product reverses the order of the factors: $(AB)^T = B^T A^T$.

---

### Step 1: Compute $A^T$ and $B^T$
* $A$ is $2 \times 3$, so $A^T$ is $3 \times 2$:
  $$
  A^T = \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix}
  $$
* $B$ is $3 \times 2$, so $B^T$ is $2 \times 3$:
  $$
  B^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix}
  $$

---

### Step 2: Compute $AB$
Since $A$ is $2 \times 3$ and $B$ is $3 \times 2$, $AB$ is defined and has size $2 \times 2$:
$$
AB = \begin{pmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 1(1)+2(2)+3(-1) & 1(0)+2(1)+3(3) \\ 4(1)+5(2)+6(-1) & 4(0)+5(1)+6(3) \end{pmatrix} = \begin{pmatrix} 1+4-3 & 0+2+9 \\ 4+10-6 & 0+5+18 \end{pmatrix} = \begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix}
$$

---

### Step 3: Verify $(AB)^T = B^T A^T$
1. **Left-hand side $(AB)^T$:**
   $$
   (AB)^T = \begin{pmatrix} 2 & 11 \\ 8 & 23 \end{pmatrix}^T = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}
   $$
2. **Right-hand side $B^T A^T$:**
   Since $B^T$ is $2 \times 3$ and $A^T$ is $3 \times 2$, their product is $2 \times 2$:
   $$
   B^T A^T = \begin{pmatrix} 1 & 2 & -1 \\ 0 & 1 & 3 \end{pmatrix} \begin{pmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{pmatrix} = \begin{pmatrix} 1(1)+2(2)+(-1)(3) & 1(4)+2(5)+(-1)(6) \\ 0(1)+1(2)+3(3) & 0(4)+1(5)+3(6) \end{pmatrix} = \begin{pmatrix} 1+4-3 & 4+10-6 \\ 0+2+9 & 0+5+18 \end{pmatrix} = \begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}
   $$

Since both sides equal $\begin{pmatrix} 2 & 8 \\ 11 & 23 \end{pmatrix}$, we have verified that $(AB)^T = B^T A^T$.