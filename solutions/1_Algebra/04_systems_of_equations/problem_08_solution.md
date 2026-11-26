# Problem 8: Two Systems with the Same Coefficient Matrix

## Question
### Given
The systems

$$
\begin{cases}
2x+y=5, \\
x-y=1,
\end{cases}
$$

and

$$
\begin{cases}
2x+y=1, \\
x-y=4.
\end{cases}
$$

### Find
Solve both systems by elimination. Compare the successive elimination steps. Identify which part of the calculation is the same in both cases and explain why.

## Solution

We solve both systems by elimination:
$$
\text{System 1: } \begin{cases} 2x + y = 5, \\ x - y = 1, \end{cases}
\qquad
\text{System 2: } \begin{cases} 2x + y = 1, \\ x - y = 4. \end{cases}
$$

### 1. Solving System 1

Augmented matrix:
$$
\left(\begin{array}{cc|c}
2 & 1 & 5 \\
1 & -1 & 1
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - \frac{1}{2}R_1}
\left(\begin{array}{cc|c}
2 & 1 & 5 \\
0 & -\frac{3}{2} & -\frac{3}{2}
\end{array}\right)
$$

Back-substitution:
* From Row 2: $-\frac{3}{2}y = -\frac{3}{2} \implies y = 1$.
* From Row 1: $2x + 1 = 5 \implies 2x = 4 \implies x = 2$.

Solution to System 1: $\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$.

### 2. Solving System 2

Augmented matrix:
$$
\left(\begin{array}{cc|c}
2 & 1 & 1 \\
1 & -1 & 4
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - \frac{1}{2}R_1}
\left(\begin{array}{cc|c}
2 & 1 & 1 \\
0 & -\frac{3}{2} & \frac{7}{2}
\end{array}\right)
$$

Back-substitution:
* From Row 2: $-\frac{3}{2}y = \frac{7}{2} \implies y = -\frac{7}{3}$.
* From Row 1: $2x - \frac{7}{3} = 1 \implies 2x = \frac{10}{3} \implies x = \frac{5}{3}$.

Solution to System 2: $\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 5/3 \\ -7/3 \end{pmatrix}$.

### 3. Comparison of Elimination Steps

* **What is the same:** Both the sequence of elementary row operations ($R_2 \leftarrow R_2 - \frac{1}{2}R_1$) and the resulting reduced coefficient matrix $\begin{pmatrix} 2 & 1 \\ 0 & -3/2 \end{pmatrix}$ are identical in both cases.
* **Why:** Which row operations are needed to create zeros below the pivots depends **only on the entries of the coefficient matrix $A$**, completely independently of the right-hand side vector $b$. The right-hand side merely undergoes the same linear combinations along for the ride.

### Final Result

$$
\text{System 1: } \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 2 \\ 1 \end{pmatrix}, \qquad
\text{System 2: } \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 5/3 \\ -7/3 \end{pmatrix}
$$