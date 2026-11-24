# Problem 12: Homogeneous System

## Solution

We are given the homogeneous system of linear equations:
$$\begin{cases} x + 2y - z = 0, \\ 2x + 4y - 2z = 0, \\ x - y + 2z = 0. \end{cases}$$

### 1. Gaussian Elimination

Write the augmented matrix:
$$\left(\begin{array}{ccc\|c} 1 & 2 & -1 & 0 \\ 2 & 4 & -2 & 0 \\ 1 & -1 & 2 & 0 \end{array}\right)$$

Apply $R_2 \leftarrow R_2 - 2R_1$ and $R_3 \leftarrow R_3 - R_1$:
$$\left(\begin{array}{ccc\|c} 1 & 2 & -1 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & -3 & 3 & 0 \end{array}\right)$$

Swap $R_2$ and $R_3$ ($R_2 \leftrightarrow R_3$) and scale the new $R_2$ by $-\frac{1}{3}$:
$$\left(\begin{array}{ccc\|c} 1 & 2 & -1 & 0 \\ 0 & 1 & -1 & 0 \\ 0 & 0 & 0 & 0 \end{array}\right)$$

### 2. Parametric Description of All Solutions

* **Pivot variables:** $x$ and $y$.
* **Free variable:** $z = t \in \mathbb{R}$.

From Row 2 ($y - z = 0$):
$$y = t$$

From Row 1 ($x + 2y - z = 0$):
$$x + 2t - t = 0 \implies x + t = 0 \implies x = -t$$

Thus, all solutions are given by:
$$\begin{pmatrix} x \\ y \\ z \end{pmatrix} = t \begin{pmatrix} -1 \\ 1 \\ 1 \end{pmatrix}, \quad t \in \mathbb{R}.$$

### 3. Why $(0, 0, 0)$ Always Satisfies a Homogeneous System

In a homogeneous system $A\mathbf{x} = \mathbf{0}$, every equation has the linear form $a_{i1}x + a_{i2}y + a_{i3}z = 0$ with zero constant term on the right-hand side. Substituting $(x, y, z) = (0, 0, 0)$ makes every term equal to $a_{ij} \cdot 0 = 0$, so the left-hand side sums to $0$, which always equals the right-hand side $0$ (in matrix form, $A\mathbf{0} = \mathbf{0}$ holds for every matrix $A$).

### Final Result

$$\begin{pmatrix} x \\ y \\ z \end{pmatrix} = t \begin{pmatrix} -1 \\ 1 \\ 1 \end{pmatrix}, \quad t \in \mathbb{R}$$