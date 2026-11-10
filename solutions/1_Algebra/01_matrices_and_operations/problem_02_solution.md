
# Problem 02: Matrix Addition and Scalar Multiplication

## Given

A = [[1, 2],
     [-1, 3]]

B = [[4, -2],
     [0, 5]]

## 1. Matrix Addition (A + B)

A + B = [[1+4, 2+(-2)],
         [-1+0, 3+5]]

A + B = [[5, 0],
         [-1, 8]]

## 2. Matrix Subtraction (A - B)

A - B = [[1-4, 2-(-2)],
         [-1-0, 3-5]]

A - B = [[-3, 4],
         [-1, -2]]

## 3. Scalar Multiplication (3A - 2B)

First, calculate 3A:

3A = [[3, 6],
      [-3, 9]]

Then, calculate 2B:

2B = [[8, -4],
      [0, 10]]

Now subtract:

3A - 2B = [[3-8, 6-(-4)],
           [-3-0, 9-10]]

3A - 2B = [[-5, 10],
           [-3, -1]]

## 4. Explanation

Matrix addition is possible only when both matrices have the same dimensions.

This is because matrix addition is performed by adding corresponding entries in the same positions.

Both matrices A and B have dimensions 2 x 2, so addition and subtraction are possible.

## Final Results

A + B = [[5, 0], [-1, 8]]

A - B = [[-3, 4], [-1, -2]]

3A - 2B = [[-5, 10], [-3, -1]]
