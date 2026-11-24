# Problem 10: A Polynomial Through Three Points

## Solution

We want to find $p(x) = ax^2 + bx + c$ passing through $(0, 1)$, $(1, 3)$, and $(2, 9)$.

### 1. Reducing to a Linear System

Evaluating $p(x)$ at each given point yields three linear equations in the unknown coefficients $a, b, c$:
* At $(0, 1)$: $p(0) = a(0)^2 + b(0) + c = 1 \implies c = 1$
* At $(1, 3)$: $p(1) = a(1)^2 + b(1) + c = 3 \implies a + b + c = 3$
* At $(2, 9)$: $p(2) = a(2)^2 + b(2) + c = 9 \implies 4a + 2b + c = 9$

This gives the system:
$$
\begin{cases}
c = 1, \\
a + b + c = 3, \\
4a + 2b + c = 9.
\end{cases}
$$

### 2. Solving the System

Form the augmented matrix (ordering variables as $a, b, c$):
$$
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 3 \\
4 & 2 & 1 & 9 \\
0 & 0 & 1 & 1
\end{array}\right)
\xrightarrow{R_2 \leftarrow R_2 - 4R_1}
\left(\begin{array}{ccc|c}
1 & 1 & 1 & 3 \\
0 & -2 & -3 & -3 \\
0 & 0 & 1 & 1
\end{array}\right)
$$

Back-substitution:
* From Row 3: $c = 1$.
* From Row 2 ($-2b - 3c = -3$): $-2b - 3(1) = -3 \implies -2b = 0 \implies b = 0$.
* From Row 1 ($a + b + c = 3$): $a + 0 + 1 = 3 \implies a = 2$.

Thus, the polynomial is $p(x) = 2x^2 + 1$.

### 3. Verification

Check all three points:
* $p(0) = 2(0)^2 + 1 = 1$ (Passes through $(0, 1)$)
* $p(1) = 2(1)^2 + 1 = 2 + 1 = 3$ (Passes through $(1, 3)$)
* $p(2) = 2(2)^2 + 1 = 8 + 1 = 9$ (Passes through $(2, 9)$)

### Final Result

$$
p(x) = 2x^2 + 1 \quad (a = 2, \; b = 0, \; c = 1)
$$