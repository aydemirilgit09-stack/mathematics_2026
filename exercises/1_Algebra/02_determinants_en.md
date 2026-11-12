# Determinants

## Goal of the Set

After completing this set, the student should be able to compute determinants of small matrices, understand their connection with invertibility, know how row operations affect the determinant, and recognize situations in which the determinant gives quick information about a matrix or a system of equations.

## Basic Exercises


### Exercise 1. Determinant of a 2×2 Matrix

## Question

Consider the following two matrices:

$$
A = \begin{pmatrix}
3 & -2 \\
5 & 4
\end{pmatrix},
\qquad
B = \begin{pmatrix}
1 & 7 \\
2 & 14
\end{pmatrix}
$$

Calculate the determinant of each matrix. Determine which matrix is invertible and justify your answer using the determinant criterion.

## Solution

For a 2×2 matrix, the determinant is calculated using:

$$
\det(M) = ad - bc
$$

**Step 1: Calculate the determinant of matrix A.**

$$
\det(A) = 3(4) - (-2)(5)
$$

$$
= 12 + 10 = 22
$$

Since the determinant is non-zero, matrix A is invertible.

**Step 2: Calculate the determinant of matrix B.**

$$
\det(B) = 1(14) - 7(2)
$$

$$
= 14 - 14 = 0
$$

Since the determinant is zero, matrix B is not invertible.

**Final Answer:**

Matrix A is invertible because its determinant is 22, while matrix B is not invertible because its determinant is 0.

















> **Why this exercise:** introduces the simplest determinant calculation and immediately connects it with invertibility.

### Exercise 2. Determinant of a 3×3 Matrix

## Question

Consider the following 3x3 matrix:

$$
A =
\begin{pmatrix}
1 & 2 & -1 \\
0 & 3 & 4 \\
2 & 1 & 5
\end{pmatrix}
$$

Calculate the determinant of matrix A using Sarrus' rule. Then verify your result using cofactor expansion along the first row.

## Solution

For a 3x3 matrix, Sarrus' rule is used to calculate the determinant.

**Step 1: Apply Sarrus' rule.**

$$
\det(A) =
(1 \cdot 3 \cdot 5)
+ (2 \cdot 4 \cdot 2)
+ (-1 \cdot 0 \cdot 1)
$$

$$
- [(-1 \cdot 3 \cdot 2)
+ (2 \cdot 0 \cdot 5)
+ (1 \cdot 4 \cdot 1)]
$$

$$
= 15 + 16 + 0 - (-6 + 0 + 4)
$$

$$
= 31 - (-2) = 33
$$

**Step 2: Verify using cofactor expansion.**

Expanding along the first row:

$$
\det(A) =
1(3 \cdot 5 - 4 \cdot 1)
- 2(0 \cdot 5 - 4 \cdot 2)
+ (-1)(0 \cdot 1 - 3 \cdot 2)
$$

$$
= 11 + 16 + 6 = 33
$$

**Final Answer:**

The determinant of matrix A is 33. Both methods give the same result, confirming that the calculation is correct.












> **Why this exercise:** teaches a basic method for $3\times3$ matrices and builds the habit of checking the result without adding a second full solution.

### Exercise 3. Swapping Two Rows

## Question

Consider the following matrix:

$$
A =
\begin{pmatrix}
1 & 2 & 0 \\
0 & 3 & 1 \\
2 & 1 & 1
\end{pmatrix}
$$

Compute the determinant of A. Then form a matrix B by swapping the first and second rows of A.

First predict the determinant of B using the determinant row-swap property, and then verify your prediction by calculation.

## Solution

**Step 1: Calculate the determinant of matrix A.**

Expanding along the first row:

$$
\det(A) =
1(3 \cdot 1 - 1 \cdot 1)
- 2(0 \cdot 1 - 1 \cdot 2)
+ 0
$$

$$
= 1(2) - 2(-2)
$$

$$
= 2 + 4 = 6
$$

**Step 2: Form matrix B by swapping the first and second rows.**

$$
B =
\begin{pmatrix}
0 & 3 & 1 \\
1 & 2 & 0 \\
2 & 1 & 1
\end{pmatrix}
$$

**Step 3: Predict the determinant of B.**

When two rows of a matrix are swapped, the determinant changes its sign.

$$
\det(B) = -\det(A) = -6
$$

**Step 4: Verify by calculation.**

Expanding along the first row:

$$
\det(B) =
0 - 3(1 \cdot 1 - 0 \cdot 2)
+ 1(1 \cdot 1 - 2 \cdot 2)
$$

$$
= -3 + (1 - 4)
$$

$$
= -3 - 3 = -6
$$

**Final Answer:**

The determinant of A is 6, while the determinant of B is -6. This confirms that swapping two rows changes the sign of the determinant.

> **Why this exercise:** gives a second classical calculation with a $3\times3$ determinant while teaching the precise effect of a row swap on the sign of the determinant.

### Exercise 4. Triangular Matrix

## Question

Consider the following upper triangular matrix:

$$
A =
\begin{pmatrix}
2 & 4 & 1 \\
0 & -3 & 5 \\
0 & 0 & 7
\end{pmatrix}
$$

Calculate the determinant of A without expanding it. State the general rule for finding the determinant of a triangular matrix and explain why it applies here.

## Solution

The matrix A is an upper triangular matrix because all entries below the main diagonal are zero.

For any triangular matrix, the determinant is equal to the product of its diagonal entries.

**Step 1: Identify the diagonal entries.**

The diagonal entries are 2, -3 and 7.

**Step 2: Calculate the determinant.**

$$
\det(A) = 2 \cdot (-3) \cdot 7
$$

$$
= -6 \cdot 7
$$

$$
= -42
$$

**Final Answer:**

The determinant of matrix A is -42.

The determinant of a triangular matrix is always the product of its diagonal entries. This property allows us to calculate the determinant directly without expanding it.

> **Why this exercise:** reinforces an important property of triangular matrices.

### Exercise 5. Row Operations
## Question

Consider the following matrix:

$$
A =
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2
\end{pmatrix}
$$

Find the determinant of A by simplifying the matrix with row operations. At each step, indicate whether and how the determinant changes.

## Solution

**Step 1: Apply row operations.**

Start with the given matrix:

$$
A =
\begin{pmatrix}
1 & 2 & 3 \\
2 & 1 & 0 \\
-1 & 4 & 2
\end{pmatrix}
$$

Perform the following operations:

$$
R_2 \rightarrow R_2 - 2R_1
$$

$$
R_3 \rightarrow R_3 + R_1
$$

The resulting matrix is:

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 6 & 5
\end{pmatrix}
$$

**Step 2: Continue simplifying.**

$$
R_3 \rightarrow R_3 + 2R_2
$$

$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & -7
\end{pmatrix}
$$

**Step 3: Calculate the determinant.**

All operations used were adding a multiple of one row to another row. Therefore, the determinant does not change.

The matrix is now upper triangular, so its determinant is the product of its diagonal entries.

$$
\det(A) = 1 \cdot (-3) \cdot (-7)
$$

$$
\det(A) = 21
$$

**Final Answer:**

The determinant of matrix A is 21. Row operations that add a multiple of one row to another do not change the determinant.


> **Why this exercise:** connects determinants with row operations and requires conscious tracking of every step.

### Exercise 6. Parameter and Invertibility
## Question

Consider the following parameter-dependent matrix:

$$
A(t) =
\begin{pmatrix}
t & 1 \\
2 & t
\end{pmatrix}
$$

Find all values of t for which the matrix is not invertible. Explain how your answer is related to the determinant being zero.

## Solution

**Step 1: Calculate the determinant.**

For a 2x2 matrix, the determinant is calculated using:

$$
\det(A) = ad - bc
$$

For the given matrix:

$$
\det(A(t)) = t \cdot t - 1 \cdot 2
$$

$$
\det(A(t)) = t^2 - 2
$$

**Step 2: Find when the matrix is not invertible.**

A matrix is not invertible when its determinant is equal to zero.

Therefore:

$$
t^2 - 2 = 0
$$

$$
t^2 = 2
$$

$$
t = \pm \sqrt{2}
$$

**Final Answer:**

The matrix is not invertible for:

$$
t = \sqrt{2} \quad \text{or} \quad t = -\sqrt{2}
$$

For all other values of t, the matrix is invertible because its determinant is non-zero.
> **Why this exercise:** shows how the determinant can be used to study a family of matrices depending on a parameter.

### Exercise 7. Using Properties Instead of Recomputing
## Question

Suppose that for a 3x3 matrix A, det(A) = -4. Compute:

$$
\det(2A), \quad \det(A^T), \quad \det(A^2), \quad \det(-A)
$$

Justify each answer using the appropriate determinant property.

## Solution

**Step 1: Calculate det(2A).**

For a 3x3 matrix:

$$
\det(kA) = k^3 \det(A)
$$

Therefore:

$$
\det(2A) = 2^3 \cdot (-4)
$$

$$
= 8 \cdot (-4) = -32
$$

**Step 2: Calculate det(A^T).**

The determinant of a matrix is equal to the determinant of its transpose.

$$
\det(A^T) = \det(A) = -4
$$

**Step 3: Calculate det(A²).**

Using the product property:

$$
\det(A^2) = \det(A)\cdot\det(A)
$$

$$
= (-4)\cdot(-4) = 16
$$

**Step 4: Calculate det(-A).**

For a 3x3 matrix:

$$
\det(-A) = (-1)^3\det(A)
$$

$$
= -1\cdot(-4) = 4
$$

**Final Answer:**

$$
\det(2A) = -32
$$

$$
\det(A^T) = -4
$$

$$
\det(A^2) = 16
$$

$$
\det(-A) = 4
$$

All results follow directly from the determinant properties for scalar multiplication, transpose, and matrix products.
> **Why this exercise:** teaches how to use determinant properties instead of repeating a full calculation.

### Exercise 8. Determinant of a Product
Let $A,B$ be square matrices such that $\det A=3$ and $\det B=-5$. Compute $\det(AB)$, $\det(BA)$ and, if it exists, $\det(A^{-1}B)$. Explain why the first two results are equal even though usually $AB\neq BA$.


## Solution

We are given:

$$
\det(A)=3,\qquad \det(B)=-5
$$

**Step 1: Calculate det(AB).**

Using the determinant product property:

$$
\det(AB)=\det(A)\cdot\det(B)
$$

$$
=3\cdot(-5)=-15
$$

**Step 2: Calculate det(BA).**

$$
\det(BA)=\det(B)\cdot\det(A)
$$

$$
=(-5)\cdot3=-15
$$

**Step 3: Calculate det(A^{-1}B).**

Since det(A) is non-zero, A is invertible.

$$
\det(A^{-1})=\frac{1}{\det(A)}=\frac13
$$

Therefore:

$$
\det(A^{-1}B)=\det(A^{-1})\cdot\det(B)
$$

$$
=\frac13\cdot(-5)=-\frac53
$$

**Final Answer:**

$$
\det(AB)=-15
$$

$$
\det(BA)=-15
$$

$$
\det(A^{-1}B)=-\frac53
$$

The determinants of AB and BA are equal because multiplication of determinants is commutative, even though matrix multiplication itself is generally not commutative.

> **Why this exercise:** organizes how determinants behave with respect to products and inverses.

### Exercise 9. Area and the Determinant
## Question
The given vectors are:

\[
u=\begin{pmatrix}3\\1\end{pmatrix},
\qquad
v=\begin{pmatrix}1\\4\end{pmatrix}
\]

These two vectors span a parallelogram.

**Tasks:**
1. Compute the area of the parallelogram using the determinant.
2. Reverse the order of the vectors.
3. Explain how reversing the order changes the determinant and why the area remains unchanged.



## Solution

The area of a parallelogram is equal to the absolute value of the determinant formed by its two vectors.

**Step 1: Calculate the determinant.**

The given vectors are:

$$
u=\begin{pmatrix}3\\1\end{pmatrix},
\qquad
v=\begin{pmatrix}1\\4\end{pmatrix}
$$

$$
\det(u,v)=
\begin{vmatrix}
3 & 1\\
1 & 4
\end{vmatrix}
$$

$$
=3\cdot4-1\cdot1
$$

$$
=12-1=11
$$

**Step 2: Calculate the area.**

The area is the absolute value of the determinant.

$$
Area=|11|=11
$$

**Step 3: Reverse the order of the vectors.**

When the order of the vectors is reversed:

$$
\det(v,u)=
\begin{vmatrix}
1 & 3\\
4 & 1
\end{vmatrix}
$$

$$
=1\cdot1-3\cdot4
$$

$$
=1-12=-11
$$

**Step 4: Compare the areas.**

$$
Area=|-11|=11
$$

**Final Answer:**

The original determinant is 11, and the reversed determinant is -11. Reversing the order of the vectors changes the sign of the determinant, but the area remains 11 because area is always non-negative.

> **Why this exercise:** gives the determinant a geometric interpretation and distinguishes its sign from the value of the area.

### Exercise 10. Detecting Dependence
## Question

The given matrix is:

\[
A=
\begin{pmatrix}
1 & 2 & 3\\
2 & 4 & 6\\
0 & 1 & 5
\end{pmatrix}
\]

**Tasks:**
1. Identify a specific dependence between the rows.
2. Explain why the rows are linearly dependent.
3. Connect this dependence to the determinant being zero.
4. Explain why the matrix is not invertible.

## Solution

The second row is twice the first row.

\[
R_2 = 2R_1
\]

Therefore, the rows are linearly dependent.

A matrix with linearly dependent rows has a determinant equal to zero.

\[
\det(A)=0
\]

**Final Answer:**

The determinant is zero because the second row is twice the first row. Therefore, the matrix is singular and not invertible.

> **Why this exercise:** teaches how to recognize a zero determinant from the structure of a matrix.

## More Challenging Exercises

### Exercise 11. Shortening the Calculation with Row Operations
Compute

$$
\det
\begin{pmatrix}
1 & 2 & 3 \\
1 & 3 & 4 \\
1 & 4 & 6 \\
\end{pmatrix}
$$

by first performing row operations that create as many zeros as possible. State which operations do not change the determinant.

## Solution

**Step 1: Perform row operations.**

Start with the given matrix:

\[
A=
\begin{pmatrix}
1&2&3\\
1&3&4\\
1&4&6
\end{pmatrix}
\]

Subtract the first row from the second row:

\[
R_2 \leftarrow R_2-R_1
\]

Subtract the first row from the third row:

\[
R_3 \leftarrow R_3-R_1
\]

The matrix becomes:

\[
\begin{pmatrix}
1&2&3\\
0&1&1\\
0&2&3
\end{pmatrix}
\]

**Step 2: Create more zeros.**

\[
R_3 \leftarrow R_3-2R_2
\]

The matrix becomes:

\[
\begin{pmatrix}
1&2&3\\
0&1&1\\
0&0&1
\end{pmatrix}
\]

**Step 3: Calculate the determinant.**

The matrix is now upper triangular, so the determinant is the product of its diagonal entries.

\[
\det(A)=1\cdot1\cdot1=1
\]

**Final Answer:**

The determinant of matrix A is 1.

All row operations used were of the form of adding a multiple of one row to another row. These operations do not change the determinant.

> **Why this exercise:** develops planning instead of mechanically repeating the same procedure.

### Exercise 12. A Parameter Revealed by a Row Operation
For

$$
A(t)=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 4 & t \\
0 & 1 & 1 \\
\end{pmatrix}
$$

find the values of $t$ for which the matrix is not invertible.

Before computing the determinant, perform the operation

$$
R_2\leftarrow R_2-2R_1
$$

and use the resulting structure. At the end, explain what special thing happens to the rows for the value of the parameter you found.

## Solution

**Step 1: Perform the given row operation.**

\[
R_2 \leftarrow R_2-2R_1
\]

The matrix becomes:

\[
\begin{pmatrix}
1&2&3\\
0&0&t-6\\
0&1&1
\end{pmatrix}
\]

**Step 2: Find the determinant.**

Expanding along the first column:

\[
\det(A)=
1\begin{vmatrix}
0&t-6\\
1&1
\end{vmatrix}
\]

\[
\det(A)=0-(t-6)
\]

\[
\det(A)=6-t
\]

**Step 3: Find when the matrix is not invertible.**

A matrix is not invertible when its determinant is zero.

\[
6-t=0
\]

\[
t=6
\]

**Final Answer:**

The matrix is not invertible when t = 6.

When t = 6, the second row becomes a zero row. Therefore, the rows are linearly dependent and the determinant is zero.

> **Why this exercise:** combines a parameter, row operations, and recognition of dependence in one short argument.

### Exercise 13. Determinant by Elimination
Compute the determinant

$$
A=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 5 & 7 \\
1 & 0 & 2 \\
\end{pmatrix}
$$

using elimination. Record the effect of every row operation used on the value of the determinant.
## Solution

**Step 1: Perform row operations.**

Start with the given matrix:

\[
A=
\begin{pmatrix}
1&2&3\\
2&5&7\\
1&0&2
\end{pmatrix}
\]

Subtract twice the first row from the second row:

\[
R_2 \leftarrow R_2-2R_1
\]

Subtract the first row from the third row:

\[
R_3 \leftarrow R_3-R_1
\]

The matrix becomes:

\[
\begin{pmatrix}
1&2&3\\
0&1&1\\
0&-2&-1
\end{pmatrix}
\]

**Step 2: Create an upper triangular matrix.**

Add twice the second row to the third row:

\[
R_3 \leftarrow R_3+2R_2
\]

The matrix becomes:

\[
\begin{pmatrix}
1&2&3\\
0&1&1\\
0&0&1
\end{pmatrix}
\]

**Step 3: Calculate the determinant.**

All row operations used were adding a multiple of one row to another row. Therefore, the determinant does not change.

The matrix is now upper triangular, so its determinant is the product of its diagonal entries.

\[
\det(A)=1\cdot1\cdot1=1
\]

**Final Answer:**

The determinant of matrix A is 1.

All row operations used preserve the determinant because they involve adding a multiple of one row to another row.
> **Why this exercise:** reinforces organizing a determinant calculation through row operations without introducing an unnecessary second procedure.

### Exercise 14. A System of Equations and the Determinant
Consider the system $Ax=b$, where

$$
A=
\begin{pmatrix}
1 & 2 \\
k & 4 \\
\end{pmatrix}.
$$

For which values of $k$ does the system have exactly one solution for every $b$? For the remaining value, give an example of a right-hand side $b$ for which the system has infinitely many solutions, and an example for which it has no solution.
## Solution

**Step 1: Calculate the determinant.**

For the given matrix:

\[
A=
\begin{pmatrix}
1&2\\
k&4
\end{pmatrix}
\]

The determinant is:

\[
\det(A)=1\cdot4-2\cdot k
\]

\[
\det(A)=4-2k
\]

**Step 2: Find when the system has exactly one solution.**

A system has exactly one solution when the determinant is non-zero.

\[
4-2k\neq0
\]

\[
2k\neq4
\]

\[
k\neq2
\]

Therefore, the system has exactly one solution for every b when \(k\neq2\).

**Step 3: Consider the special case \(k=2\).**

When \(k=2\), the matrix becomes:

\[
A=
\begin{pmatrix}
1&2\\
2&4
\end{pmatrix}
\]

The second row is twice the first row.

**Example 1: Infinitely many solutions**

Choose:

\[
b=
\begin{pmatrix}
2\\
4
\end{pmatrix}
\]

Both equations represent the same line:

\[
x+2y=2
\]

Therefore, there are infinitely many solutions.

**Example 2: No solution**

Choose:

\[
b=
\begin{pmatrix}
2\\
5
\end{pmatrix}
\]

The equations become:

\[
x+2y=2
\]

\[
2x+4y=5
\]

The second equation is inconsistent with twice the first equation. Therefore, there is no solution.

**Final Answer:**

The system has exactly one solution for every b when \(k\neq2\).

When \(k=2\), the system can have infinitely many solutions or no solution, depending on the right-hand side b.
> **Why this exercise:** connects the determinant with uniqueness of solutions and requires distinguishing the exceptional cases.

### Exercise 15. Combining Determinant Properties
Let $A$ and $B$ be invertible $2\times2$ matrices with

$$
\det A=-2,\qquad \det B=3.
$$

Without finding the entries of the matrices, compute

$$
\det\left(B^{-1}A^TB\right).
$$

State the determinant properties you use in order and explain why the factors involving $B$ eventually cancel.
## Solution

**Step 1: Apply the determinant of a product property.**

We use the property:

\[
\det(XYZ)=\det(X)\cdot\det(Y)\cdot\det(Z)
\]

Therefore:

\[
\det(B^{-1}A^TB)
=
\det(B^{-1})\cdot\det(A^T)\cdot\det(B)
\]

**Step 2: Apply the inverse and transpose properties.**

We know that:

\[
\det(B^{-1})=\frac{1}{\det(B)}=\frac{1}{3}
\]

Also:

\[
\det(A^T)=\det(A)=-2
\]

**Step 3: Calculate the determinant.**

Substituting the known values:

\[
\det(B^{-1}A^TB)
=
\frac{1}{3}\cdot(-2)\cdot3
\]

\[
=-2
\]

**Final Answer:**

\[
\boxed{\det(B^{-1}A^TB)=-2}
\]

The determinant properties used are the product property, the inverse property, and the transpose property. The factors involving B cancel because:

\[
\frac{1}{\det(B)}\cdot\det(B)=1
\]

Therefore, the final result depends only on the determinant of A.
> **Why this exercise:** tests the transfer of several known properties into one short problem instead of checking a single property again with numbers.

### Exercise 16. Determinant of a 2x2 Matrix

**Question**

Compute the determinant:

\[
A=\begin{pmatrix}
4 & 3\\
2 & 5
\end{pmatrix}
\]

**Solution**

For a 2x2 matrix, the determinant is:

\[
\det(A)=ad-bc
\]

\[
\det(A)=(4)(5)-(3)(2)
\]

\[
=20-6=14
\]

**Final Answer:** The determinant is 14.

---

### Exercise 17. Determinant of a Triangular Matrix

**Question**

Compute the determinant:

\[
A=\begin{pmatrix}
2 & 1 & 4\\
0 & 3 & -2\\
0 & 0 & 5
\end{pmatrix}
\]

**Solution**

The matrix is upper triangular. Therefore, multiply the diagonal entries:

\[
\det(A)=2\cdot3\cdot5
\]

\[
\det(A)=30
\]

**Final Answer:** The determinant is 30.

---

### Exercise 18. Finding a Singular Matrix

**Question**

Find the value of k for which the matrix is not invertible:

\[
A=\begin{pmatrix}
1 & 2\\
3 & k
\end{pmatrix}
\]

**Solution**

A matrix is not invertible when its determinant is zero.

\[
\det(A)=1\cdot k-2\cdot3
\]

\[
k-6=0
\]

\[
k=6
\]

**Final Answer:** The matrix is not invertible when k = 6.

---

### Exercise 19. Effect of Row Swapping

**Question**

Calculate the determinant of the matrix and explain what happens when its rows are exchanged.

\[
A=\begin{pmatrix}
1 & 2\\
3 & 4
\end{pmatrix}
\]

**Solution**

First, calculate the original determinant:

\[
\det(A)=1\cdot4-2\cdot3
\]

\[
\det(A)=4-6=-2
\]

After exchanging the rows:

\[
B=\begin{pmatrix}
3 & 4\\
1 & 2
\end{pmatrix}
\]

\[
\det(B)=3\cdot2-4\cdot1
\]

\[
\det(B)=6-4=2
\]

**Final Answer:** Swapping two rows changes the sign of the determinant.

---

### Exercise 20. Determinant and Invertibility

**Question**

Calculate the determinant and determine whether the matrix is invertible.

\[
A=\begin{pmatrix}
1 & 2 & 0\\
0 & 3 & 1\\
2 & 1 & 4
\end{pmatrix}
\]

**Solution**

Expand the determinant along the first row:

\[
\det(A)=
1\begin{vmatrix}3&1\\1&4\end{vmatrix}
-2\begin{vmatrix}0&1\\2&4\end{vmatrix}
\]

\[
=1(12-1)-2(0-2)
\]

\[
=11+4=15
\]

Since the determinant is not zero, the matrix is invertible.

**Final Answer:** The determinant is 15, and the matrix is invertible.
