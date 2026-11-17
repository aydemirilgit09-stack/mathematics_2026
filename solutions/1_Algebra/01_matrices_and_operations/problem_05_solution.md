## Question

Let

$$
A=
\begin{pmatrix}
2 & -1 \\
1 & 3 \\
\end{pmatrix},\qquad x=
\begin{pmatrix}
4 \\
2 \\
\end{pmatrix}.
$$

Compute $Ax$. Then express $Ax$ as a linear combination of the columns of $A$, with coefficients coming from the vector $x$.

## Solution

### Method
A matrix $A$ of size $2 \times 2$ multiplied by a column vector $x$ of size $2 \times 1$ produces a $2 \times 1$ vector. This can be computed either using the row-by-column dot product definition or by taking a linear combination of the columns of $A$ weighted by the entries of $x$.

---

### Step 1: Compute $Ax$ via Row-by-Column Multiplication
$$
Ax = \begin{pmatrix} 2 & -1 \\ 1 & 3 \end{pmatrix} \begin{pmatrix} 4 \\ 2 \end{pmatrix} = \begin{pmatrix} 2(4) + (-1)(2) \\ 1(4) + 3(2) \end{pmatrix} = \begin{pmatrix} 8 - 2 \\ 4 + 6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}
$$

---

### Step 2: Express $Ax$ as a Linear Combination of the Columns of $A$
Let the columns of $A$ be $a_1 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$ and $a_2 = \begin{pmatrix} -1 \\ 3 \end{pmatrix}$, and the components of $x$ be $x_1 = 4$ and $x_2 = 2$. Then:
$$
Ax = x_1 a_1 + x_2 a_2 = 4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix}
$$

### Verification
Evaluating the linear combination directly confirms the result from Step 1:
$$
4 \begin{pmatrix} 2 \\ 1 \end{pmatrix} + 2 \begin{pmatrix} -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 8 \\ 4 \end{pmatrix} + \begin{pmatrix} -2 \\ 6 \end{pmatrix} = \begin{pmatrix} 6 \\ 10 \end{pmatrix}.
$$