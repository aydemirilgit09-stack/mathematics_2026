
# Problem 04: Matrix Multiplication and Noncommutativity

## Question
Given the matrices A and B below, calculate AB and BA. Then compare the two results and explain whether matrix multiplication is commutative.
A = [[1, 2],
     [0, 1]]

B = [[2, 0],
     [3, 1]]

## Solution
### 1. Calculate AB

AB = [[1*2 + 2*3, 1*0 + 2*1],
      [0*2 + 1*3, 0*0 + 1*1]]

AB = [[8, 2],
      [3, 1]]

### 2. Calculate BA

BA = [[2*1 + 0*0, 2*2 + 0*1],
      [3*1 + 1*0, 3*2 + 1*1]]

BA = [[2, 4],
      [3, 7]]

###3. Compare AB and BA

AB = [[8, 2],
      [3, 1]]

BA = [[2, 4],
      [3, 7]]

Therefore:

AB != BA

### 4. Explanation

Matrix multiplication is not commutative.

This means that changing the order of multiplication can produce different results.

In this example, AB and BA are both defined, but their results are different.

### Final Results

AB = [[8, 2], [3, 1]]

BA = [[2, 4], [3, 7]]

AB != BA
