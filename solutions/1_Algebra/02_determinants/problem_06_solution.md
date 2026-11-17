# Problem 06: Parameter and Invertibility

## Question
### Given
Consider the following parameter-dependent matrix:

$$
A(t) =
\begin{pmatrix}
t & 1 \\
2 & t
\end{pmatrix}.
$$

### Find
1. Find all values of $t$ for which the matrix is not invertible.
2. Explain how your answer is related to the determinant being zero.

## Solution

### 1. Compute the Determinant of $A(t)$
Using the $2 \times 2$ determinant formula $\det\begin{pmatrix} a & b \\ c & d \end{pmatrix} = ad - bc$:
$$
\det(A(t)) = t \cdot t - 1 \cdot 2 = t^2 - 2.
$$

---

### 2. Find the Values of $t$ for Non-Invertibility
**Connection to Zero Determinant:** By the invertibility theorem for square matrices, a matrix $A(t)$ fails to be invertible (is singular) if and only if its determinant equals zero, because $\det(A(t)) = 0$ implies its rows (and columns) are linearly dependent and the inverse formula $A(t)^{-1} = \frac{1}{\det(A(t))} \operatorname{adj}(A(t))$ involves division by zero.

Set $\det(A(t)) = 0$ and solve for $t$:
$$
\begin{aligned}
t^2 - 2 &= 0 \\
t^2 &= 2 \\
t &= \pm\sqrt{2}.
\end{aligned}
$$

Thus, $A(t)$ is not invertible when $t = \sqrt{2}$ or $t = -\sqrt{2}$, and it is invertible for all other real (or complex) values $t \neq \pm\sqrt{2}$.

### Verification
* For $t = \sqrt{2}$: $A(\sqrt{2}) = \begin{pmatrix} \sqrt{2} & 1 \\ 2 & \sqrt{2} \end{pmatrix}$, where $R_2 = \sqrt{2} R_1$ and $\det(A(\sqrt{2})) = (\sqrt{2})^2 - 2 = 0$.
* For $t = -\sqrt{2}$: $A(-\sqrt{2}) = \begin{pmatrix} -\sqrt{2} & 1 \\ 2 & -\sqrt{2} \end{pmatrix}$, where $R_2 = -\sqrt{2} R_1$ and $\det(A(-\sqrt{2})) = (-\sqrt{2})^2 - 2 = 0$.

### Final Results
- Not invertible for: $t = \sqrt{2}$ and $t = -\sqrt{2}$
- Invertible for: $t \neq \pm\sqrt{2}$