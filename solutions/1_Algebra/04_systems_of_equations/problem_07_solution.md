# Problem 7: Choosing a Method Deliberately

## Solution

### 1. Triangular System — Direct Back-Substitution

We are given:
$$
\begin{cases}
2x - y = 3, \\
4y = 8.
\end{cases}
$$

* **Chosen Method:** **Direct back-substitution** (no forward elimination or matrix inversion needed).
* **Justification:** The coefficient matrix $\begin{pmatrix} 2 & -1 \\ 0 & 4 \end{pmatrix}$ is already in upper-triangular form. Forward elimination is completely unnecessary because the lower-left entry is already $0$, and computing $A^{-1}$ would do extra work for a single right-hand side.
* **Complete Execution:**
  From the second equation:
  $$
  4y = 8 \implies y = 2.
  $$
  Substitute $y = 2$ into the first equation:
  $$
  2x - 2 = 3 \implies 2x = 5 \implies x = \frac{5}{2}.
  $$
  **Solution for Case 1:** $\begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 5/2 \\ 2 \end{pmatrix}$.

### 2. Three Systems $A\mathbf{x} = b_i$ with $A^{-1}$ Already Known

* **Chosen Method:** **Direct matrix-vector multiplication** $\mathbf{x}_i = A^{-1}b_i$ for each $i = 1, 2, 3$.
* **Plan and Reusability:**
  * The expensive part of using an inverse—computing $A^{-1}$—has already been done and is **reused** across all three right-hand sides $b_1, b_2, b_3$.
  * Rather than running Gaussian elimination three separate times on the same matrix $A$, we simply perform three fast matrix-vector products: $\mathbf{x}_1 = A^{-1}b_1$, $\mathbf{x}_2 = A^{-1}b_2$, and $\mathbf{x}_3 = A^{-1}b_3$.

### 3. Single $3 \times 3$ System Without $A^{-1}$ Given

* **Chosen Method:** **Gaussian elimination** on the augmented matrix $(A \mid b)$ followed by back-substitution.
* **Plan and Unnecessary Computation:**
  * Reduce $(A \mid b)$ to row echelon form using elementary row operations, then solve for the unknowns from bottom to top.
  * Computing $A^{-1}$ is **unnecessary** here because there is only **one** right-hand side vector $b$. Finding $A^{-1}$ requires solving three systems simultaneously (reducing $(A \mid I_3)$), which roughly triples the arithmetic effort compared to solving $(A \mid b)$ directly.

### Final Result

$$
\begin{aligned}
\text{1. } & \text{Back-substitution directly gives } \begin{pmatrix} x \\ y \end{pmatrix} = \begin{pmatrix} 5/2 \\ 2 \end{pmatrix}. \\
\text{2. } & \text{Multiply } \mathbf{x}_i = A^{-1}b_i \text{ for } i = 1, 2, 3 \text{ (reusing the precomputed } A^{-1}\text{)}. \\
\text{3. } & \text{Gaussian elimination with back-substitution (computing } A^{-1} \text{ is unnecessary for a single } b\text{)}.
\end{aligned}
$$