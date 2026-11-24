# Problem 9: A System from a Sum Condition

## Solution

We are given the system of linear equations:
$$
\begin{cases}
x + y = 10, \\
2x + 5y = 32.
\end{cases}
$$

### 1. Solving the System by Elimination

Form the augmented matrix and apply $R_2 \leftarrow R_2 - 2R_1$:
$$
\left(\begin{array}{cc|c}
1 & 1 & 10 \\
2 & 5 & 32
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(\begin{array}{cc|c}
1 & 1 & 10 \\
0 & 3 & 12
\end{array}\right)
$$

From Row 2:
$$
3y = 12 \implies y = 4.
$$

Substitute $y = 4$ into Row 1:
$$
x + 4 = 10 \implies x = 6.
$$

### 2. Geometric Explanation of Uniqueness

In the Cartesian plane $\mathbb{R}^2$, each linear equation defines a straight line:
* **Line 1:** $x + y = 10 \iff y = -x + 10$ (slope $m_1 = -1$).
* **Line 2:** $2x + 5y = 32 \iff y = -\frac{2}{5}x + \frac{32}{5}$ (slope $m_2 = -\frac{2}{5}$).

Because the two lines have **different slopes** ($m_1 = -1 \neq -\frac{2}{5} = m_2$), they are neither parallel nor coincident. Two non-parallel lines in a plane intersect at **exactly one point**, which is $(6, 4)$.

### Final Result

$$
\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 6 \\ 4 \end{pmatrix} \quad (\text{unique intersection point of two non-parallel lines})
$$