# Problem 15: Classifying Three Systems

## Question
### Given
**System 1**

$$
\begin{cases}
x+y=2, \\
x-y=0,
\end{cases}
$$

**System 2**

$$
\begin{cases}
x+y=2, \\
2x+2y=4,
\end{cases}
$$

**System 3**

$$
\begin{cases}
x+y=2, \\
2x+2y=5.
\end{cases}
$$

### Find
For each system, perform only as much elimination as necessary to recognize its type. Justify the classification: one solution, infinitely many solutions, or no solution.

## Solution

We perform minimal elimination on each system to classify its solution set:

### 1. System 1

$$
\begin{cases}
x + y = 2, \\
x - y = 0.
\end{cases}
$$

Augmented matrix and single elimination step ($R_2 \leftarrow R_2 - R_1$):
$$
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
1 & -1 & 0
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - R_1}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & -2 & -2
\end{array}\right)
$$

* **Classification:** **One solution** (unique solution).
* **Justification:** Both columns have non-zero pivots ($1$ in column 1 and $-2$ in column 2), leaving $0$ free variables and no contradictory rows.

### 2. System 2

$$
\begin{cases}
x + y = 2, \\
2x + 2y = 4.
\end{cases}
$$

Augmented matrix and single elimination step ($R_2 \leftarrow R_2 - 2R_1$):
$$
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
2 & 2 & 4
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 0
\end{array}\right)
$$

* **Classification:** **Infinitely many solutions**.
* **Justification:** The second row reduces to $0 = 0$ (consistent, no contradiction), leaving only $1$ pivot for $2$ unknowns, so $y$ is a free variable that can take infinitely many values.

### 3. System 3

$$
\begin{cases}
x + y = 2, \\
2x + 2y = 5.
\end{cases}
$$

Augmented matrix and single elimination step ($R_2 \leftarrow R_2 - 2R_1$):
$$
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
2 & 2 & 5
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - 2R_1}
\left(\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 1
\end{array}\right)
$$

* **Classification:** **No solution** (inconsistent).
* **Justification:** The second row reduces to $0x + 0y = 1$, i.e., $0 = 1$, which is a contradiction.

### Final Result

$$
\begin{aligned}
\text{System 1:} & \quad \text{One solution (2 pivots for 2 unknowns, consistent).} \\
\text{System 2:} & \quad \text{Infinitely many solutions (1 pivot for 2 unknowns, row } 0 = 0\text{).} \\
\text{System 3:} & \quad \text{No solution (contradictory row } 0 = 1\text{).}
\end{aligned}
$$