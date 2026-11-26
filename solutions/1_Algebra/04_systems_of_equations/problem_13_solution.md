# Problem 13: Does Every Equation Add New Information?

## Question
### Given
The system

$$
x_1+x_2=10,\qquad x_2+x_3=8,\qquad x_1-x_3=2.
$$

### Find
Solve the system and check whether all three equations are independently necessary to describe the solution set. If one follows from the others, show this by calculation.

## Solution

We are given the system:
$$
\begin{cases}
x_1 + x_2 = 10, \\
x_2 + x_3 = 8, \\
x_1 - x_3 = 2.
\end{cases}
$$

### 1. Solving the System by Elimination

Form the augmented matrix:
$$
\left(\begin{array}{ccc|c}
1 & 1 & 0 & 10 \\
0 & 1 & 1 & 8 \\
1 & 0 & -1 & 2
\end{array}\right)
$$

Apply $R_3 \leftarrow R_3 - R_1$:
$$
\left(\begin{array}{ccc|c}
1 & 1 & 0 & 10 \\
0 & 1 & 1 & 8 \\
0 & -1 & -1 & -8
\end{array}\right)
$$

Apply $R_3 \leftarrow R_3 + R_2$:
$$
\left(\begin{array}{ccc|c}
1 & 1 & 0 & 10 \\
0 & 1 & 1 & 8 \\
0 & 0 & 0 & 0
\end{array}\right)
$$

Let $x_3 = t \in \mathbb{R}$ be the free variable:
* From Row 2: $x_2 + t = 8 \implies x_2 = 8 - t$.
* From Row 1: $x_1 + (8 - t) = 10 \implies x_1 = 2 + t$.

### 2. Redundancy Check by Calculation

No, not all three equations are independently necessary—**the third equation follows directly from the first two** and adds no new restriction to the solution set.

Subtracting Equation 2 from Equation 1 yields:
$$
(x_1 + x_2) - (x_2 + x_3) = 10 - 8 \implies x_1 - x_3 = 2,
$$
which is identically the third equation. Therefore, removing the third equation leaves the exact same solution set.

### Final Result

$$
\begin{pmatrix} x_1 \\ x_2 \\ x_3 \end{pmatrix} = \begin{pmatrix} 2 + t \\ 8 - t \\ t \end{pmatrix}, \quad t \in \mathbb{R} \quad (\text{Equation 3 is redundant: } \text{Eq. 1} - \text{Eq. 2} = \text{Eq. 3})
$$