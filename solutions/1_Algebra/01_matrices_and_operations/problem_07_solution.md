# Problem 07: Identity Matrix, Zero Matrix, and Powers
## Question
### Given

A = [[2, 1],
     [0, 2]]

## Solution
### 1. Identity Matrix

I = [[1, 0],
     [0, 1]]

AI = [[2, 1],
      [0, 2]]

IA = [[2, 1],
      [0, 2]]

### 2. Zero Matrix

0 = [[0, 0],
     [0, 0]]

A + 0 = [[2, 1],
         [0, 2]]

### 3. Calculate A^2

A^2 = A * A

A^2 = [[2*2 + 1*0, 2*1 + 1*2],
       [0*2 + 2*0, 0*1 + 2*2]]

A^2 = [[4, 4],
       [0, 4]]

### 4. Calculate A^3

A^3 = A^2 * A

A^3 = [[4*2 + 4*0, 4*1 + 4*2],
       [0*2 + 4*0, 0*1 + 4*2]]

A^3 = [[8, 12],
       [0, 8]]

### 5. Explanation

The identity matrix does not change a matrix when multiplied by it.

The zero matrix does not change a matrix when added to it.

Successive powers of A are calculated by multiplying A by itself.

### Final Results

AI = [[2, 1], [0, 2]]

IA = [[2, 1], [0, 2]]

A + 0 = [[2, 1], [0, 2]]

A^2 = [[4, 4], [0, 4]]

A^3 = [[8, 12], [0, 8]]
