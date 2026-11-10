
# Problem 2: Determinant of a 3x3 Matrix

## Given

A = [[1, 2, -1], [0, 3, 4], [2, 1, 5]]

## 1. Calculate the Determinant Using Sarrus' Rule

det(A) = (1 * 3 * 5) + (2 * 4 * 2) + (-1 * 0 * 1)

det(A) = 15 + 16 + 0

det(A) = 31

Subtract the negative diagonals:

det(A) = 31 - [(-1 * 3 * 2) + (2 * 0 * 5) + (1 * 4 * 1)]

det(A) = 31 - (-6 + 0 + 4)

det(A) = 31 - (-2)

det(A) = 33

## 2. Verify Using a Determinant Property

Apply the row operation:

R3 = R3 - 2R1

The determinant does not change.

The new matrix is:

A = [[1, 2, -1], [0, 3, 4], [0, -3, 7]]

Expanding along the first column:

det(A) = 1 * [(3 * 7) - (4 * -3)]

det(A) = 21 + 12

det(A) = 33

## Final Result

det(A) = 33

Both methods give the same result. Therefore, the calculation is verified.
