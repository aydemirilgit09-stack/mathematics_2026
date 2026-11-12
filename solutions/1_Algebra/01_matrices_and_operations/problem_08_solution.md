# Problem 08: Row Operations and Their Reversibility
## Question
### Given

A = [[1, 2, -1],
     [2, 4, 1],
     [-1, 1, 3]]
## Solution
### 1. First Operation

R2 <- R2 - 2R1

The new matrix is:

[[1, 2, -1],
 [0, 0, 3],
 [-1, 1, 3]]

Reverse operation:

R2 <- R2 + 2R1

### 2. Second Operation

R3 <- R3 + R1

The new matrix is:

[[1, 2, -1],
 [0, 0, 3],
 [0, 3, 2]]

Reverse operation:

R3 <- R3 - R1

### 3. Third Operation

Interchange R2 and R3.

The new matrix is:

[[1, 2, -1],
 [0, 3, 2],
 [0, 0, 3]]

Reverse operation:

Interchange R2 and R3 again.

### 4. Final Results

Final matrix:

[[1, 2, -1],
 [0, 3, 2],
 [0, 0, 3]]

All three row operations are reversible.

### Explanation

Each row operation has an inverse operation that restores the previous matrix.

These operations are useful in solving systems of linear equations and performing Gaussian elimination.
