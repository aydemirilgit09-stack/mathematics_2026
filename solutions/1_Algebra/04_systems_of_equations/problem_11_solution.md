# Problem 11: A Parameter in a System of Three Equations

## Solution

We analyze the system depending on the parameter $t \in \mathbb{R}$:
$$
\begin{cases}
x + y + z = 1, \\
x + ty + z = 2, \\
x + y + tz = 3.
\end{cases}
$$

### 1. Forward Elimination

Write the augmented matrix:
$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
1 & t & 1 & 2 \\
1 & 1 & t & 3
\end{array}\right)
$$

Eliminate $x$ from Row 2 and Row 3 using $R_2 \leftarrow R_2 - R_1$ and $R_3 \leftarrow R_3 - R_1$:
$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
0 & t - 1 & 0 & 1 \\
0 & 0 & t - 1 & 2
\end{array}\right)
$$

To proceed with back-substitution, we would normally divide Row 2 and Row 3 by $(t - 1)$. This standard calculation step ceases to be valid when $t - 1 = 0$, i.e., **$t = 1$**.

### 2. Case Analysis

* **Case 1: $t = 1$**
  Substituting $t = 1$ into the reduced matrix gives:
  $$
  \left(\begin{array}{ccc|c}
  1 & 1 & 1 & 1 \\
  0 & 0 & 0 & 1 \\
  0 & 0 & 0 & 2
  \end{array}\right)
  $$
  Row 2 reads $0 = 1$ and Row 3 reads $0 = 2$, both of which are contradictions. Hence, for $t = 1$, the system is **inconsistent (no solution)**.

* **Case 2: $t \neq 1$**
  Since $t - 1 \neq 0$, we can safely divide Row 2 and Row 3 by $t - 1$:
  $$
  y = \frac{1}{t - 1}, \qquad z = \frac{2}{t - 1}.
  $$
  Substituting into Row 1 ($x + y + z = 1$):
  $$
  x = 1 - \frac{1}{t - 1} - \frac{2}{t - 1} = 1 - \frac{3}{t - 1} = \frac{t - 4}{t - 1}.
  $$
  Therefore, for every $t \neq 1$, the system has **exactly one solution**.

### Final Result

$$
\begin{cases}
t = 1: & \text{no solution (inconsistent)}, \\
t \neq 1: & \text{exactly one solution } \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} \frac{t - 4}{t - 1} \\ \frac{1}{t - 1} \\ \frac{2}{t - 1} \end{pmatrix}.
\end{cases}
$$