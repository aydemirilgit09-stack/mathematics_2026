
# Problem 03: When Can Matrices Be Multiplied?

## Question
### Given

A = 2 x 3
B = 3 x 4
C = 4 x 2
D = 2 x 2

    For the products AB, BA, BC, CB, AC, CA, AD, and DA:

Determine whether each matrix multiplication is defined. If it is defined, state the dimensions of the resulting matrix. Justify each answer using the matrix multiplication compatibility rule.

## Solution

Two matrices can be multiplied if the number of columns in the first matrix equals the number of rows in the second matrix.

The resulting matrix has the number of rows of the first matrix and the number of columns of the second matrix.

###  Checking Each Product

#### AB

A (2 x 3) * B (3 x 4)

Defined because 3 = 3.

Result dimension: 2 x 4.

### BA

B (3 x 4) * A (2 x 3)

Not defined because 4 != 2.

### BC

B (3 x 4) * C (4 x 2)

Defined because 4 = 4.

Result dimension: 3 x 2.

### CB

C (4 x 2) * B (3 x 4)

Not defined because 2 != 3.

### AC

A (2 x 3) * C (4 x 2)

Not defined because 3 != 4.

### CA

C (4 x 2) * A (2 x 3)

Defined because 2 = 2.

Result dimension: 4 x 3.

### AD

A (2 x 3) * D (2 x 2)

Not defined because 3 != 2.

### DA

D (2 x 2) * A (2 x 3)

Defined because 2 = 2.

Result dimension: 2 x 3.

### 3. Final Results

| Product | Defined? | Result Dimension |
|---------|----------|------------------|
| AB | Yes | 2 x 4 |
| BA | No | - |
| BC | Yes | 3 x 2 |
| CB | No | - |
| AC | No | - |
| CA | Yes | 4 x 3 |
| AD | No | - |
| DA | Yes | 2 x 3 |

### Explanation

Matrix multiplication depends on the compatibility of the inner dimensions.

If the inner dimensions are equal, multiplication is possible. Otherwise, it is not defined.
