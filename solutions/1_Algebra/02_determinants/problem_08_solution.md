# Problem 08: Determinant of a Product

## Question
### Given
Let $A, B$ be square matrices of the same size such that $\det A = 3$ and $\det B = -5$.

### Find
1. Compute $\det(AB)$, $\det(BA)$, and (if it exists) $\det(A^{-1}B)$.
2. Explain why $\det(AB)$ and $\det(BA)$ are equal even though usually $AB \neq BA$.

## Solution

### 1. Compute $\det(AB)$ and $\det(BA)$
By the multiplicative property of determinants, for any two $n \times n$ matrices $A$ and $B$:
$$
\det(AB) = \det(A)\det(B) = 3 \cdot (-5) = -15.
$$
Similarly:
$$
\det(BA) = \det(B)\det(A) = (-5) \cdot 3 = -15.
$$

---

### 2. Existence and Computation of $\det(A^{-1}B)$
Since $\det(A) = 3 \neq 0$, the matrix $A$ is invertible, so $A^{-1}$ exists and its determinant is:
$$
\det(A^{-1}) = \frac{1}{\det(A)} = \frac{1}{3}.
$$
Applying the product property to $A^{-1}B$:
$$
\det(A^{-1}B) = \det(A^{-1})\det(B) = \frac{1}{3} \cdot (-5) = -\frac{5}{3}.
$$

---

### 3. Why $\det(AB) = \det(BA)$ Despite $AB \neq BA$
While matrix multiplication is noncommutative ($AB$ and $BA$ are generally different matrices), the determinant maps each square matrix to a **real (or complex) scalar**. Multiplication of real numbers is commutative, so:
$$
\det(AB) = \det(A)\det(B) = \det(B)\det(A) = \det(BA).
$$

### Verification
Using the $1 \times 1$ matrices $A = (3)$ and $B = (-5)$:
* $\det(AB) = \det((-15)) = -15$, and $\det(BA) = \det((-15)) = -15$.
* $\det(A^{-1}B) = \det\left(\left(\frac{1}{3}\right)(-5)\right) = -\frac{5}{3}$.

### Final Results
- $\det(AB) = -15$
- $\det(BA) = -15$
- $\det(A^{-1}B) = -\frac{5}{3}$