
# Problem 05: Matrix Times Vector

## Given

A = [[2, -1],
     [1, 3]]

x = [[4],
     [2]]

## 1. Calculate Ax

Ax = [[2*4 + (-1)*2],
      [1*4 + 3*2]]

Ax = [[8 - 2],
      [4 + 6]]

Therefore:

Ax = [[6],
      [10]]

## 2. Linear Combination of Columns

The columns of matrix A are:

First column: [2, 1]^T

Second column: [-1, 3]^T

The vector x contains the coefficients 4 and 2.

Therefore:

Ax = 4*[2, 1]^T + 2*[-1, 3]^T

Ax = [8, 4]^T + [-2, 6]^T

Ax = [6, 10]^T

## 3. Explanation

Multiplying a matrix by a vector produces a linear combination of the columns of the matrix.

The coefficients of this linear combination are the entries of the vector x.

## Final Result

Ax = [6, 10]^T
