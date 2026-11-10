
# Problem 14: Rotation Matrices

## Given

R(theta) = [[cos(theta), -sin(theta)],
            [sin(theta),  cos(theta)]]

## 1. Calculate R(alpha) * R(beta)

R(alpha) = [[cos(alpha), -sin(alpha)],
            [sin(alpha),  cos(alpha)]]

R(beta) = [[cos(beta), -sin(beta)],
           [sin(beta),  cos(beta)]]

Multiply the matrices:

R(alpha) * R(beta) =

[[cos(alpha)cos(beta) - sin(alpha)sin(beta),
  -cos(alpha)sin(beta) - sin(alpha)cos(beta)],

 [sin(alpha)cos(beta) + cos(alpha)sin(beta),
  -sin(alpha)sin(beta) + cos(alpha)cos(beta)]]

## 2. Apply Trigonometric Identities

Using the angle-sum formulas:

cos(alpha + beta) = cos(alpha)cos(beta) - sin(alpha)sin(beta)

sin(alpha + beta) = sin(alpha)cos(beta) + cos(alpha)sin(beta)

Therefore:

R(alpha) * R(beta) =

[[cos(alpha + beta), -sin(alpha + beta)],
 [sin(alpha + beta),  cos(alpha + beta)]]

## 3. Final Result

R(alpha) * R(beta) = R(alpha + beta)

## 4. Geometric Explanation

A rotation matrix rotates a vector around the origin.

Applying a rotation by beta degrees and then a rotation by alpha degrees is equivalent to one rotation by alpha + beta degrees.

Therefore, combining two rotations adds their angles.

This confirms that matrix multiplication represents the composition of rotations.
