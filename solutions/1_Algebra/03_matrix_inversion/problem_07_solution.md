# Problem 07: Inverse of a Product

## Question
### Given
For

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
2 & 0 \\
0 & 3 \\
\end{pmatrix}
$$

### Find
1. Compute $(AB)^{-1}$ and $B^{-1}A^{-1}$.
2. Verify that both results are identical and explain the meaning of the reversed order.

## Solution

### 1. Compute $(AB)^{-1}$ Directly
First, compute the product $AB$:
$$
AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 0 & 3 \end{pmatrix} = \begin{pmatrix} 2 & 3 \\ 0 & 3 \end{pmatrix}.
$$
Since $\det(AB) = (2)(3) - (3)(0) = 6$, its inverse is:
$$
(AB)^{-1} = \frac{1}{6} \begin{pmatrix} 3 & -3 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3} \end{pmatrix}.
$$

---

### 2. Compute $B^{-1}A^{-1}$
Find $A^{-1}$ and $B^{-1}$ separately:
* $\det(A) = 1 \implies A^{-1} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}$.
* $\det(B) = 6 \implies B^{-1} = \frac{1}{6}\begin{pmatrix} 3 & 0 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & \frac{1}{3} \end{pmatrix}$.

Now multiply $B^{-1}A^{-1}$:
$$
B^{-1}A^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & \frac{1}{3} \end{pmatrix} \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} \frac{1}{2}(1) + 0(0) & \frac{1}{2}(-1) + 0(1) \\ 0(1) + \frac{1}{3}(0) & 0(-1) + \frac{1}{3}(1) \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3} \end{pmatrix}.
$$

---

### 3. Comparison and Meaning of the Reversed Order
* **Comparison:** $(AB)^{-1} = B^{-1}A^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3} \end{pmatrix}$.
* **Meaning of Reversed Order ("Socks and Shoes" Rule):** Applying $AB$ to a vector $x$ means first applying $B$ and then applying $A$ ($A(Bx)$). To undo this two-step process and recover $x$, we must undo the **last** operation ($A$) first by multiplying by $A^{-1}$, and then undo the **first** operation ($B$) by multiplying by $B^{-1}$:
  $$
  (B^{-1}A^{-1})(AB) = B^{-1}(A^{-1}A)B = B^{-1}IB = B^{-1}B = I.
  $$

### Final Result
$$
(AB)^{-1} = B^{-1}A^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & \frac{1}{3} \end{pmatrix}
$$