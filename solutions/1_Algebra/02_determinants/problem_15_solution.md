# Problem 15: Combining Determinant Properties

## Question
### Given
Let $A$ and $B$ be invertible $2 \times 2$ matrices with

$$
\det A = -2, \qquad \det B = 3.
$$

### Find
Without finding the entries of the matrices, compute:
$$
\det\left(B^{-1} A^T B\right).
$$
State the determinant properties used in order and explain why the factors involving $B$ eventually cancel.

## Solution

### Step-by-Step Computation Using Determinant Properties

1. **Product Property ($\det(XYZ) = \det(X)\det(Y)\det(Z)$):**
   Because the determinant of a product of square matrices equals the product of their determinants:
   $$
   \det\left(B^{-1} A^T B\right) = \det(B^{-1}) \cdot \det(A^T) \cdot \det(B).
   $$

2. **Inverse Property ($\det(B^{-1}) = \frac{1}{\det(B)}$) and Transpose Property ($\det(A^T) = \det(A)$):**
   Since $B$ is invertible ($\det(B) = 3 \neq 0$):
   $$
   \det(B^{-1}) = \frac{1}{\det(B)} = \frac{1}{3}, \qquad \det(A^T) = \det(A) = -2.
   $$

3. **Substitute and Simplify:**
   $$
   \det\left(B^{-1} A^T B\right) = \frac{1}{3} \cdot (-2) \cdot 3 = -2.
   $$

---

### Why the Factors Involving $B$ Cancel
Determinants map matrices to nonzero real scalars, and scalar multiplication is commutative and associative:
$$
\det(B^{-1})\det(A^T)\det(B) = \left(\frac{1}{\det(B)} \cdot \det(B)\right) \det(A^T) = 1 \cdot \det(A) = \det(A).
$$
More generally, $B^{-1} M B$ is a **similarity transformation** of $M = A^T$, and similar matrices always share the same determinant regardless of the invertible change-of-basis matrix $B$.

### Verification
Testing with diagonal matrices $A = \begin{pmatrix} -2 & 0 \\ 0 & 1 \end{pmatrix}$ ($\det A = -2$) and $B = \begin{pmatrix} 3 & 0 \\ 0 & 1 \end{pmatrix}$ ($\det B = 3$):
$$
B^{-1} A^T B = \begin{pmatrix} \frac{1}{3} & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 3 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} -2 & 0 \\ 0 & 1 \end{pmatrix} \implies \det(B^{-1} A^T B) = -2.
$$

### Final Result
- $\det\left(B^{-1} A^T B\right) = -2$