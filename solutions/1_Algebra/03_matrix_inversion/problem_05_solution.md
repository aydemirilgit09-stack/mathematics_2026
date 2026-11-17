# Problem 05: A 3×3 Matrix

## Question
### Given
Consider the $3 \times 3$ matrix

$$
A=
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 1 \\
1 & 0 & 1 \\
\end{pmatrix}.
$$

### Find
Use Gauss–Jordan elimination to find $A^{-1}$, and verify the result by matrix multiplication.

## Solution

### 1. Gauss–Jordan Elimination on $[A \mid I_3]$
Set up the augmented matrix $[A \mid I_3]$:
$$
\left[\begin{array}{ccc|ccc}
1 & 1 & 0 & 1 & 0 & 0 \\
0 & 1 & 1 & 0 & 1 & 0 \\
1 & 0 & 1 & 0 & 0 & 1
\end{array}\right]
$$

1. **Eliminate the $(3,1)$ entry ($R_3 \leftarrow R_3 - R_1$):**
   $$
   \left[\begin{array}{ccc|ccc}
   1 & 1 & 0 & 1 & 0 & 0 \\
   0 & 1 & 1 & 0 & 1 & 0 \\
   0 & -1 & 1 & -1 & 0 & 1
   \end{array}\right]
   $$

2. **Eliminate the $(3,2)$ entry ($R_3 \leftarrow R_3 + R_2$):**
   $$
   \left[\begin{array}{ccc|ccc}
   1 & 1 & 0 & 1 & 0 & 0 \\
   0 & 1 & 1 & 0 & 1 & 0 \\
   0 & 0 & 2 & -1 & 1 & 1
   \end{array}\right]
   $$

3. **Normalize the third pivot ($R_3 \leftarrow \frac{1}{2}R_3$):**
   $$
   \left[\begin{array}{ccc|ccc}
   1 & 1 & 0 & 1 & 0 & 0 \\
   0 & 1 & 1 & 0 & 1 & 0 \\
   0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
   \end{array}\right]
   $$

4. **Eliminate the $(2,3)$ entry above the third pivot ($R_2 \leftarrow R_2 - R_3$):**
   $$
   \left[\begin{array}{ccc|ccc}
   1 & 1 & 0 & 1 & 0 & 0 \\
   0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
   0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
   \end{array}\right]
   $$

5. **Eliminate the $(1,2)$ entry above the second pivot ($R_1 \leftarrow R_1 - R_2$):**
   $$
   \left[\begin{array}{ccc|ccc}
   1 & 0 & 0 & \frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
   0 & 1 & 0 & \frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
   0 & 0 & 1 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
   \end{array}\right]
   $$

Reading off the right block gives:
$$
A^{-1} = \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{pmatrix} = \frac{1}{2}\begin{pmatrix}
1 & -1 & 1 \\
1 & 1 & -1 \\
-1 & 1 & 1
\end{pmatrix}.
$$

---

### Verification
Multiply $A$ by $A^{-1}$:
$$
AA^{-1} = \begin{pmatrix} 1 & 1 & 0 \\ 0 & 1 & 1 \\ 1 & 0 & 1 \end{pmatrix} \cdot \frac{1}{2}\begin{pmatrix} 1 & -1 & 1 \\ 1 & 1 & -1 \\ -1 & 1 & 1 \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 1+1+0 & -1+1+0 & 1-1+0 \\ 0+1-1 & 0+1+1 & 0-1+1 \\ 1+0-1 & -1+0+1 & 1+0+1 \end{pmatrix} = \frac{1}{2}\begin{pmatrix} 2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1 \end{pmatrix} = I_3.
$$

### Final Result
$$
A^{-1} = \begin{pmatrix}
\frac{1}{2} & -\frac{1}{2} & \frac{1}{2} \\
\frac{1}{2} & \frac{1}{2} & -\frac{1}{2} \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2}
\end{pmatrix}
$$