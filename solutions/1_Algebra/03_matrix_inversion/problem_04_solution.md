# Problem 04: Gauss–Jordan

## Question
### Given
Consider the matrix

$$
A=
\begin{pmatrix}
1 & 2 \\
3 & 5 \\
\end{pmatrix}.
$$

### Find
1. Find $A^{-1}$ using the Gauss–Jordan elimination method.
2. Show the augmented matrix $[A \mid I]$ after successive elementary row operations.
3. Explain why obtaining $I$ on the left gives $A^{-1}$ on the right.

## Solution

### 1. Gauss–Jordan Elimination on $[A \mid I]$
Form the $2 \times 4$ augmented matrix $[A \mid I_2]$:
$$
\left[\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
3 & 5 & 0 & 1
\end{array}\right]
$$

1. **Eliminate the entry below the first pivot ($R_2 \leftarrow R_2 - 3R_1$):**
   $$
   \left[\begin{array}{cc|cc}
   1 & 2 & 1 & 0 \\
   0 & -1 & -3 & 1
   \end{array}\right]
   $$

2. **Scale row 2 to make the second pivot equal to $1$ ($R_2 \leftarrow -R_2$):**
   $$
   \left[\begin{array}{cc|cc}
   1 & 2 & 1 & 0 \\
   0 & 1 & 3 & -1
   \end{array}\right]
   $$

3. **Eliminate the entry above the second pivot ($R_1 \leftarrow R_1 - 2R_2$):**
   $$
   \left[\begin{array}{cc|cc}
   1 & 0 & -5 & 2 \\
   0 & 1 & 3 & -1
   \end{array}\right]
   $$

Since the left block is now $I_2$, the right block is $A^{-1}$:
$$
A^{-1} = \begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix}.
$$

---

### 2. Why Obtaining $I$ on the Left Gives $A^{-1}$ on the Right
Each elementary row operation applied to $[A \mid I]$ is equivalent to multiplying both blocks on the left by an elementary matrix $E_i$. If a sequence of row operations $E_k \cdots E_2 E_1$ reduces $A$ to $I$, then letting $M = E_k \cdots E_2 E_1$:
$$
M [A \mid I] = [MA \mid MI] = [I \mid M].
$$
Because $MA = I$ (and $A$ is square), $M$ must be the unique inverse matrix $A^{-1}$. Consequently, the right-hand block $MI = M$ becomes $A^{-1}$.

### Verification
$$
AA^{-1} = \begin{pmatrix} 1 & 2 \\ 3 & 5 \end{pmatrix} \begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix} = \begin{pmatrix} -5 + 6 & 2 - 2 \\ -15 + 15 & 6 - 5 \end{pmatrix} = \begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} = I_2.
$$

### Final Result
$$
A^{-1} = \begin{pmatrix} -5 & 2 \\ 3 & -1 \end{pmatrix}
$$