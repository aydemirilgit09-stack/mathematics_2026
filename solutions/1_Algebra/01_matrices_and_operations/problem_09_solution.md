# Problem 09: Composing Transformations

## Question
### Given
Let

$$
S=
\begin{pmatrix}
2 & 0 \\
0 & 1 \\
\end{pmatrix},\qquad R=
\begin{pmatrix}
0 & -1 \\
1 & 0 \\
\end{pmatrix}, \qquad x=
\begin{pmatrix}
1 \\
2 \\
\end{pmatrix}.
$$

The matrix $S$ describes nonuniform scaling, while $R$ describes a $90^\circ$ counterclockwise rotation.

### Find
1. Compute $RSx$ and $SRx$.
2. Compare the results and explain geometrically why the order of these transformations matters.

## Solution

### 1. Compute $RSx$ (First Scale, Then Rotate)
Matrix multiplication associates with vector application, so $RSx = R(Sx)$.

First, apply $S$ to $x$:
$$
Sx = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 2(1) + 0(2) \\ 0(1) + 1(2) \end{pmatrix} = \begin{pmatrix} 2 \\ 2 \end{pmatrix}
$$

Next, apply $R$ to the resulting vector $Sx$:
$$
RSx = R(Sx) = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 2 \\ 2 \end{pmatrix} = \begin{pmatrix} 0(2) + (-1)(2) \\ 1(2) + 0(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 2 \end{pmatrix}
$$

---

### 2. Compute $SRx$ (First Rotate, Then Scale)
Similarly, $SRx = S(Rx)$.

First, apply $R$ to $x$:
$$
Rx = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} \begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} 0(1) + (-1)(2) \\ 1(1) + 0(2) \end{pmatrix} = \begin{pmatrix} -2 \\ 1 \end{pmatrix}
$$

Next, apply $S$ to the resulting vector $Rx$:
$$
SRx = S(Rx) = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} \begin{pmatrix} -2 \\ 1 \end{pmatrix} = \begin{pmatrix} 2(-2) + 0(1) \\ 0(-2) + 1(1) \end{pmatrix} = \begin{pmatrix} -4 \\ 1 \end{pmatrix}
$$

---

### 3. Comparison and Geometric Explanation
* **Comparison:** $RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix} \neq \begin{pmatrix} -4 \\ 1 \end{pmatrix} = SRx$.
* **Geometric Reason:** The matrix $S$ stretches coordinates only along the **horizontal ($x$-axis)** by a factor of $2$ while leaving the vertical ($y$-axis) unchanged.
  * In $RSx$, the original $x$-coordinate ($1$) is doubled to $2$ **before** rotation, and then the $90^\circ$ counterclockwise rotation moves that stretched coordinate onto the $y$-axis, giving $(-2, 2)^T$.
  * In $SRx$, the rotation happens **first**, moving the original $y$-coordinate ($2$) onto the negative $x$-axis as $-2$, and then $S$ doubles that new $x$-coordinate to $-4$, giving $(-4, 1)^T$.
  * Because nonuniform scaling depends on axis alignment and rotation changes which component lies along each axis, the two operations do not commute ($RS \neq SR$).

### Verification
Computing the composite matrices $RS$ and $SR$ directly confirms both vectors:
$$
RS = \begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix} = \begin{pmatrix} 0 & -1 \\ 2 & 0 \end{pmatrix} \implies RSx = \begin{pmatrix} 0 & -1 \\ 2 & 0 \end{pmatrix}\begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} -2 \\ 2 \end{pmatrix},
$$
$$
SR = \begin{pmatrix} 2 & 0 \\ 0 & 1 \end{pmatrix}\begin{pmatrix} 0 & -1 \\ 1 & 0 \end{pmatrix} = \begin{pmatrix} 0 & -2 \\ 1 & 0 \end{pmatrix} \implies SRx = \begin{pmatrix} 0 & -2 \\ 1 & 0 \end{pmatrix}\begin{pmatrix} 1 \\ 2 \end{pmatrix} = \begin{pmatrix} -4 \\ 1 \end{pmatrix}.
$$

### Final Results
- $RSx = \begin{pmatrix} -2 \\ 2 \end{pmatrix}$
- $SRx = \begin{pmatrix} -4 \\ 1 \end{pmatrix}$