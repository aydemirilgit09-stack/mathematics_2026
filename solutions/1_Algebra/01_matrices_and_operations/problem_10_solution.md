# Problem 10: Columns of a Matrix Product

## Question
### Given
Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\qquad B=
\begin{pmatrix}
1 & 2 \\
-1 & 0 \\
3 & 1 \\
\end{pmatrix}.
$$

Denote the columns of $B$ by $b_1, b_2$.

### Find
1. Compute $Ab_1$ and $Ab_2$.
2. Compute the matrix $AB$.
3. Compare the results and explain why the columns of $AB$ are exactly the vectors $Ab_1$ and $Ab_2$.

## Solution

### 1. Compute $Ab_1$ and $Ab_2$
From matrix $B$, the two column vectors are:
$$
b_1 = \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix}, \qquad b_2 = \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix}.
$$

Multiply $A$ by each column vector:
$$
Ab_1 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ -1 \\ 3 \end{pmatrix} = \begin{pmatrix} 1(1) + 2(-1) + 0(3) \\ 0(1) + 1(-1) + 1(3) \end{pmatrix} = \begin{pmatrix} 1 - 2 + 0 \\ 0 - 1 + 3 \end{pmatrix} = \begin{pmatrix} -1 \\ 2 \end{pmatrix}
$$

$$
Ab_2 = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 \\ 0 \\ 1 \end{pmatrix} = \begin{pmatrix} 1(2) + 2(0) + 0(1) \\ 0(2) + 1(0) + 1(1) \end{pmatrix} = \begin{pmatrix} 2 + 0 + 0 \\ 0 + 0 + 1 \end{pmatrix} = \begin{pmatrix} 2 \\ 1 \end{pmatrix}
$$

---

### 2. Compute the Matrix Product $AB$
Since $A$ is $2 \times 3$ and $B$ is $3 \times 2$, $AB$ is a $2 \times 2$ matrix:
$$
AB = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 2 \\ -1 & 0 \\ 3 & 1 \end{pmatrix} = \begin{pmatrix} 1(1)+2(-1)+0(3) & 1(2)+2(0)+0(1) \\ 0(1)+1(-1)+1(3) & 0(2)+1(0)+1(1) \end{pmatrix} = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}
$$

---

### 3. Comparison and Explanation
* **Comparison:** The first column of $AB$ is $\begin{pmatrix} -1 \\ 2 \end{pmatrix} = Ab_1$, and the second column of $AB$ is $\begin{pmatrix} 2 \\ 1 \end{pmatrix} = Ab_2$. Thus, $AB = \begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix}$.
* **Explanation:** By definition of matrix multiplication, the $(i, j)$-th entry of $AB$ is the dot product of row $i$ of $A$ with column $j$ of $B$ ($b_j$). Collecting all rows $i = 1, \dots, m$ for a fixed column $j$ forms precisely the matrix-vector product $Ab_j$. Therefore, matrix multiplication acts column-by-column on the right factor:
  $$
  A \begin{pmatrix} b_1 & b_2 \end{pmatrix} = \begin{pmatrix} Ab_1 & Ab_2 \end{pmatrix}.
  $$

### Final Results
- $Ab_1 = \begin{pmatrix} -1 \\ 2 \end{pmatrix}$, $Ab_2 = \begin{pmatrix} 2 \\ 1 \end{pmatrix}$
- $AB = \begin{pmatrix} -1 & 2 \\ 2 & 1 \end{pmatrix}$