# Problem 14: A Matrix That Is Its Own Inverse

## Question
### Given
Assume that a square matrix $A$ satisfies

$$
A^2 = I.
$$

### Find
1. Show that $A^{-1} = A$.
2. Give a concrete example of a $2 \times 2$ matrix $A$ different from $I$ and $-I$ that satisfies $A^2 = I$, and verify it by matrix multiplication.

## Solution

### 1. Proof That $A^{-1} = A$
By definition, a square matrix $B$ is the inverse of $A$ if and only if $AB = I$ and $BA = I$. Given that $A^2 = I$, we can rewrite $A^2$ as the product $A \cdot A$:
$$
A \cdot A = A^2 = I.
$$
Setting $B = A$, both conditions $AB = AA = I$ and $BA = AA = I$ are immediately satisfied. Because the inverse of a square matrix is unique, it follows that:
$$
A^{-1} = A.
$$
*(Such matrices are called **involutory matrices**.)*

---

### 2. Example of a $2 \times 2$ Matrix ($A \neq \pm I$) and Verification
Choose the reflection matrix across the line $y = x$:
$$
A = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}.
$$
Clearly, $A \neq \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I$ and $A \neq \begin{pmatrix} -1 & 0 \\ 0 & -1 \end{pmatrix} = -I$.

**Verification by Multiplication:**
$$
A^2 = AA = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 0(0) + 1(1) & 0(1) + 1(0) \\ 1(0) + 0(1) & 1(1) + 0(0) \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2.
$$
Since $A^2 = I_2$, we have verified that $A^{-1} = A = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$.

### Final Results
- Proof: $A^2 = I \implies A \cdot A = I \implies A^{-1} = A$.
- Example: $A = \begin{pmatrix} 0 & 1 \\ 1 & 0 \end{pmatrix}$ satisfies $A^2 = I$.