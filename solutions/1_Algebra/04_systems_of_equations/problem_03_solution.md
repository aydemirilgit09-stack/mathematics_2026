# Problem 3: Inconsistent System

## Question
### Given
The system

$$
\begin{cases}
x+2y=3, \\
2x+4y=7.
\end{cases}
$$

### Find
Solve or show that the system is inconsistent. Show how the contradiction appears in the matrix after elimination and interpret it in terms of equations.

## Solution

We are given the system:
$$
\begin{cases}
x + 2y = 3, \\
2x + 4y = 7.
\end{cases}
$$

### 1. Elimination on the Augmented Matrix

Form the augmented matrix:
$$
\left(\begin{array}{cc|c}
1 & 2 & 3 \\
2 & 4 & 7
\end{array}\right)
$$

Apply the row operation $R_2 \leftarrow R_2 - 2R_1$:
$$
\left(\begin{array}{cc|c}
1 & 2 & 3 \\
0 & 0 & 1
\end{array}\right)
$$

### 2. Interpretation of the Contradiction

* **Matrix view:** The second row has all zeros in the coefficient part ($0, 0$) and a non-zero entry ($1$) in the right-hand side column.
* **Equation view:** Translating the second row back into an equation gives:
$$
0x + 0y = 1 \implies 0 = 1,
$$
which is a false statement (contradiction) for all real numbers $x$ and $y$.

### Final Result

$$
\text{The system is inconsistent and has no solution.}
$$