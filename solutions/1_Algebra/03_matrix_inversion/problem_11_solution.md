# Problem 11: Parameter and Invertibility

## Question
### Given
Consider the parameter-dependent matrix

$$
A(t)=
\begin{pmatrix}
1 & t \\
t & 1 \\
\end{pmatrix}.
$$

### Find
1. Find all values of $t$ for which $A(t)$ is invertible.
2. Give an explicit formula for $A(t)^{-1}$ whenever it exists.
3. Explain what happens to this formula at the excluded values of $t$.

## Solution

### 1. Condition for Invertibility
Compute the determinant of $A(t)$:
$$
\det(A(t)) = (1)(1) - (t)(t) = 1 - t^2.
$$

A square matrix is invertible if and only if $\det(A(t)) \neq 0$:
$$
1 - t^2 \neq 0 \implies t^2 \neq 1 \implies t \neq 1 \quad \text{and} \quad t \neq -1.
$$
Thus, $A(t)$ is invertible for all $t \in \mathbb{R} \setminus \{-1, 1\}$.

---

### 2. Explicit Formula for $A(t)^{-1}$
Using the $2 \times 2$ inverse formula $M^{-1} = \frac{1}{\det(M)} \begin{pmatrix} d & -b \\ -c & a \end{pmatrix}$ for $t \neq \pm 1$:
$$
A(t)^{-1} = \frac{1}{1 - t^2} \begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix} = \begin{pmatrix} \frac{1}{1 - t^2} & -\frac{t}{1 - t^2} \\ -\frac{t}{1 - t^2} & \frac{1}{1 - t^2} \end{pmatrix}.
$$

---

### 3. Behavior at the Excluded Values ($t = 1$ and $t = -1$)
* **In the formula:** When $t = 1$ or $t = -1$, the denominator $1 - t^2$ equals $0$, causing **division by zero** in every entry of the formula (as $t \to \pm 1$, the entries diverge to $\pm\infty$).
* **Structurally in $A(t)$:**
  * At $t = 1$: $A(1) = \begin{pmatrix} 1 & 1 \\ 1 & 1 \end{pmatrix}$, where $R_2 = R_1$ (identical rows).
  * At $t = -1$: $A(-1) = \begin{pmatrix} 1 & -1 \\ -1 & 1 \end{pmatrix}$, where $R_2 = -R_1$ (proportional rows).
  In both cases, the rows are linearly dependent and $\det(A(\pm 1)) = 0$, so no inverse exists.

### Verification
For $t \neq \pm 1$:
$$
A(t)A(t)^{-1} = \frac{1}{1 - t^2} \begin{pmatrix} 1 & t \\ t & 1 \end{pmatrix} \begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix} = \frac{1}{1 - t^2} \begin{pmatrix} 1 - t^2 & -t + t \\ t - t & -t^2 + 1 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2.
$$

### Final Results
- Invertible for: $t \neq \pm 1$
- $A(t)^{-1} = \frac{1}{1 - t^2} \begin{pmatrix} 1 & -t \\ -t & 1 \end{pmatrix}$