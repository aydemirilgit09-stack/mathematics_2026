
# Problem 10: Columns of a Matrix Product

## Given

A = [[1, 2, 0],
     [0, 1, 1]]

B = [[1, 2],
     [-1, 0],
     [3, 1]]

The columns of B are:

b1 = [1, -1, 3]

b2 = [2, 0, 1]

## 1. Calculate Ab1

Ab1 = [[1, 2, 0],
       [0, 1, 1]] * [1, -1, 3]

Ab1 = [1*1 + 2*(-1) + 0*3,
       0*1 + 1*(-1) + 1*3]

Ab1 = [-1, 2]

## 2. Calculate Ab2

Ab2 = [[1, 2, 0],
       [0, 1, 1]] * [2, 0, 1]

Ab2 = [1*2 + 2*0 + 0*1,
       0*2 + 1*0 + 1*1]

Ab2 = [2, 1]

## 3. Calculate AB

AB = [[1, 2, 0],
      [0, 1, 1]] * [[1, 2],
                     [-1, 0],
                     [3, 1]]

AB = [[-1, 2],
      [2, 1]]

## 4. Compare the Results

Ab1 = [-1, 2]

Ab2 = [2, 1]

The columns of AB are exactly Ab1 and Ab2.

## 5. Explanation

When a matrix is multiplied by another matrix, each column of the second matrix is multiplied by the first matrix.

Therefore, the columns of AB are obtained by calculating Ab1 and Ab2 separately.

## Final Results

Ab1 = [-1, 2]

Ab2 = [2, 1]

AB = [[-1, 2],
      [2, 1]]
