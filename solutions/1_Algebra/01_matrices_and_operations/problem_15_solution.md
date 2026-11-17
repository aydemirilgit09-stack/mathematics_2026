# Problem 15: Associativity of Multiplication and Different Calculation Paths

## Question
### Given
Given

$$
A=
\begin{pmatrix}
1 & 2 & 0 \\
0 & 1 & 1 \\
\end{pmatrix},\quad B=
\begin{pmatrix}
1 & 0 \\
2 & 1 \\
-1 & 3 \\
\end{pmatrix},\quad C=
\begin{pmatrix}
2 & 1 \\
0 & -1 \\
\end{pmatrix}.
$$

### Find
1. Compute $(AB)C$ and $A(BC)$.
2. Compare the results and the number of intermediate operations.
3. Explain what associativity of matrix multiplication means in this example.

## Solution

### 1. Path 1: Compute $(AB)C$
**Step 1a: Compute $AB$** ($A$ is $2 \times 3$, $B$ is $3 \times 2$, so $AB$ is $2 \times 2$):
$$
AB = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} = \begin{pmatrix} 1(1)+2(2)+0(-1) & 1(0)+2(1)+0(3) \\ 0(1)+1(2)+1(-1) & 0(0)+1(1)+1(3) \end{pmatrix} = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix}
$$

**Step 1b: Multiply $(AB)$ by $C$** ($(AB)$ is $2 \times 2$, $C$ is $2 \times 2$, so $(AB)C$ is $2 \times 2$):
$$
(AB)C = \begin{pmatrix} 5 & 2 \\ 1 & 4 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix} = \begin{pmatrix} 5(2)+2(0) & 5(1)+2(-1) \\ 1(2)+4(0) & 1(1)+4(-1) \end{pmatrix} = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}
$$

---

### 2. Path 2: Compute $A(BC)$
**Step 2a: Compute $BC$** ($B$ is $3 \times 2$, $C$ is $2 \times 2$, so $BC$ is $3 \times 2$):
$$
BC = \begin{pmatrix} 1 & 0 \\ 2 & 1 \\ -1 & 3 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 0 & -1 \end{pmatrix} = \begin{pmatrix} 1(2)+0(0) & 1(1)+0(-1) \\ 2(2)+1(0) & 2(1)+1(-1) \\ -1(2)+3(0) & -1(1)+3(-1) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix}
$$

**Step 2b: Multiply $A$ by $(BC)$** ($A$ is $2 \times 3$, $(BC)$ is $3 \times 2$, so $A(BC)$ is $2 \times 2$):
$$
A(BC) = \begin{pmatrix} 1 & 2 & 0 \\ 0 & 1 & 1 \end{pmatrix} \begin{pmatrix} 2 & 1 \\ 4 & 1 \\ -2 & -4 \end{pmatrix} = \begin{pmatrix} 1(2)+2(4)+0(-2) & 1(1)+2(1)+0(-4) \\ 0(2)+1(4)+1(-2) & 0(1)+1(1)+1(-4) \end{pmatrix} = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}
$$

---

### 3. Comparison of Results, Operation Counts, and Meaning of Associativity
* **Comparison of Results:** Both paths yield the exact same matrix:
  $$
  (AB)C = A(BC) = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}.
  $$
* **Comparison of Intermediate Operations:**
  For multiplying an $m \times k$ matrix by a $k \times n$ matrix, the standard algorithm requires $m \cdot k \cdot n$ scalar multiplications and $m \cdot (k - 1) \cdot n$ scalar additions:
  * **Path 1 $(AB)C$:**
    * $AB$ ($2 \times 3$ by $3 \times 2$): $2 \times 3 \times 2 = 12$ multiplications and $2 \times 2 \times 2 = 8$ additions.
    * $(AB)C$ ($2 \times 2$ by $2 \times 2$): $2 \times 2 \times 2 = 8$ multiplications and $2 \times 1 \times 2 = 4$ additions.
    * **Total for $(AB)C$:** **$20$ scalar multiplications** and **$12$ scalar additions** ($32$ operations).
  * **Path 2 $A(BC)$:**
    * $BC$ ($3 \times 2$ by $2 \times 2$): $3 \times 2 \times 2 = 12$ multiplications and $3 \times 1 \times 2 = 6$ additions.
    * $A(BC)$ ($2 \times 3$ by $3 \times 2$): $2 \times 3 \times 2 = 12$ multiplications and $2 \times 2 \times 2 = 8$ additions.
    * **Total for $A(BC)$:** **$24$ scalar multiplications** and **$14$ scalar additions** ($38$ operations).
  * Thus, computing $(AB)C$ is more efficient because $AB$ reduces the intermediate matrix to a smaller $2 \times 2$ size before multiplying by $C$.
* **Meaning of Associativity:** Even though matrix multiplication is not commutative ($AB \neq BA$), it is **associative**: as long as the left-to-right order $A, B, C$ is preserved, grouping adjacent pairs differently does not change the final matrix. This allows us to choose the parenthesization that minimizes computational work.

### Final Result
$$
(AB)C = A(BC) = \begin{pmatrix} 10 & 3 \\ 2 & -3 \end{pmatrix}.
$$