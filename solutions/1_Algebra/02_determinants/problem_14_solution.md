# Problem 14: A System of Equations and the Determinant

## Question
### Given
Consider the linear system $Ax = b$, where

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}.
$$

### Find
1. Determine for which values of $k$ the system has **exactly one solution** for every $b \in \mathbb{R}^2$.
2. For the remaining exceptional value of $k$, give:
   - an example of a right-hand side vector $b$ for which the system has **infinitely many solutions**, and
   - an example of a right-hand side vector $b$ for which the system has **no solution**.

## Solution

### 1. Condition for a Unique Solution
A square linear system $Ax = b$ has a unique solution $x = A^{-1}b$ for every right-hand side $b$ if and only if $A$ is invertible, i.e., $\det(A) \neq 0$.

Compute $\det(A)$:
$$
\det(A) = (1)(4) - (2)(k) = 4 - 2k.
$$

Set $\det(A) \neq 0$:
$$
4 - 2k \neq 0 \implies 2k \neq 4 \implies k \neq 2.
$$
Thus, the system has **exactly one solution for every $b$ when $k \neq 2$**.

---

### 2. Analysis of the Exceptional Case $k = 2$
When $k = 2$, $\det(A) = 0$ and the matrix becomes:
$$
A =
\begin{pmatrix}
1 & 2 \\
2 & 4
\end{pmatrix},
$$
whose second row is twice the first row ($R_2 = 2R_1$). Writing $x = \begin{pmatrix} x_1 \\ x_2 \end{pmatrix}$ and $b = \begin{pmatrix} b_1 \\ b_2 \end{pmatrix}$, the system is:
$$
\begin{cases}
x_1 + 2x_2 = b_1 \\
2x_1 + 4x_2 = b_2.
\end{cases}
$$

* **Example 1: Infinitely Many Solutions**
  Choose $b = \begin{pmatrix} 2 \\ 4 \end{pmatrix}$ (so $b_2 = 2b_1$). The augmented matrix reduces to:
  $$
  \left(\begin{array}{cc|c} 1 & 2 & 2 \\ 2 & 4 & 4 \end{array}\right)
  \xrightarrow{R_2 \leftarrow R_2 - 2R_1}
  \left(\begin{array}{cc|c} 1 & 2 & 2 \\ 0 & 0 & 0 \end{array}\right).
  $$
  Both equations represent the same line $x_1 + 2x_2 = 2$, giving infinitely many solutions $(x_1, x_2) = (2 - 2t, t)$ for any $t \in \mathbb{R}$.

* **Example 2: No Solution (Inconsistent System)**
  Choose $b = \begin{pmatrix} 2 \\ 5 \end{pmatrix}$ (so $b_2 \neq 2b_1$). The augmented matrix reduces to:
  $$
  \left(\begin{array}{cc|c} 1 & 2 & 2 \\ 2 & 4 & 5 \end{array}\right)
  \xrightarrow{R_2 \leftarrow R_2 - 2R_1}
  \left(\begin{array}{cc|c} 1 & 2 & 2 \\ 0 & 0 & 1 \end{array}\right).
  $$
  The second row gives the contradiction $0 = 1$, so no solution exists.

### Final Results
- Unique solution for every $b$: $k \neq 2$
- For $k = 2$: $b = \begin{pmatrix} 2 \\ 4 \end{pmatrix}$ gives infinitely many solutions; $b = \begin{pmatrix} 2 \\ 5 \end{pmatrix}$ gives no solution.