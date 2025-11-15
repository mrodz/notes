## Problem 1

### (a) Triumphing over the past. Suppose that $T : V →V$ is a linear transformation from a finite-dimensional vector space to itself. Suppose $im(T ) ∩ ker(T ) = 0$. Prove that $rank(T ) = rank(T ◦T )$.

1. Given: $im(T) \cap ker(T) = 0$
2. Let B = T(V). $im(T \circ T) = T(B) \subseteq B$
3. Hence, $dim(im(T\circ T)) <= dim(im(T))$ because $im(T\circ T)$ is a subset of $im(T)$
4. Let $x \in im(T)$
5. If T(x)=0, given $x \in im(T)$ and $x \in ker(T)$, but the only intersection of the image and the kernel is $\{0\}$, then $x=0$.
6. This shows that $T$ is injective on its image, aka when it is restricted to $B=im(T)$
7. Since $T$ is injective on $im(T)$, The linear map $T:im(T)→T(im(T))=im(T∘T)$ is injective
8. $im(T \circ T)=T(im T)$, and we know that the $T$ map is injective onto its image, the dimension of the image is the dimension of the domain.
9. Thus, we can write $dim(im(T\circ T))=dim(im(T))$
10. Thus, $rank(T \circ T) = rank(T)$
11. Done $\blacksquare$

### (b) Find an example of a linear transformation $T : V →V$ where $im(T ) ∩ker(T ) \neq 0$. Compute $rank(T )$ and $rank(T ◦T )$ in this specific case.

1. T in $\mathbb{R}^2 \to \mathbb{R}^2$
2. Let T: $$T\begin{pmatrix}x\\y\end{pmatrix}=\begin{pmatrix}y\\0\end{pmatrix}$$
3. Find $ker(T)$.
	1. x= any R, y= 0.
	2. Hence, the kernel is $c\begin{pmatrix}1\\0\end{pmatrix}\forall c \in \mathbb{R}$
4. Find $im(T)$
	1. It is $(x)\begin{pmatrix}1\\0\end{pmatrix}$
	2. So, $im(T)=c\begin{pmatrix}1\\0\end{pmatrix}\forall c \in \mathbb{R}$
5. rank(T)
	1. By rank nullity, $$\begin{equation}\begin{split}dim(\mathbb{R}^2)&=rank(T)+dim(ker(T))\\2&=dim(im(T))+1\end{split}\end{equation}$$
	2. rank(T)=1
6. $T(T(x,y))=T(y,0)=(0,0)$.
7. Thus, $T\circ T$ sends every vector to (0, 0)
8. Hence, $\ker(T\circ T) = (x, y) \forall x\in\mathbb{R}, y \in \mathbb{R}$
9. Hence, $\dim(\ker(T\circ T)) = 2$
10. By rank-nullity, $dim(im(T \circ T))+dim(ker(T \circ T))=dim(\mathbb{R}^2) \implies rank(T \circ T) + 2 = 2$
11. So, $rank(T \circ T) = 0$
12. Done $\blacksquare$

## Problem 2. Recall that $det : Mat_{n×n}(F ) →F$ is a function satisfying:

(i) det is multilinear in the rows;
(ii) det is zero on any matrix with two equal rows;
(iii) det($I_n$) = 1.

Without using any explicit formula for det, just using the above properties...

### (a) Prove that det changes sign when the rows of a matrix are flipped.
1. Let A be an $n\times n$ matrix. Its rows are $r_1, r_2, r_3, ..., r_n$
2. Let A' be the matrix where $r_1$ and $r_2$ are swapped
3. WTS $det(A)=-det(A')$
4. We know we can build a matrix with two equal rows to get det = 0
5. Let C be the matrix: $\begin{pmatrix}r_1+r_2\\r_1+r_2\\r_3\\...\\r_n\end{pmatrix}$
6. det(C) is zero by axiom (ii)
7. By axiom (i), we can expand det(C) many times: $$\begin{equation}\begin{split}\det(\begin{pmatrix}r_1+r_2\\r_1+r_2\\r_3\\...\\r_n\end{pmatrix})&=\det(\begin{pmatrix}r_1\\r_1+r_2\\r_3\\...\\r_n\end{pmatrix})+\det(\begin{pmatrix}r_2\\r_1+r_2\\r_3\\...\\r_n\end{pmatrix})\\0&=\det(\begin{pmatrix}r_1\\r_1\\r_3\\...\\r_n\end{pmatrix})+\det(\begin{pmatrix}r_1\\r_2\\r_3\\...\\r_n\end{pmatrix})+\det(\begin{pmatrix}r_2\\r_1\\r_3\\...\\r_n\end{pmatrix})+\det(\begin{pmatrix}r_2\\r_2\\r_3\\...\\r_n\end{pmatrix})\\0&=0+\det(A)+\det(A')+0\\0&=\det(A)+\det(A')\\\det(A)&=-\det(A')\end{split}\end{equation}$$
8. The same argument applies to swapping adjacent rows $r_i$​ and $r_{i+1}$​
9. Each adjacent swap changes the sign, so swapping any two rows changes the sign
10. Done $\blacksquare$

### (b) If a row of A is the zero vector, then det(A) = 0.

1. Let the zero row of a matrix A be row $i$
2. The row can be expressed as zero times any arbitrary vector of length $n$, call it $v_i$
3. By axiom (i), we know that the multilinear det(A) means that we can factor out the zero: $$\begin{equation}\begin{split}\det\begin{pmatrix}r_1\\r_2\\...\\r_i\\...\\r_n\end{pmatrix}&=\det\begin{pmatrix}r_1\\r_2\\...\\0 * v_i\\...\\r_n\end{pmatrix}\\&=0*\det\begin{pmatrix}r_1\\r_2\\...\\ v_i\\...\\r_n\end{pmatrix}\\&=0\end{split}\end{equation}$$
4. Done $\blacksquare$

### (c) If one row of A is a linear combination of the others, then $det(A) = 0$.

1. Let row $i$ be a linear combination of the others.
2. Thus, $r_i = a_1r_1 + a_2r_2 + a_{i-1}r_{i-1} + a_{i+1}r_{i+1} + ... + a_nr_n$ not including $a_ir_i$ for some scalars $a_k$
3. so, determinant of A is (shortened the sum visually, but recall $r_i$ does not include $a_ir_i$): $$\det\begin{pmatrix}r_1\\...\\r_i\\...\\r_n\end{pmatrix}=\det\begin{pmatrix}r_1\\...\\a_1r_1 + a_2r_2 + a_{i-1}r_{i-1} + a_{i+1}r_{i+1} + ... + a_nr_n\\...\\r_n\end{pmatrix}$$
4. By axiom (i), we can split the determinant into a sum of multiple determinants
5. Thus $$=a_1\det\begin{pmatrix}r_1\\...\\r_1\\...\\r_n\end{pmatrix}+a_2\det\begin{pmatrix}r_1\\...\\r_2\\...\\r_n\end{pmatrix}+...+a_{i-1}\det\begin{pmatrix}r_1\\...\\r_{i-1}\\...\\r_n\end{pmatrix}+a_{i+1}\det\begin{pmatrix}r_1\\...\\r_{i+1}\\...\\r_n\end{pmatrix}+a_n\det\begin{pmatrix}r_1\\...\\r_n\\...\\r_n\end{pmatrix}$$
6. In each determinant, there are at least two rows that match every time.
	1. Row i and row j are identical (both equal to rj​).
7. Hence, by axiom (ii), det(A)=zero.
8. Done $\blacksquare$

---

![[images/MATH 2250 Homework 6 P3.png]]
![[images/MATH 2250 Homework 6 P4.png]]


----

## Problem 5

### (a) Let A be a square matrix and R its RREF. Show that $\det(A) = 0$ if and only if $R \neq I_n$.

1. First: WTS given $R \neq I_n$, $\det(A)=0$
	1. If $R \neq I_n$, $rank(R)<n$, so there must be linear dependence between at least two rows of R
	2. Since row operations preserve linear dependence relations, the rows of A are also linearly dependent
	3. We already proved that if one row of A is a linear combination of the others, then $det(A) = 0$.
	4. Done
2. Second: WTS given $\det(A)=0$, $R \neq I_n$
	1. Suppose $\det(A) =0$ and $R=I_n$ (We go for proof by contradiction)
	2. There exists some matrix M that can be built from the elementary row operations used to create A's reduced row echelon form, such that $$MA=R$$
	3. M can be written as $M=E_kE_{k-1} ... E_2E_1$ for some integer number $k$ elementary row operations
	4. WTS that applying every $E_i$ ERO to the matrix $E_{i-1}E_{i-2}...E_1A$ does not produce a zero determinant
		1. ERO #1: a row swap - does not produce a zero determinant, as it flips the sign as proven in 2.a
		2. ERO #2: multiplying a row by nonzero scalar c (where c is nonzero) multiplies the determinant by c, giving $\det(E) ≠ 0$
		3. ERO #3: adding a multiple of one row to another does not change the determinant
			1. Let $Y=E_i^3H$ be an ERO #3 applied to some arbitrary matrix H on row $i$.
			2. $Y = \begin{pmatrix}r_1\\...\\r_i+Gr_j\\...\\r_n\end{pmatrix}$
			3. G is the multiple of row $j$ added to row $i$.
			4. $\det(Y) = \det \begin{pmatrix}r_1\\...\\r_i+Gr_j\\...\\r_n\end{pmatrix}=\det \begin{pmatrix}r_1\\...\\r_i\\...\\r_j\\...\\r_n\end{pmatrix}+G\det \begin{pmatrix}r_1\\...\\r_j\\...\\r_j\\...\\r_n\end{pmatrix}$
			5. But, since the rightmost determinant is linearly dependent, its determinant is zero.
			6. So, the determinant is exactly the same.
			7. Hence, the determinant of adding a multiple of one row to another does not change the determinant.
		4. By these facts, we know that $det(E_i)\neq 0$ for all $i$
	5. Since $M = E_k...E_1$ and $\det(E_i) ≠ 0$ for all $i$, we have $$\det(M) = det(E_k)*det(E_{k-1})*...*det(E_1) ≠ 0$$
	6. Applying the determinant and the multiplicative property, we get: $$\det(M)*\det(A)=\det(R)$$
	7. We know that $R=I_n$ and the determinant of the identity matrix is 1, hence: $$\det(M)*\det(A)=1$$
	8. So, $\det(A)$ cannot be zero, or else this will not hold up: $$\det(M)*0=1$$
	9. But, $\det(A)=0$ by assumption. This is a contradiction. 
	10. Our assumption is false, hence $R \neq I_n$
3. We've proven both directions. Hence, we're done $\blacksquare$

### (b) Give an example of two $3×3$ matrices with the same RREF but different determinants, and explain why this does not contradict part (a).

1. Let A be $\begin{pmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{pmatrix}$
2. Let B be $\begin{pmatrix}2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2\end{pmatrix}$
3. Because one of the elementary row operations is scalar multiplication, we can multiply each row of B by 0.5 in our search for its reduced row echelon form. 
4. Hence, RREF of A = RREF of B = $\begin{pmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{pmatrix}$= $I_3$
5. So, we've found two $3 \times 3$ matrices with the same RREF, but the determinants are clearly different. $$\begin{equation}\begin{split}\det(A)&=1\\\det(B)&=2*\det\begin{pmatrix}2 & 0\\0 & 2\end{pmatrix}=2*2*2=8\end{split}\end{equation}$$
6. This doesn't contradict part a because of the multiplicity of determinants. For matrix B, $$\det\begin{pmatrix}2 & 0 & 0 \\ 0 & 2 & 0 \\ 0 & 0 & 2\end{pmatrix}=2^3\det \begin{pmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{pmatrix}$$
7. And since we know that the determinant of the identity matrix is nonzero, even though $B\neq I_n$, $RREF_B = I_n$, so $\det(B)\neq 0$
8. Summed up: since both matrices have $RREF=I_3$​, part a. correctly predicts that both have nonzero determinants. Notably part A does not determine the values of these nonzero determinants, which is how we get differing det's
