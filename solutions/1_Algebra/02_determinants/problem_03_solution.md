
# Problem 3: Swapping Two Rows
## Question
### Given

A = [[1, 2, 0], [0, 3, 1], [2, 1, 1]]
## Solution
### 1. Calculate det(A)

Using cofactor expansion along the first row:

det(A) = 1(3 * 1 - 1 * 1) - 2(0 * 1 - 1 * 2) + 0

det(A) = 1(2) - 2(-2)

det(A) = 2 + 4

det(A) = 6

### 2. Swap the First and Second Rows

After swapping the first and second rows:

B = [[0, 3, 1], [1, 2, 0], [2, 1, 1]]

Swapping two rows changes the sign of the determinant.

Therefore:

det(B) = -det(A)

det(B) = -6

### 3. Verify by Calculation

det(B) = 0(2 * 1 - 0 * 1) - 3(1 * 1 - 0 * 2) + 1(1 * 1 - 2 * 2)

det(B) = 0 - 3 + (1 - 4)

det(B) = -3 - 3

det(B) = -6

### Final Results

det(A) = 6

det(B) = -6

Swapping two rows changes the sign of the determinant but does not change its absolute value.
