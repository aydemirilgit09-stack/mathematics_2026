# Problem 4: Infinitely Many Solutions

## Solution

We are given the system:
$$
\begin{cases}
x + y + z = 2, \\
2x + 2y + 2z = 4, \\
x - y + z = 0.
\end{cases}
$$

### 1. Gaussian Elimination

Write the augmented matrix:
$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
2 & 2 & 2 & 4 \\
1 & -1 & 1 & 0
\end{array}\right)
$$

Apply $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:
$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & 0 & 0 & 0 \\
0 & -2 & 0 & -2
\end{array}\right)
$$

Swap $R_2$ and $R_3$ ($R_2 \leftrightarrow R_3$) and scale the new $R_2$ by $-\frac{1}{2}$:
$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 2 \\
0 & 1 & 0 & 1 \\
0 & 0 & 0 & 0
\end{array}\right)
$$

### 2. Parametric Description

* **Pivot variables:** $x$ (column 1) and $y$ (column 2).
* **Free variable:** $z$ (column 3 has no pivot). Let $z = t \in \mathbb{R}$.

From Row 2:
$$
y = 1
$$

From Row 1 ($x + y + z = 2$):
$$
x + 1 + t = 2 \implies x = 1 - t
$$

Thus, the general solution in parametric form is:
$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 1 - t \\ 1 \\ t \end{pmatrix} = \begin{pmatrix} 1 \\ 1 \\ 0 \end{pmatrix} + t \begin{pmatrix} -1 \\ 0 \\ 1 \end{pmatrix}, \quad t \in \mathbb{R}.
$$

### 3. Verification for a Chosen Parameter Value

Choose $t = 2$, which gives the point $(x, y, z) = (-1, 1, 2)$. Substitute into the original equations:
* **Equation 1:** $-1 + 1 + 2 = 2$ (Matches $2$)
* **Equation 2:** $2(-1) + 2(1) + 2(2) = -2 + 2 + 4 = 4$ (Matches $4$)
* **Equation 3:** $-1 - 1 + 2 = 0$ (Matches $0$)

### Final Result

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 1 - t \\ 1 \\ t \end{pmatrix}, \quad t \in \mathbb{R} \quad (\text{free variable: } z = t)
$$