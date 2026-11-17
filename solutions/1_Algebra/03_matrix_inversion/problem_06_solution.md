# Problem 06: Solving a System Using the Inverse

## Question
### Given
Consider the linear system $Ax = b$, where

$$
A=
\begin{pmatrix}
2 & 1 \\
1 & 3 \\
\end{pmatrix},\qquad b=
\begin{pmatrix}
5 \\
7 \\
\end{pmatrix}.
$$

### Find
Solve $Ax = b$ using $x = A^{-1}b$, then substitute the resulting vector back into $Ax = b$ to check the result.

## Solution

### Step 1: Compute $A^{-1}$
First, check the determinant of $A$:
$$
\det(A) = (2)(3) - (1)(1) = 6 - 1 = 5 \neq 0.
$$
Using the $2 \times 2$ inverse formula:
$$
A^{-1} = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix}.
$$

---

### Step 2: Solve for $x$ Using $x = A^{-1}b$
Multiply both sides of $Ax = b$ on the left by $A^{-1}$:
$$
x = A^{-1}b = \frac{1}{5} \begin{pmatrix} 3 & -1 \\ -1 & 2 \end{pmatrix} \begin{pmatrix} 5 \\ 7 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 3(5) + (-1)(7) \\ (-1)(5) + 2(7) \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 15 - 7 \\ -5 + 14 \end{pmatrix} = \frac{1}{5} \begin{pmatrix} 8 \\ 9 \end{pmatrix} = \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix}.
$$

---

### Verification
Substitute $x = \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix}$ back into $Ax$:
$$
Ax = \begin{pmatrix} 2 & 1 \\ 1 & 3 \end{pmatrix} \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix} = \begin{pmatrix} 2\left(\frac{8}{5}\right) + 1\left(\frac{9}{5}\right) \\ 1\left(\frac{8}{5}\right) + 3\left(\frac{9}{5}\right) \end{pmatrix} = \begin{pmatrix} \frac{16 + 9}{5} \\ \frac{8 + 27}{5} \end{pmatrix} = \begin{pmatrix} \frac{25}{5} \\ \frac{35}{5} \end{pmatrix} = \begin{pmatrix} 5 \\ 7 \end{pmatrix} = b.
$$
Both equations are satisfied, confirming the solution.

### Final Result
$$
x = \begin{pmatrix} \frac{8}{5} \\ \frac{9}{5} \end{pmatrix}
$$