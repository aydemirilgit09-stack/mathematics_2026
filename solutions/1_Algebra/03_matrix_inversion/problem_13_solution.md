# Problem 13: Undoing a Composite Transformation

## Question
### Given
The matrices

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad H=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}
$$

describe nonuniform horizontal scaling and horizontal shear, respectively. Let $T = HS$.

### Find
1. Find $T^{-1}$ in two ways:
   - First compute $T = HS$, then find its inverse directly.
   - Use the product inverse rule $(HS)^{-1} = S^{-1}H^{-1}$.
2. Compare the results, and additionally compute $H^{-1}S^{-1}$ to verify that the incorrect order yields a different matrix.
3. Explain the rule: *"When undoing a composition of operations, we undo them from the end."*

## Solution

### 1. Method 1: Compute $T = HS$ First, Then Invert $T$
Multiply $H$ and $S$:
$$
T = HS = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 0 & 1 \end{pmatrix}.
$$
Now compute $T^{-1}$ using the $2 \times 2$ inverse formula ($\det(T) = 2 \cdot 1 - 1 \cdot 0 = 2$):
$$
T^{-1} = \frac{1}{2} \begin{pmatrix} 1 & -1 \\ 0 & 2 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & 1 \end{pmatrix}.
$$

---

### 2. Method 2: Use $(HS)^{-1} = S^{-1}H^{-1}$
Compute the individual inverses:
* $S^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 1 \end{pmatrix}$ (since $\det(S) = 2$).
* $H^{-1} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix}$ (since $\det(H) = 1$).

Multiply $S^{-1}$ on the left of $H^{-1}$:
$$
S^{-1}H^{-1} = \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} \frac{1}{2}(1) + 0(0) & \frac{1}{2}(-1) + 0(1) \\ 0(1) + 1(0) & 0(-1) + 1(1) \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & 1 \end{pmatrix}.
$$
Both methods produce the exact same matrix $T^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & 1 \end{pmatrix}$.

---

### 3. Check the Incorrect Order $H^{-1}S^{-1}$ and Explain the Rule
Compute $H^{-1}S^{-1}$:
$$
H^{-1}S^{-1} = \begin{pmatrix} 1 & -1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} \frac{1}{2} & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} \frac{1}{2} & -1 \\ 0 & 1 \end{pmatrix} \neq \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & 1 \end{pmatrix} = T^{-1}.
$$

**Explanation of the Rule:** When $T = HS$ acts on a vector $x$, $Tx = H(Sx)$ applies $S$ **first** and $H$ **second** (at the end). To restore $x$, we must peel off the outer layer first: undo $H$ by applying $H^{-1}$ to get $H^{-1}(HSx) = Sx$, and only then undo $S$ by applying $S^{-1}$ to get $S^{-1}(Sx) = x$. Thus, operations are undone in reverse (last-in, first-out) order: $(HS)^{-1} = S^{-1}H^{-1}$.

### Final Results
- $T^{-1} = (HS)^{-1} = S^{-1}H^{-1} = \begin{pmatrix} \frac{1}{2} & -\frac{1}{2} \\ 0 & 1 \end{pmatrix}$
- Incorrect order: $H^{-1}S^{-1} = \begin{pmatrix} \frac{1}{2} & -1 \\ 0 & 1 \end{pmatrix} \neq T^{-1}$