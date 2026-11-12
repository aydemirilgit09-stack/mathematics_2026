
# Problem 15: Associativity of Multiplication and Different Calculation Paths

## Given

A = [[1, 2, 0],
     [0, 1, 1]]

B = [[1, 0],
     [2, 1],
     [-1, 3]]

C = [[2, 1],
     [0, -1]]

## 1. Calculate AB

AB = [[1, 2, 0], [0, 1, 1]] * [[1, 0], [2, 1], [-1, 3]]

AB = [[5, 2],
      [1, 4]]

## 2. Calculate (AB)C

(AB)C = [[5, 2], [1, 4]] * [[2, 1], [0, -1]]

(AB)C = [[10, 3],
         [2, -3]]

## 3. Calculate BC

BC = [[1, 0], [2, 1], [-1, 3]] * [[2, 1], [0, -1]]

BC = [[2, 1],
      [4, 1],
      [-2, -4]]

## 4. Calculate A(BC)

A(BC) = [[1, 2, 0], [0, 1, 1]] * [[2, 1], [4, 1], [-2, -4]]

A(BC) = [[10, 3],
         [2, -3]]

## 5. Compare the Results

(AB)C = [[10, 3],
         [2, -3]]

A(BC) = [[10, 3],
         [2, -3]]

Therefore:

(AB)C = A(BC)

## 6. Compare the Number of Operations

Both calculation paths require two matrix multiplications.

For (AB)C:
- First multiplication: 12 scalar multiplications and 8 additions.
- Second multiplication: 8 scalar multiplications and 4 additions.
- Total: 20 multiplications and 12 additions.

For A(BC):
- First multiplication: 12 scalar multiplications and 6 additions.
- Second multiplication: 12 scalar multiplications and 8 additions.
- Total: 24 multiplications and 14 additions.

Therefore, calculating (AB)C requires fewer scalar operations in this example.

## 7. Explanation

Matrix multiplication is associative.

This means that changing the grouping of matrices does not change the final result.

However, different calculation paths may require different numbers of operations.

In this example, calculating (AB)C is more efficient than calculating A(BC).

## Final Result

(AB)C = A(BC) = [[10, 3], [2, -3]]

Matrix multiplication is associative, but the computational cost can depend on the order of grouping.
