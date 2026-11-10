
# Problem 13: A Recurrence Written in Matrix Form

## Given

F = [[1, 1],
     [1, 0]]

## 1. Calculate F^2

F^2 = F * F

F^2 = [[2, 1],
       [1, 1]]

## 2. Calculate F^3

F^3 = F^2 * F

F^3 = [[3, 2],
       [2, 1]]

## 3. Calculate F^4

F^4 = F^3 * F

F^4 = [[5, 3],
       [3, 2]]

## 4. Calculate F^5

F^5 = F^4 * F

F^5 = [[8, 5],
       [5, 3]]

## 5. Compare with the Fibonacci Sequence

The Fibonacci sequence is:

0, 1, 1, 2, 3, 5, 8, ...

The matrix powers contain consecutive Fibonacci numbers.

F^2 = [[2, 1], [1, 1]]
F^3 = [[3, 2], [2, 1]]
F^4 = [[5, 3], [3, 2]]
F^5 = [[8, 5], [5, 3]]

Each new Fibonacci number is the sum of the previous two numbers.

## 6. Calculate F * Vector

Let the vector be:

x = [[a],
     [b]]

Then:

F * x = [[1, 1], [1, 0]] * [[a], [b]]

F * x = [[a + b],
         [a]]

## 7. Explanation

Matrix multiplication creates the sum of two consecutive terms and keeps the previous term for the next step.

This is exactly the Fibonacci recurrence relation.

## Final Result

F^2 = [[2, 1], [1, 1]]

F^3 = [[3, 2], [2, 1]]

F^4 = [[5, 3], [3, 2]]

F^5 = [[8, 5], [5, 3]]

F * [[a], [b]] = [[a + b], [a]]
