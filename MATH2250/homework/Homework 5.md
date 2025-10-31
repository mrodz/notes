## Problem 1. Suppose all matrices are $n ×n$ over a field $F$.

### (a) If $AB= BA= I_n$ and $AC= CA= I_n$, prove that $B= C$. (Hence the inverse of a matrix, if it exists, is unique.)

1. Recall $BA=AC=I_n$
2. Recall any square matrix times the identity matrix is the same matrix
3. Hence, $B(I_n)=B$
4. Substitute for $I_n$ to get $B(AC)=B$
5. $B(AC)=(BA)C$ by matrix associativity
6. Substitute $BA$ for $I_n$ to get $(I_n)C=B$
7. Hence, $C=B$ $\blacksquare$

### (b) If $E$ is invertible, prove that $E^⊤$ is invertible and $(E^⊤)^{−1} =(E^{−1})^⊤$

1. Given $E$, $E$ is invertible
2. WTS $E^⊤$ is invertible
3. If $E$ is invertible, it has an inverse such that: $$\begin{equation}\begin{split}i.\quad&EE^{-1}=I_n\\ii.\quad& E^{-1}E=I_n\end{split}\end{equation}$$
4. WTS that given $E^⊤$, there exists some $M$ such that: $$\begin{equation}\begin{split}i.\quad&E^⊤M=I_n\\ii.\quad& ME^⊤=I_n\end{split}\end{equation}$$
5. If $M$ exists, $M$ must be $(E^⊤)^{-1}$
6. Recall: $(AB)^⊤=B^⊤A^⊤$
7. Suppose $M=(E^{-1})^⊤$
8. Apply the transpose operation to $EE^{-1}=I_n$. $$\begin{equation}\begin{split}EE^{-1}&=I_n\\E^⊤(E^{-1})^⊤&=I_n^⊤\\ E^⊤M&=I_n\end{split}\end{equation}$$
9. Apply the transpose operation to $E^{-1}E=I_n$ $$\begin{equation}\begin{split}E^{-1}E&=I_n\\(E^{-1})^⊤E^⊤&=I_n^⊤\\ ME^⊤&=I_n\end{split}\end{equation}$$
10. Hence, $M=(E^{-1})^⊤$ is the inverse of $E^⊤$
11. Since the inverse of $E^⊤$ is $(E^⊤)^{-1}$: $$(E^{-1})^⊤=(E^⊤)^{-1}$$

### (c) If $P$ and $Q$ are invertible, prove that $PQ$ is invertible and $(P Q)^{−1}= Q^{−1}P^{−1}$

1. If $P$ is invertible, there exists $P^{-1}$ such that $PP^{-1}= P^{-1}P=I_n$
2. If $Q$ is invertible, there exists $Q^{-1}$ such that $QQ^{-1}= Q^{-1}Q=I_n$
3. WTS there exists some $M$ such that $M(PQ)=I_n$ and $(PQ)M=I_n$
4. We want to find $M$. If we can find $M$, it exists and is the inverse of $PQ$ 
5. Try to find $M$ for $M(PQ)=I_n$ as follows: $$\begin{equation}\begin{split}M(PQ)&=I_n\\M(PQ)Q^{-1}&=I_nQ^{-1}\\MP&=Q^{-1}\\MP(P^{-1})&=Q^{-1}P^{-1}\\M&=Q^{-1}P^{-1}\end{split}\end{equation}$$
6. Try to find $M$ for $(PQ)M=I_n$ as follows: $$\begin{equation}\begin{split}(PQ)M&=I_n\\P^{-1}(PQ)M&=P^{-1}I_n\\QM&=P^{-1}\\(Q^{-1})QM&=Q^{-1}P^{-1}\\M&=Q^{-1}P^{-1}\end{split}\end{equation}$$
7. Hence, because $M$ is the same for both inverse calculations, $M=Q^{-1}P^{-1}$ is the inverse of $PQ$. Because $PQ$ has an inverse, by definition, it is invertible.

### (d) If $M$ is invertible and $X \neq 0$, prove that $M X\neq 0$.

1. If $M$ is invertible, there exists $M^{-1}$ such that $MM^{-1}= M^{-1}M=I_n$
2. Suppose $MX=0$
3. Apply $M^{-1}$ to both sides: $$\begin{equation}\begin{split}MX&=0\\M^{-1}MX&=M^{-1}(0)\\X&=M^{-1}(0)\end{split}\end{equation}$$
4. $M^{-1}(0) = 0 \implies X = 0$
5. This violates our initial condition that $X\neq 0$. Hence, $MX \neq 0$.

## Problem 2. Suppose $A$ and $B$ are distinct real $n ×n$ matrices satisfying $A^3 = B^3$ and $A^2B= B^2A$. Prove that $A^2 + B^2$ is not invertible.

1. Given:
	1. $AAA=BBB$
	2. $AAB=BBA$
	3. $A\neq B$ (keyword is "distinct")
2. WTS $A^2+B^2$ is not invertible
3. To do this, we can either try prove it's impossible to compute an inverse to $A^2+B^2$ (but this does not feel possible given what we learned in class) or try to find some nonzero vector that, when multiplied with $A^2+B^2$, equals zero. 
	1. WTS $\ker (A^2+B^2) \neq \{0\}$
4. Let $v$ be an $n\text{-dimensional}$ vector in $\mathbb{F}$
5. WTS $\exists v : (A^2+B^2)v=0$
6. Expand: $$\begin{equation}\begin{split}AAA&=BBB\\0&=AAA-BBB\\0&=AAA-BBB+AAB-AAB\\0&=AAA-AAB-BBB+AAB\\0&=AAA-AAB-BBB+BBA \text{ , sub AAB=BBA}\\0&=AA(A-B)-BB(B-A)\\0&=AA(A-B)+BB(A-B)\\0&=(AA+BB)(A-B)\\0&=(A^2+B^2)(A-B)\end{split}\end{equation}$$
7. Since $A\neq B$, the matrix $A-B$ is not zero. That means there exists a nonzero vector $w$ such that $(A-B)w\neq 0$
8. Let $v=(A-B)w$
9. Hence, $(A^2+B^2)(A-B)w=0$
10. That means $v\in \ker (A^2+B^2)$ 
11. And, that means $A^2+B^2$ sends a non-zero vector ($v$) to zero.
12. By definition, this means it's impossible for $A^2+B^2$ to have an inverse.
13. Hence, $A^2+B^2$ is NOT invertible. It doesn't have $\ker = \{0\}$

## Problem 3. The Fibonacci numbers are defined by $F_0 = 0, F_1 = 1, F_{n+2} = F_{n+1} + F_n$ for all $n ≥0$.

### (a) Prove the following.

Let:
$$M=\begin{pmatrix}1 & 1\\1 & 0\end{pmatrix}$$
WTS, for each k ≥1:
$$M^k=\begin{pmatrix}F_{k+1} & F_k\\F_k & F_{k-1}\end{pmatrix}$$

1. We go by induction.
2. At k=1, $$\begin{equation}\begin{split}M^1&=\begin{pmatrix}F_{1+1} & F_1\\F_1 & F_{1-1}\end{pmatrix}\\&=\begin{pmatrix}1 & 1\\1 & 0\end{pmatrix}\end{split}\end{equation}$$
3. Hence, the base case checks out.
4. Now, we want to check the $k+1$ case: $$\begin{equation}\begin{split}M^{k+1}=M^kM&=\begin{pmatrix}F_{k+1} & F_k\\F_k & F_{k-1}\end{pmatrix}\begin{pmatrix}1 & 1\\1 & 0\end{pmatrix}\\&=\begin{pmatrix}F_{k+1}+F_k & F_{k+1}\\F_{k}+F_{k-1} & F_k\end{pmatrix}\end{split}\end{equation}$$
5. Recall: $F_k+F_{k+1} = F_{k+2}$. 
	1. Subtracting one from k: $F_k+F_{k-1}=F_{k+1}$
6. Substitute: $$\begin{pmatrix}F_{k+2} & F_{k+1}\\F_{k+1} & F_k\end{pmatrix}$$
7. Identify (k+1) $$\begin{pmatrix}F_{(k+1)+1} & F_{(k+1)}\\F_{(k+1)} & F_{(k+1)-1}\end{pmatrix}$$
8. This has the same form as $M^k$. Hence, we're done by induction! $\blacksquare$

### (b) Prove that for all $m, n ∈\mathbb{N}$, $F_mF_n + F_{m−1}F_{n−1} = F_{m+n−1}$.

1. Assume $m,n \geq 1$
2. we'll use our work from part (a)
3. Let $M^m=\begin{pmatrix}F_{m+1} & F_m\\F_m & F_{m-1}\end{pmatrix}$
4. Let $M^{n-1}=\begin{pmatrix}F_{n} & F_{n-1}\\F_{n-1} & F_{n-2}\end{pmatrix}$
5. $M^{m+n-1}=M^mM^{n-1}=\begin{pmatrix}F_{m+1} & F_m\\F_m & F_{m-1}\end{pmatrix}\begin{pmatrix}F_{n} & F_{n-1}\\F_{n-1} & F_{n-2}\end{pmatrix}$
6. The product is $$\begin{pmatrix} F_{m+1}F_n + F_m F_{n-1} & F_{m+1}F_{n-1} + F_m F_{n-2}\\ F_m F_n + F_{m-1}F_{n-1} & F_m F_{n-1} + F_{m-1}F_{n-2} \end{pmatrix}$$
7. But if we set $k=m+n-1$ and directly plug that into M we get: $$\begin{pmatrix} F_{m+n} & F_{m+n-1}\\ F_{m+n-1} & F_{m+n-2} \end{pmatrix}$$
8. Hence, because the entries in the bottom left corner for identical matrices are the same, then we can imply $F_{m+n-1}=F_mF_n + F_{m−1}F_{n−1}$
	1. the identity holds for all $m,n≥1$
9. Done.

## Problem 4. Let $V= P_{≤3}(\mathbb{R})$, the space of real polynomials of degree at most 3. Define the linear map $L : V →V$ by $L[f (x)] = f (x + 1)−f (x)$.

### (a) Write the matrix for $L$ with respect to the basis $\{1, x, x^2, x^3\}$.

We are dealing with a $4\times 4$ matrix because the basis is size four and our map maintains dimensionality.

| basis term | L of basis term | output for matrix | x4  | x3  | x2  | x1  |
| ---------- | --------------- | ----------------- | --- | --- | --- | --- |
| $1$        | $1-1$           | 0                 | 0   | 0   | 0   | 0   |
| $x$        | $(x+1)-x$       | 1                 | 0   | 0   | 0   | 1   |
| $x^2$      | $(x+1)^2-x^2$   | $2x+1$            | 0   | 0   | 2   | 1   |
| $x^3$      | $(x+1)^3-x^3$   | $3x^2+3x+1$       | 0   | 3   | 3   | 1   |
my answer put together:

The matrix for $L$ with respect to the basis $\{1, x, x^2, x^3\}$ is:
$$
\begin{pmatrix}0 & 1 & 1 & 1  \\ 0 & 0 & 2 & 3 \\ 0 & 0 & 0 & 3 \\ 0 & 0 & 0 & 0\end{pmatrix}
$$
### (b) Write the matrix for $L$ with respect to the basis $\{1, x, x(x−1), x(x−1)(x−2)\}$.

Again our result will be a $4\times 4$ matrix because $L$ preserves dimension

| basis term    | L of basis term                                                                           | output for matrix | x4  | x3  | x2  | x1  |
| ------------- | ----------------------------------------------------------------------------------------- | ----------------- | --- | --- | --- | --- |
| $1$           | $1-1$                                                                                     | 0                 | 0   | 0   | 0   | 0   |
| $x$           | $x+1-x$                                                                                   | 1                 | 0   | 0   | 0   | 1   |
| $x(x-1)$      | $(x+1)(x+1-1)-x(x-1)$                                                                     | $2x$              | 0   | 0   | 2   | 0   |
| $x(x-1)(x-2)$ | $\begin{equation}\begin{split}(x+1)(x+1-1)(x+1-2)\\-x(x-1)(x-2)\end{split}\end{equation}$ | $3x^2-3x$         | 0   | 3   | 3   | 0   |
The matrix for $L$ with respect to the basis $\{1, x, x(x−1), x(x−1)(x−2)\}$.

$$
\begin{pmatrix}0 & 1 & 0 & 0  \\ 0 & 0 & 2 & 0 \\ 0 & 0 & 0 & 3 \\ 0 & 0 & 0 & 0\end{pmatrix}
$$


## Problem 5. Let $A, B, C$ be $n ×n$ matrices over a field $\mathbb{F}$ . Recall that $A$ is similar to $B$, written $A∼B$, if there exists an invertible matrix $S$ such that $A= SBS^{−1}$.

### (a) Prove that $A∼A$

1. WTS there exists some $S, S^{-1}$ such that $A= SAS^{−1}$
2. Let $S=I_n, S^{-1}=I_n^{-1}$
3. $A= I_nAI_n^{−1}$
4. Recall $I_n=I_n^-1$
5. $A= I_nAI_n$
6. $A=A$
7. Done. $\blacksquare$

### (b) If $A∼B$, prove that $B∼A$

1. Given $A ∼ B$
2. This implies that S exists such that $A= SBS^{−1}$
3. WTS that there exists some $M, M^{-1}$ such that $B= MAM^{−1}$
4. Multiply $S$ on the right and $S^{-1}$ on the left: $S^{-1}AS= S^{-1}SBS^{−1}S$
5. Now, we have: $S^{-1}AS= B$
6. $B=S^{-1}AS$
7. Now, consider that $S$ is $S^-1$'s inverse. So, we can say: $$B=MAM^{-1}$$
8. Hence, even though we used a different letter, we've shown that there exists some matrix $M$ such that left-multiplying A by M and right-multiplying A by $M^{-1}$ results in B.
9. This is the def of similarity. Hence, we are done. $\blacksquare$

### (c) If $A∼B$ and $B∼C$, prove that $A∼C$.

1. If $A∼B$, then there exists some matrix $X$ such that $A= XBX^{−1}$
2. If $B∼C$, then there exists some matrix $Y$ such that $B= YCY^{−1}$
3. WTS there exists some matrix $Z$ such that $A= ZCZ^{−1}$
4. Substitute B: $$\begin{equation}\begin{split}A&= XBX^{−1}\\&= X(YCY^{−1})X^{−1}\\&=(XY)C(Y^{-1}X^{-1})\end{split}\end{equation}$$
5. Let $Z=XY$. 
6. $X$ and $Y$ are invertible by the definition of similarity
7. By problem 1 c, the product of two invertible matrices is also invertible
8. Hence, $Z^{-1}$ exists.
9. Hence: $$A=ZCZ^{-1}$$
10. Hence, we're done. $A∼C$ $\blacksquare$

### (d) If $A∼B$, prove that $A^⊤∼B^⊤$

1. If $A∼B$, then there exists some matrix $X$ such that $A= XBX^{−1}$
2. WTS that there exists some matrix M such that $A^⊤= MB^⊤M^{−1}$
3. Transpose both sides: $$\begin{equation}\begin{split}A&= XBX^{−1}\\A^⊤&= (XBX^{−1})^⊤\\&= (X^{−1})^⊤B^⊤X^⊤\end{split}\end{equation}$$
4. By problem 2 b we know $(E^⊤)^{−1} =(E^{−1})^⊤$. Hence: $$\begin{equation}\begin{split}A^⊤&= (X^{−1})^⊤B^⊤X^⊤\\&=(X^⊤)^{−1}B^⊤X^⊤\end{split}\end{equation}$$
5. We know $X^⊤$ is invertible also by problem 2 b which states for any invertible matrix $E$, $E^⊤$ is also invertible
6. Let $M=(X^⊤)^{−1}$
7. Hence, we can show: $$\begin{equation}\begin{split}A^⊤&= MB^⊤M^{-1}\end{split}\end{equation}$$
8. By the definition of similarity, we're done. $A^⊤∼B^⊤$ $\blacksquare$

## Problem 6. Let $A$ and $B$ be $n ×n$ matrices. Recall that $\text{tr}(A)$ is the sum of the diagonal entries of $A$.

### (a) If $A∼B$, prove that $\text{rank}(A) = \text{rank}(B)$.

1. If $A∼B$, then there exists some matrix $X$ such that $A= XBX^{−1}$
2. WTS $\text{rank}(A)=\text{rank}(XB)$
	1. Let $v$ be an $n\text{-dimensional}$ vector
	2. Since $X$ is invertible, a linear transformation $L(v)=Xv$ is a bijection
	3. The image of $XB$ is $\{XBv : \forall v\}=X(\text{Im}(B))$
	4. Since $X$ is a bijection, it preserves linear independence and hence dimension. That means that: $$\dim(\text{Im}(XB))=\dim(\text{Im}(B))$$
3. WTS $\text{rank}(A)=\text{rank}(BX^{-1})$
	1. Let $v, w$ be $n\text{-dimensional}$ vectors
	2. Since $X^{-1}$ is invertible, a linear transformation $L(v)=X^{-1}v$ is a bijection
	3. The image of $BX^{-1}$ is $\{BX^{-1}v : \forall v\}=\{Bw : \forall w\}=\text{Im}(B)$
	4. So, $\dim(\text{Im}(BX^{-1}))=\dim(\text{Im}(B))$
4. The dimension of the image is the rank
5. Left-multiplication by an invertible matrix preserves rank
6. Right-multiplication by an invertible matrix preserves rank
7. So, $\text{rank}(XBX^{-1})=\text{rank}(BX^{-1})=\text{rank}(B)$
8. Hence, $\text{rank}(A)=\text{rank}(XBX^{-1})=\text{rank}(B)$

### (b) If $A∼B$, prove that $\text{tr}(A) = \text{tr}(B)$.

1. If $A∼B$, then there exists some matrix $X$ such that $A= XBX^{−1}$
2. Recall $\text{tr}(HK) = \text{tr}(KH)$ for square matrices
3. Apply $\text{tr}$ to both sides: $$\begin{equation}\begin{split}\text{tr}(A)&=\text{tr}( X(BX^{−1}))\\&=\text{tr}((BX^{-1})X)\\&=\text{tr}(B(X^{-1}X))\\&=\text{tr}(B)\end{split}\end{equation}$$
4. Done. $\blacksquare$.

### (c) Find two invertible matrices in Mat2×2(R) which are not similar.

1. I suspect opposite diagonals aren't similar
2. Matrix 1: $$A=\begin{pmatrix}2 & 0 \\0 & 2\end{pmatrix} \quad A^{-1}=\begin{pmatrix}.5 & 0 \\0 & .5\end{pmatrix}$$
3. Matrix 2: $$B=\begin{pmatrix}0 & 2 \\2 & 0\end{pmatrix}\quad B^{-1}=\begin{pmatrix}0 & .5 \\.5 & 0\end{pmatrix}$$
4. Are they invertible?
	1. Yes. $AA^{-1}=A^{-1}A=I_2$
	2. Yes. $BB^{-1}=B^{-1}B=I_2$
5. Are they similar?
6. The traces are different. You can see this visually. We saw that for any similar $A$ and $B$, $\text{tr}(A) = \text{tr}(B)$ by part b.
7. Hence, since our $A$ and $B$ violate the trace restriction, they cannot be similar $\blacksquare$
