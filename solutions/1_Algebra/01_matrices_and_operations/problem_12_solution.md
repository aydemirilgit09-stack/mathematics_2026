
# Problem 12: Formula for a Matrix Power
## Question
### Given

A = [[1, 1],
     [0, 1]]
## Solution
### 1. Calculate A^2

A^2 = A * A

A^2 = [[1, 1], [0, 1]] * [[1, 1], [0, 1]]

A^2 = [[1, 2],
       [0, 1]]

### 2. Calculate A^3

A^3 = A^2 * A

A^3 = [[1, 2], [0, 1]] * [[1, 1], [0, 1]]

A^3 = [[1, 3],
       [0, 1]]

### 3. Calculate A^4

A^4 = A^3 * A

A^4 = [[1, 3], [0, 1]] * [[1, 1], [0, 1]]

A^4 = [[1, 4],
       [0, 1]]

### 4. General Formula

By observing the pattern:

A^2 = [[1, 2], [0, 1]]
A^3 = [[1, 3], [0, 1]]
A^4 = [[1, 4], [0, 1]]

We obtain the general formula:

A^n = [[1, n],
       [0, 1]]

### 5. Verify the Formula for n + 1

Assume the formula is true for n:

A^n = [[1, n], [0, 1]]

Multiply by A:

A^(n+1) = A^n * A

A^(n+1) = [[1, n], [0, 1]] * [[1, 1], [0, 1]]

A^(n+1) = [[1, n+1],
           [0, 1]]

Therefore, the formula is also true for n + 1.

### Final Result

A^n = [[1, n],
       [0, 1]]

The pattern is confirmed for all positive integers n.
