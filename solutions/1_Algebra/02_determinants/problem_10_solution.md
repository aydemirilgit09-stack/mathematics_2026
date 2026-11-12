
# Problem 10: Detecting Dependence
## Question
### Given

A = [[1, 2, 3], [2, 4, 6], [0, 1, 5]]
## Solution
### 1. Identify the Row Dependence

The second row is twice the first row.

R2 = 2 * R1

Therefore, the rows are linearly dependent.

### 2. Determine the Determinant

A matrix with linearly dependent rows has a determinant equal to zero.

det(A) = 0

### 3. Explain Invertibility

A square matrix is invertible if and only if its determinant is not zero.

Since det(A) = 0, the matrix is not invertible.

### Final Result

R2 = 2 * R1

The rows are linearly dependent.

det(A) = 0

The matrix is singular and not invertible.
