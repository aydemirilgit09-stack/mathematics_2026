# Problem 13: A Recurrence Written in Matrix Form

## Question
### Given
Let

$$
F=
\begin{pmatrix}
1 & 1 \\
1 & 0 \\
\end{pmatrix}.
$$

### Find
1. Compute $F^2$, $F^3$, $F^4$, and $F^5$.
2. Compare the numbers obtained with the sequence $0, 1, 1, 2, 3, 5, 8, \ldots$ and describe the relationship observed.
3. Compute $F \begin{pmatrix} a \\ b \end{pmatrix}$ and explain how this multiplication performs one recurrence step.

## Solution

### 1. Compute $F^2$, $F^3$, $F^4$, and $F^5$
* **Compute $F^2$:**
  $$
  F^2 = FF = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 1(1)+1(1) & 1(1)+1(0) \\ 1(1)+0(1) & 1(1)+0(0) \end{pmatrix} = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}
  $$
* **Compute $F^3$:**
  $$
  F^3 = F^2 F = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 2(1)+1(1) & 2(1)+1(0) \\ 1(1)+1(1) & 1(1)+1(0) \end{pmatrix} = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}
  $$
* **Compute $F^4$:**
  $$
  F^4 = F^3 F = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 3(1)+2(1) & 3(1)+2(0) \\ 2(1)+1(1) & 2(1)+1(0) \end{pmatrix} = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}
  $$
* **Compute $F^5$:**
  $$
  F^5 = F^4 F = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix} \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 5(1)+3(1) & 5(1)+3(0) \\ 3(1)+2(1) & 3(1)+2(0) \end{pmatrix} = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}
  $$

---

### 2. Relationship with the Fibonacci Sequence
Let the Fibonacci sequence be indexed as $f_0 = 0, f_1 = 1, f_2 = 1, f_3 = 2, f_4 = 3, f_5 = 5, f_6 = 8, \ldots$, where $f_{n+1} = f_n + f_{n-1}$.

Comparing the entries of $F^n$ for $n = 1, 2, 3, 4, 5$:
* $F^1 = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} f_2 & f_1 \\ f_1 & f_0 \end{pmatrix}$
* $F^2 = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix} = \begin{pmatrix} f_3 & f_2 \\ f_2 & f_1 \end{pmatrix}$
* $F^3 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix} = \begin{pmatrix} f_4 & f_3 \\ f_3 & f_2 \end{pmatrix}$
* $F^4 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix} = \begin{pmatrix} f_5 & f_4 \\ f_4 & f_3 \end{pmatrix}$
* $F^5 = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix} = \begin{pmatrix} f_6 & f_5 \\ f_5 & f_4 \end{pmatrix}$

In general, for any $n \ge 1$, the entries of $F^n$ are consecutive Fibonacci numbers:
$$
F^n = \begin{pmatrix} f_{n+1} & f_n \\ f_n & f_{n-1} \end{pmatrix}.
$$

---

### 3. Recurrence Step via Matrix-Vector Multiplication
Compute $F \begin{pmatrix} a \\ b \end{pmatrix}$:
$$
F \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1 & 1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} 1\cdot a + 1\cdot b \\ 1\cdot a + 0\cdot b \end{pmatrix} = \begin{pmatrix} a + b \\ a \end{pmatrix}.
$$

**Explanation:** If the input vector stores two consecutive terms $\begin{pmatrix} f_n \\ f_{n-1} \end{pmatrix}$ (with $a = f_n$ and $b = f_{n-1}$):
* The first row $\begin{pmatrix} 1 & 1 \end{pmatrix}$ sums both components to compute the next term $a + b = f_n + f_{n-1} = f_{n+1}$.
* The second row $\begin{pmatrix} 1 & 0 \end{pmatrix}$ shifts the previous leading term $a = f_n$ down into the second slot, advancing the state vector from $\begin{pmatrix} f_n \\ f_{n-1} \end{pmatrix}$ to $\begin{pmatrix} f_{n+1} \\ f_n \end{pmatrix}$.

### Verification
Starting with $\begin{pmatrix} f_1 \\ f_0 \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \end{pmatrix}$ and applying $F^5$:
$$
F^5 \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix} \begin{pmatrix} 1 \\ 0 \end{pmatrix} = \begin{pmatrix} 8 \\ 5 \end{pmatrix} = \begin{pmatrix} f_6 \\ f_5 \end{pmatrix},
$$
which accurately produces the 6th and 5th Fibonacci numbers.

### Final Results
- $F^2 = \begin{pmatrix} 2 & 1 \\ 1 & 1 \end{pmatrix}$, $F^3 = \begin{pmatrix} 3 & 2 \\ 2 & 1 \end{pmatrix}$, $F^4 = \begin{pmatrix} 5 & 3 \\ 3 & 2 \end{pmatrix}$, $F^5 = \begin{pmatrix} 8 & 5 \\ 5 & 3 \end{pmatrix}$
- $F \begin{pmatrix} a \\ b \end{pmatrix} = \begin{pmatrix} a+b \\ a \end{pmatrix}$