# Problem 14: A Small Change in the Right-Hand Side

## Solution

We compare the two overdetermined systems:
$$
\text{System A: } \begin{cases} x + y = 2, \\ 2x - y = 1, \\ 3x = 3, \end{cases}
\qquad
\text{System B: } \begin{cases} x + y = 2, \\ 2x - y = 1, \\ 3x = 3.1. \end{cases}
$$

### 1. Consistency Check for System A

Reduce the augmented matrix:
$$
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
2 & -1 & 1 \\
3 & 0 & 3
\end{array}\right)
\xrightarrow{\substack{R_2 \leftarrow R_2 - 2R_1 \\ R_3 \leftarrow R_3 - 3R_1}}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -3 & -3 \\
0 & -3 & -3
\end{array}\right)
\xrightarrow{R_3 \leftarrow R_3 - R_2}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -3 & -3 \\
0 & 0 & 0
\end{array}\right)
$$

* From Row 2: $-3y = -3 \implies y = 1$.
* From Row 1: $x + 1 = 2 \implies x = 1$.
* Row 3 becomes $0 = 0$.

System A is **consistent** with the unique solution $(x, y) = (1, 1)$.

### 2. Consistency Check for System B

Reduce the augmented matrix using the exact same row operations:
$$
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
2 & -1 & 1 \\
3 & 0 & 3.1
\end{array}\right)
\xrightarrow{\substack{R_2 \leftarrow R_2 - 2R_1 \\ R_3 \leftarrow R_3 - 3R_1}}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -3 & -3 \\
0 & -3 & -2.9
\end{array}\right)
\xrightarrow{R_3 \leftarrow R_3 - R_2}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -3 & -3 \\
0 & 0 & 0.1
\end{array}\right)
$$

Row 3 reads $0 = 0.1$, which is a contradiction. Thus, System B is **inconsistent (no solution)**.

### 3. Why a Small Change Changes the System Type

Notice that the third left-hand side is the sum of the first two: $(x + y) + (2x - y) = 3x$. The first two equations alone already force $x = 1$ and $y = 1$, which uniquely fixes $3x = 3$. In System A, the third equation $3x = 3$ agrees with this intersection point (geometrically, all three lines pass through $(1, 1)$). Changing the right-hand side slightly from $3$ to $3.1$ shifts the third line to $x = \frac{3.1}{3} \neq 1$, so the three lines no longer share a common intersection point and the system becomes inconsistent.

### Final Result

$$
\text{System A: consistent, unique solution } \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 1 \\ 1 \end{pmatrix}; \qquad
\text{System B: inconsistent (no solution, since } 0 = 0.1\text{).}
$$