
# Problem 11: When Do Matrices Commute?

## Given

A = [[1, 1],
     [0, 1]]

B = [[a, b],
     [c, d]]

## 1. Calculate AB

AB = [[1, 1],
      [0, 1]] * [[a, b],
                  [c, d]]

AB = [[a + c, b + d],
      [c, d]]

## 2. Calculate BA

BA = [[a, b],
      [c, d]] * [[1, 1],
                  [0, 1]]

BA = [[a, a + b],
      [c, c + d]]

## 3. Set AB Equal to BA

For AB = BA, corresponding entries must be equal.

a + c = a

Therefore, c = 0.

b + d = a + b

Therefore, d = a.

The remaining equations give the same condition c = 0.

## 4. General Form of Matrix B

Since c = 0 and d = a:

B = [[a, b],
     [0, a]]

## 5. Final Result

AB = BA if and only if:

c = 0

d = a

The general form of B is:

B = [[a, b],
     [0, a]]

where a and b can be any real numbers.

## Explanation

Two matrices commute when their multiplication gives the same result in both orders.

Therefore, matrix B must have the form shown above to commute with matrix A.
