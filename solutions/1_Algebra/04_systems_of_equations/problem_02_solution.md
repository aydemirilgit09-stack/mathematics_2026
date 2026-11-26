# Problem 2: Gaussian Elimination — One Solution

## Question
### Given
The system

$$
\begin{cases}
x+y+z=6, \\
2x-y+z=3, \\
x+2y-z=2.
\end{cases}
$$

### Find
Solve using Gaussian elimination. After solving, substitute the result into all equations and check consistency.

## Solution

We are given the system of linear equations:
$$
\begin{cases}
x + y + z = 6, \\
2x - y + z = 3, \\
x + 2y - z = 2.
\end{cases}
$$

### 1. Augmented Matrix and Forward Elimination

Write the system as an augmented matrix:
$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
2 & -1 & 1 & 3 \\
1 & 2 & -1 & 2
\end{array}\right)
$$

Eliminate $x$ from Row 2 and Row 3 using $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:
$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & -3 & -1 & -9 \\
0 & 1 & -2 & -4
\end{array}\right)
$$

Swap $R_2$ and $R_3$ ($R_2 \leftrightarrow R_3$) to obtain a pivot of $1$ in the second column:
$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & -3 & -1 & -9
\end{array}\right)
$$

Eliminate $y$ from Row 3 using $R_3 \leftarrow R_3 + 3R_2$:
$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & 0 & -7 & -21
\end{array}\right)
$$

Scale Row 3 by $-\frac{1}{7}$ ($R_3 \leftarrow -\frac{1}{7}R_3$):
$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 6 \\
0 & 1 & -2 & -4 \\
0 & 0 & 1 & 3
\end{array}\right)
$$

### 2. Back-Substitution

From Row 3:
$$
z = 3
$$

Substitute $z = 3$ into Row 2 ($y - 2z = -4$):
$$
y - 2(3) = -4 \implies y - 6 = -4 \implies y = 2
$$

Substitute $y = 2$ and $z = 3$ into Row 1 ($x + y + z = 6$):
$$
x + 2 + 3 = 6 \implies x = 1
$$

### 3. Verification

Substitute $(x, y, z) = (1, 2, 3)$ into each original equation:
* **Equation 1:** $1 + 2 + 3 = 6$ (Matches $6$)
* **Equation 2:** $2(1) - 2 + 3 = 2 - 2 + 3 = 3$ (Matches $3$)
* **Equation 3:** $1 + 2(2) - 3 = 1 + 4 - 3 = 2$ (Matches $2$)

All three equations hold, confirming the solution is consistent.

### Final Result

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix}
$$