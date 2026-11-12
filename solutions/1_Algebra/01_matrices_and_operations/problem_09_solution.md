
# Problem 09: Composing Transformations
## Question
### Given

S = [[2, 0],
     [0, 1]]

R = [[0, -1],
     [1, 0]]

x = [1, 2]
## Solution
### 1. Calculate Sx

Sx = [[2, 0],
      [0, 1]] * [1, 2]

Sx = [2*1 + 0*2, 0*1 + 1*2]

Sx = [2, 2]

### 2. Calculate RSx

RSx = [[0, -1],
       [1, 0]] * [2, 2]

RSx = [0*2 + (-1)*2, 1*2 + 0*2]

RSx = [-2, 2]

### 3. Calculate Rx

Rx = [[0, -1],
      [1, 0]] * [1, 2]

Rx = [-2, 1]

### 4. Calculate SRx

SRx = [[2, 0],
       [0, 1]] * [-2, 1]

SRx = [-4, 1]

### 5. Compare the Results

RSx = [-2, 2]

SRx = [-4, 1]

Therefore:

RSx != SRx

### 6. Geometric Explanation

Matrix S stretches the x-coordinate by a factor of 2.

Matrix R rotates the vector 90 degrees counterclockwise.

The order of transformations matters because stretching and rotation produce different results when applied in different orders.

### Final Results

RSx = [-2, 2]

SRx = [-4, 1]

The two results are different because matrix multiplication is not commutative.
