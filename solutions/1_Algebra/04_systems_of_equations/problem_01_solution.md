# Problem 1: From a System to a Matrix

## Question
### Given
The system

$$
\begin{cases}
2x-y+z=4, \\
x+3y-2z=1, \\
3x+y+z=7.
\end{cases}
$$

### Find
Write the system in the form $Ax=b$. Identify the coefficient matrix, the vector of unknowns, and the right-hand side vector. Explain how each row of the matrix corresponds to one equation.

## Solution

We are given the following system of linear equations:
$$
\begin{cases}
2x - y + z = 4, \\
x + 3y - 2z = 1, \\
3x + y + z = 7.
\end{cases}
$$

### 1. Coefficient Matrix ($A$), Vector of Unknowns ($\mathbf{x}$), and Right-Hand Side Vector ($b$)

* **Coefficient matrix ($A$):** Contains the coefficients of the unknowns $x, y, z$ from each equation:
$$
A = \begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix}
$$

* **Vector of unknowns ($\mathbf{x}$):** A column vector listing the variables in order:
$$
\mathbf{x} = \begin{pmatrix} x \\ y \\ z \end{pmatrix}
$$

* **Right-hand side vector ($b$):** A column vector containing the constant terms on the right side of the equations:
$$
b = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}
$$

### 2. Matrix Form ($A\mathbf{x} = b$)

Combining these components, the system is written in matrix form as:
$$
\begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}
$$

### 3. Row-by-Row Correspondence

Each row of the matrix multiplication $A\mathbf{x}$ computes the dot product of that row of $A$ with the column vector $\mathbf{x}$, which reconstructs the left-hand side of the corresponding equation, while the matching entry in $b$ gives the right-hand side:
* **Row 1:** $2(x) + (-1)(y) + 1(z) = 2x - y + z = 4$ (First equation)
* **Row 2:** $1(x) + 3(y) + (-2)(z) = x + 3y - 2z = 1$ (Second equation)
* **Row 3:** $3(x) + 1(y) + 1(z) = 3x + y + z = 7$ (Third equation)

### Final Result

$$
A = \begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix}, \quad \mathbf{x} = \begin{pmatrix} x \\ y \\ z \end{pmatrix}, \quad b = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}, \quad \text{so } \begin{pmatrix} 2 & -1 & 1 \\ 1 & 3 & -2 \\ 3 & 1 & 1 \end{pmatrix} \begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 4 \\ 1 \\ 7 \end{pmatrix}
$$