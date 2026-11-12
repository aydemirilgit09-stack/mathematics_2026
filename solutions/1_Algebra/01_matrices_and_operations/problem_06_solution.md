# Problem 06: Matrix Transpose

## Question
### Given
A = [[1, 2, 3],
     [4, 5, 6]]

B = [[1, 0],
     [2, 1],
     [-1, 3]]

## Solution
### 1. Transpose of Matrix A

The transpose is obtained by switching rows and columns.

A^T = [[1, 4],
       [2, 5],
       [3, 6]]

### 2. Transpose of Matrix B

B^T = [[1, 2, -1],
       [0, 1, 3]]

### 3. Matrix Multiplication (AB)

AB = [[1*1 + 2*2 + 3*(-1), 1*0 + 2*1 + 3*3],
      [4*1 + 5*2 + 6*(-1), 4*0 + 5*1 + 6*3]]

AB = [[2, 11],
      [8, 23]]

### 4. Verify the Transpose Property

(AB)^T = [[2, 8],
          [11, 23]]

Now calculate B^T A^T:

B^T A^T = [[2, 8],
           [11, 23]]

Therefore:

(AB)^T = B^T A^T

### 5. Explanation

The transpose of a matrix changes its rows into columns.

The transpose of a product reverses the order of the factors.

This example confirms the transpose property.

###Final Results

A^T = [[1, 4], [2, 5], [3, 6]]

B^T = [[1, 2, -1], [0, 1, 3]]

AB = [[2, 11], [8, 23]]

(AB)^T = B^T A^T
