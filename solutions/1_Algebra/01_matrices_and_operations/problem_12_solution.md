# Problem 12: Formula for a Matrix Power

## Question
### Given
Let

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix}.
$$

### Find
1. Compute $A^2$, $A^3$, and $A^4$, and use them to formulate a conjecture for $A^n$.
2. Assume the formula is true for $n$, multiply by $A$, and explain why you obtain the exact formula for $n+1$ (proof by mathematical induction).

## Solution

### 1. Compute $A^2$, $A^3$, and $A^4$
* **Compute $A^2$:**
  $$
  A^2 = AA = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1)+1(0) & 1(1)+1(1) \\ 0(1)+1(0) & 0(1)+1(1) \end{pmatrix} = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}
  $$
* **Compute $A^3$:**
  $$
  A^3 = A^2 A = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1)+2(0) & 1(1)+2(1) \\ 0(1)+1(0) & 0(1)+1(1) \end{pmatrix} = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}
  $$
* **Compute $A^4$:**
  $$
  A^4 = A^3 A = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1)+3(0) & 1(1)+3(1) \\ 0(1)+1(0) & 0(1)+1(1) \end{pmatrix} = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}
  $$

---

### 2. Conjecture for $A^n$
In each successive power, the diagonal entries remain $1$, the bottom-left entry remains $0$, and the top-right entry equals the exponent $n$. Therefore, for every positive integer $n \ge 1$:
$$
A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}.
$$

---

### 3. Inductive Step (From $n$ to $n+1$)
**Base Case ($n=1$):** $A^1 = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix}$, which matches the formula.

**Inductive Hypothesis:** Assume that for some integer $n \ge 1$,
$$
A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}.
$$

**Inductive Step:** Multiply $A^n$ by $A$ to compute $A^{n+1}$:
$$
A^{n+1} = A^n A = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 1(1) + n(0) & 1(1) + n(1) \\ 0(1) + 1(0) & 0(1) + 1(1) \end{pmatrix} = \begin{pmatrix} 1 & n+1 \\ 0 & 1 \end{pmatrix}.
$$

**Explanation:** When multiplying the first row $\begin{pmatrix} 1 & n \end{pmatrix}$ of $A^n$ by the second column $\begin{pmatrix} 1 \\ 1 \end{pmatrix}$ of $A$, we add $1 \cdot 1 + n \cdot 1 = n + 1$, incrementing the top-right entry by $1$ at every step while keeping all other entries invariant. By mathematical induction, the formula holds for all $n \ge 1$.

### Final Results
- $A^2 = \begin{pmatrix} 1 & 2 \\ 0 & 1 \end{pmatrix}$, $A^3 = \begin{pmatrix} 1 & 3 \\ 0 & 1 \end{pmatrix}$, $A^4 = \begin{pmatrix} 1 & 4 \\ 0 & 1 \end{pmatrix}$
- General formula: $A^n = \begin{pmatrix} 1 & n \\ 0 & 1 \end{pmatrix}$