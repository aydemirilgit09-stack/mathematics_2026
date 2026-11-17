# Problem 15: Two Methods for Solving the Same System

## Question
### Given
For

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
7 \\
8 \\
\end{pmatrix}
$$

### Find
1. Solve $Ax = b$ using $x = A^{-1}b$.
2. Solve $Ax = b$ using Gaussian elimination.
3. Compare both solutions, the number of essential steps, and state which method was simpler in this example.

## Solution

### Method 1: Using the Inverse Matrix ($x = A^{-1}b$)
1. **Compute $\det(A)$:**
   $$
   \det(A) = (2)(3) - (1)(1) = 6 - 1 = 5 \neq 0.
   $$
2. **Find $A^{-1}$:**
   $$
   A^{-1} = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}.
   $$
3. **Multiply $A^{-1}b$:**
   $$
   x = A^{-1}b = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix} \begin{pmatrix} 7 \\ 8 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 21 - 8 \\ -7 + 16 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 13 \\ 9 \end{pmatrix} = \begin{pmatrix} \frac{13}{5} \\ \frac{9}{5} \end{pmatrix}.
   $$

---

### Method 2: Using Gaussian Elimination
Form the augmented matrix $[A \mid b]$:
$$
\left[\begin{array}{cc|c}
2 & 1 & 7 \\
1 & 3 & 8
\end{array}\right]
$$

1. **Swap rows 1 and 2 ($R_1 \leftrightarrow R_2$) to get a leading $1$:**
   $$
   \left[\begin{array}{cc|c}
   1 & 3 & 8 \\
   2 & 1 & 7
   \end{array}\right]
   $$

2. **Eliminate below the pivot ($R_2 \leftarrow R_2 - 2R_1$):**
   $$
   \left[\begin{array}{cc|c}
   1 & 3 & 8 \\
   0 & -5 & -9
   \end{array}\right]
   $$

3. **Back-substitution:**
   * From row 2: $-5x_2 = -9 \implies x_2 = \frac{9}{5}$.
   * Substitute into row 1: $x_1 + 3\left(\frac{9}{5}\right) = 8 \implies x_1 = \frac{40}{5} - \frac{27}{5} = \frac{13}{5}$.

Thus, $x = \begin{pmatrix} \frac{13}{5} \\ \frac{9}{5} \end{pmatrix}$.

---

### 3. Comparison of Methods
* **Agreement of Solutions:** Both methods produce the identical unique solution $x = \begin{pmatrix} \frac{13}{5} \\ \frac{9}{5} \end{pmatrix}$.
* **Number of Essential Steps:**
  * *Inverse method:* 3 main steps (compute $\det(A)$, form $A^{-1}$, multiply $A^{-1}b$).
  * *Gaussian elimination:* 3 main steps (swap rows, eliminate $x_1$ in row 2, back-substitute).
* **Which Method Was Simpler Here:** For a single $2 \times 2$ system, **both are nearly equal in effort**, though **Gaussian elimination is slightly simpler and faster** because it avoids fractions until the final back-substitution step and requires fewer total arithmetic operations than computing an entire inverse matrix first (whereas $A^{-1}b$ would only become preferable if we needed to solve $Ax = b$ repeatedly for many different right-hand sides $b$).

### Verification
$$
Ax = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix} \begin{pmatrix} \frac{13}{5} \\ \frac{9}{5} \end{pmatrix} = \begin{pmatrix} \frac{26 + 9}{5} \\ \frac{13 + 27}{5} \end{pmatrix} = \begin{pmatrix} \frac{35}{5} \\ \frac{40}{5} \end{pmatrix} = \begin{pmatrix} 7 \\ 8 \end{pmatrix} = b.
$$

### Final Result
$$
x = \begin{pmatrix} \frac{13}{5} \\ \frac{9}{5} \end{pmatrix}
$$