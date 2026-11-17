# Problem 11: When Do Matrices Commute?

## Question
### Given
Given

$$
A=
\begin{pmatrix}
1 & 1 \\
0 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
a & b \\
c & d \\
\end{pmatrix}.
$$

### Find
1. Find the conditions on $a, b, c, d$ under which $AB = BA$.
2. Describe the general form of all such matrices $B$.

## Solution

### 1. Compute $AB$ and $BA$
First, compute $AB$:
$$
AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} a & b \\ c & d \end{pmatrix} = \begin{pmatrix} 1\cdot a + 1\cdot c & 1\cdot b + 1\cdot d \\ 0\cdot a + 1\cdot c & 0\cdot b + 1\cdot d \end{pmatrix} = \begin{pmatrix} a+c & b+d \\ c & d \end{pmatrix}
$$

Next, compute $BA$:
$$
BA = \begin{pmatrix} a & b \\ c & d \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} a\cdot 1 + b\cdot 0 & a\cdot 1 + b\cdot 1 \\ c\cdot 1 + d\cdot 0 & c\cdot 1 + d\cdot 1 \end{pmatrix} = \begin{pmatrix} a & a+b \\ c & c+d \end{pmatrix}
$$

---

### 2. Equate Corresponding Entries ($AB = BA$)
For $AB = BA$, all four corresponding entries must be equal:
$$
\begin{pmatrix} a+c & b+d \\ c & d \end{pmatrix} = \begin{pmatrix} a & a+b \\ c & c+d \end{pmatrix}
$$

This yields the system of equations:
1. Top-left: $a + c = a \implies c = 0$
2. Top-right: $b + d = a + b \implies d = a$
3. Bottom-left: $c = c$ (always satisfied)
4. Bottom-right: $d = c + d \implies c = 0$

Thus, the necessary and sufficient conditions on the parameters are:
$$
c = 0 \quad \text{and} \quad a = d, \quad \text{while } b \in \mathbb{R} \text{ is arbitrary.}
$$

---

### 3. General Form of All Commuting Matrices $B$
Substituting $c = 0$ and $d = a$ into $B$, every matrix $B$ that commutes with $A$ has the upper-triangular Toeplitz form:
$$
B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix} = aI + bN, \quad \text{where } a, b \in \mathbb{R}, \ I = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}, \ N = \begin{pmatrix} 0 & 1 \\ 0 & 0 \end{pmatrix}.
$$

### Verification
Let $B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}$ and multiply in both orders:
$$
AB = \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} a & b \\ 0 & a \end{pmatrix} = \begin{pmatrix} a & a+b \\ 0 & a \end{pmatrix}, \qquad BA = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} a & a+b \\ 0 & a \end{pmatrix}.
$$
Since $AB = BA$, the conditions are verified.

### Final Results
- Conditions: $c = 0$ and $a = d$ ($b$ arbitrary).
- General form: $B = \begin{pmatrix} a & b \\ 0 & a \end{pmatrix}$ for any $a, b \in \mathbb{R}$.