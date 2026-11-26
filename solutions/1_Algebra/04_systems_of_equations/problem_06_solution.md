# Problem 6: A System with a Parameter — Which Cases Actually Occur?

## Question
### Given
The system

$$
\begin{cases}
x+y=2, \\
ax+ay=4.
\end{cases}
$$

### Find
Analyze, depending on the parameter $a$, among the possibilities exactly one solution, infinitely many solutions, and no solution. Determine which actually occur and for which values of $a$. If one type cannot occur, explain why.

## Solution

We analyze the system depending on the parameter $a \in \mathbb{R}$:
$$
\begin{cases}
x + y = 2, \\
ax + ay = 4.
\end{cases}
$$

### 1. Elimination Step

Form the augmented matrix and apply $R_2 \leftarrow R_2 - aR_1$:
$$
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
a & a & 4
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - aR_1}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 4 - 2a
\end{array}\right)
$$

The second row represents the equation $0 \cdot x + 0 \cdot y = 4 - 2a$.

### 2. Case Analysis

* **Case 1: $a = 2$**
  The right-hand side becomes $4 - 2(2) = 0$, giving the row $(0 \; 0 \mid 0)$. The system reduces to a single equation $x + y = 2$, where $y = t$ is free and $x = 2 - t$. Thus, there are **infinitely many solutions**.

* **Case 2: $a \neq 2$**
  The right-hand side $4 - 2a \neq 0$, giving the contradiction $0 = 4 - 2a \neq 0$. Thus, the system has **no solution** (inconsistent).

* **Why "exactly one solution" cannot occur:**
  For a $2 \times 2$ system to have a unique solution, the coefficient matrix must have $2$ linearly independent rows (rank $2$). Here, the second row $(a, a) = a(1, 1)$ is always a scalar multiple of the first row $(1, 1)$ for every $a \in \mathbb{R}$, so the determinant of the coefficient matrix is identically zero ($\det A = 1\cdot a - 1\cdot a = 0$).

### Final Result

$$
\begin{cases}
a = 2: & \text{infinitely many solutions } (x, y) = (2 - t, t), \; t \in \mathbb{R}, \\
a \neq 2: & \text{no solution}, \\
\text{Exact one solution:} & \text{never occurs because the rows of } A \text{ are linearly dependent for all } a.
\end{cases}
$$