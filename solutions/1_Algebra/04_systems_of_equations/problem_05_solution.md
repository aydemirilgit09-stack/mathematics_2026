# Problem 5: Row Echelon Form and Number of Solutions

## Solution

We are given the augmented matrix in row echelon form:
$$
\left(\begin{array}{ccc|c}
1 & 2 & -1 & 3 \\
0 & 1 & 2 & 1 \\
0 & 0 & 0 & 0
\end{array}\right)
$$

### 1. Number of Solutions and Free Variables

* **Consistency:** The zero row $(0 \; 0 \; 0 \mid 0)$ corresponds to $0 = 0$, so there is no contradiction and the system is consistent.
* **Counting free variables:** There are $n = 3$ unknowns ($x_1, x_2, x_3$) and $r = 2$ pivot columns (columns 1 and 2). Therefore, the number of free variables is:
$$
n - r = 3 - 2 = 1.
$$
* Since column 3 lacks a pivot, $x_3$ can be chosen freely. Because a free variable can take any real value, the system has **infinitely many solutions**.

### 2. Parametric Form

Let $x_3 = t \in \mathbb{R}$.

From Row 2 ($x_2 + 2x_3 = 1$):
$$
x_2 = 1 - 2t
$$

From Row 1 ($x_1 + 2x_2 - x_3 = 3$):
$$
x_1 + 2(1 - 2t) - t = 3 \implies x_1 + 2 - 5t = 3 \implies x_1 = 1 + 5t
$$

### Final Result

$$
\text{Infinitely many solutions (1 free variable } x_3 = t\text{):} \quad \begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = \begin{pmatrix} 1 + 5t \\ 1 - 2t \\ t \end{pmatrix}, \quad t \in \mathbb{R}
$$