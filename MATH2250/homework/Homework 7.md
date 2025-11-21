## Problem 1
![[MATH 2250 problems 1, 2a.pdf]]
## Problem 2
### (a) *Done on paper.*
See above
### (b) Now suppose $χ_A(t)$ is as above, and $\dim E_1 = 2$ and $\dim E_{−2} = 1$, where $E_λ$ de-notes the eigenspace for $λ$. Prove that under this additional assumption, A must be diagonalizable.
1. From $\chi_A$, we get $\lambda_1=1$, $\lambda_2=-2$ 
2. The multiplicity of eigenvalue 1 in $\chi_A$ is 2, and the multiplicity of eigenvalue -2 in $\chi_A$ is 1. 
3. Eigenvectors corresponding to different eigenvalues are linearly independent 
4. Any set formed by taking linearly independent vectors from $E_1$ together with linearly independent vectors from $E_{-2}$ will be linearly independent overall
5. Hence, we can create a set of three linearly independent eigenvectors from $E_1 \cup E_{-2}$. 
	1. Since $\dim E_1 = 2$, 2 eigenvectors come from $E_1$
	2. Since $\dim E_{-2} = 1$, 1 eigenvector comes from $E_{-2}$
6. Since A is a $3\times 3$ matrix, any set of 3 linearly independent vectors forms a basis for ℝ³. Therefore, this set is an eigenbasis.
7. With respect to that eigenbasis, the representation of A is diagonal. In other words, A has a diagonal matrix representation with respect to this eigenbasis
8. Hence, A is diagonalizable

### (c) Given what you observed in part (b), write your own theorem statement which generalizes this fact. Explain, in two or three sentences, why you believe your theorem is true. You do not need to prove it. (There are multiple possible answers; try to think about the most general setup in which a fact like (b) might be true.)

I extrapolate from part (a) that the multiplicity of the eigenvalue factor term must equal the dimension of the corresponding eigenspace to guarantee diagonalizability.

My Theorem: let $A$ be an $n\times n$ matrix over a field $\mathbb{F}$. A is diagonalizable IFF:
1. The characteristic polynomial (call it $\chi_A(t)$) splits completely over $\mathbb{F}$ aka factors everything into linear factors.
2. For each eigenvalue $\lambda_i$ of $A$, the dimension of $E_{\lambda_i}$ equals the multiplicity of $\lambda_i$ in the characteristic polynomial $\chi_A(t)$

My informal explanation is that my theorem is true because when geometric multiplicity equals algebraic multiplicity for all eigenvalues, the sum of all geometric multiplicities equals n (the size of the matrix), giving us exactly n linearly independent eigenvectors. Recall that eigenvectors belonging to different eigenvalues are linearly independent. Critically, because the size is n and the dimension of the matrix is n, every eigenvector selected forms an eigenbasis. AND, this is the definition of diagonalizability.

## Problem 3
Suppose $A= PDP^{−1}$, where $D$ is diagonal with entries $λ_1,\dots,λ_n$.
### (a) Prove that $A^k = PD^kP^{−1}$ for any integer $k≥0$.

1. Let $D=\begin{pmatrix}\lambda_1 & \dots & 0 \\\vdots & \ddots & \vdots \\0 & \dots & \lambda_n \end{pmatrix}$
2. We go by induction.
3. Base case: k=0
	1. $PD^0P^{−1}=PI_n​P^{−1}$
	2. $=PP^{−1}$
	3. $=I_n$
	4. $​=A^0$
	5. Hence we've proven the base case
4. Inductive case: k=k+1
	1. $A^{k+1}=A^{k}A$
	2. $D^{k+1}=D^kD$
	3. We assume $A^k=PD^kP^{-1}$ holds.
	4. WTS k+1 case holds.
	5. $A^{k+1}=A^kA$ and $D^{k+1}=D^kD$
	6. Given: $A= PDP^{−1}$
	7. $A^{k}A = (PD^kP^{-1})\cdot(PDP^{-1})$
	8. Simplify: $$(PD^k(P^{-1}\cdot P)DP^{-1}) = PD^kDP^{−1}$$
	9. Result: $$A^{k+1} = PD^{k+1}P^{-1}$$
	10. We're done since we've shown that $A^{k+1} = PD^{k+1}P^{-1}$ holds.
5. Hence, by induction, we're done.


### (b) Suppose you were given a 5 ×5 matrix A which you were told was diagonalizable, and asked to compute the matrix power $A^{2025}$. Explain a step-by-step process for how you would do this computation in practice.

1. Find the eigenvalues of A
2. Find the eigenvectors of each eigenvalue
3. Since A is diagonalizable, you can find 5 linearly independent eigenvectors
4. Let P be a matrix formed from each eigenvector as a column: $$P=\begin{pmatrix}| & &|\\| && |\\v_1 & \dots\ & v_5\\| && |\\| && |\\\end{pmatrix}$$
5. P is invertible because every column is linearly independent
6. Let $D$ be another matrix. D is a diagonalizable matrix with the eigenvalues on each diagonal. $$D=\begin{pmatrix}\lambda_1 & \dots & 0 \\\vdots & \ddots & \vdots \\0 & \dots & \lambda_5 \end{pmatrix}$$
7. This makes computing $D^{2025}$ very easy. $$D^{2025}=\begin{pmatrix}\lambda_1^{2025} & \dots & 0 \\\vdots & \ddots & \vdots \\0 & \dots & \lambda_5^{2025} \end{pmatrix}$$
8. You can solve for the inverse of P and given the similarity relationship that we proved in (a), $$A^{2025} = PD^{2025}P^(-1)$$
9. This is big because raising $D^{2025}$ is a whole lot easier than some arbitrary $A^{2025}$. 
10. And we're done!
## Problem 4

### (a) The minimal polynomial $m_A(t)$ of $A$ is the monic polynomial of least degree with $m_A(A) = 0$. (Literally, this means plugging the matrix into the polynomial. For example, if $m_A(t) = 2t^2−1$, we say $m_A(A) = 2A^2−I$.). Prove that if A is diagonalizable, $m_A(t$) has no repeated roots.

1. Given: A is diagonalizable.
2. Hence, there exists some diagonal matrix $D$ and invertible matrix $P$ such that $A=PDP^{-1}$. Each $\lambda_{D,i}$ is an eigenvalue of $A$, possibly with repetition
3. $D=\begin{pmatrix}\lambda_{D,1} & \dots & 0 \\\vdots & \ddots & \vdots \\0 & \dots & \lambda_{D,n} \end{pmatrix}$
4. Ok. Now, let $\lambda_1, \dots, \lambda_k$ be the distinct eigenvalues of $A$.
5. A polynomial that only includes these eigenvalues looks like $$p(t)=(t-\lambda_1)\times\dots\times(t-\lambda_k)$$
6. Since the eigenvalues $\lambda_1, \ldots, \lambda_k$ are distinct, the polynomial p(t) has no repeated roots.
7. WTS $p(A)=0$
	1. Since $A=PDP^{-1}$, $$p(A)=p(PDP^{-1})=Pp(D)P^{-1}$$
	2. Because D is diagonal with eigenvalues on the diagonal (including repetitions), and p(t) contains each distinct eigenvalue as a root exactly once: $$p(D) = \begin{pmatrix}p(\lambda_{D,1}) & \dots & 0 \\ \vdots & \ddots & \vdots \\ 0 &\dots & p(\lambda_{D,n}) \end{pmatrix} = 0$$
	3. Each diagonal entry $\lambda_{D,i}$​ equals some $\lambda_j$, so $p(\lambda_{D,i})=0$
	4. Therefore, $p(λ_{D,i})=(λ_{D,i}−λ_1)⋯(λ_{D,i}−λ_k)=0$ since one factor is $(λ_{D,i}−λ_{D,i})=0$.
	5. Thus $p(D)=0$ (the zero matrix)
	6. Thus $p(A)=P0P^{−1}=0$
8. We're looking for $m_A(t)$ which is the polynomial of least degree, such that $m_A(A)=0$. We've already shown $p(A)=0$ where $p(t)$ is also monic. Hence, we know that $m_A(t)$ divides $p(t)$
9. Since $p(A)=0$ and $p(t)$ is monic, we have that $m_A(t)$ divides $p(t)$.
10. Let $p(t)=q(t)\times m_A(t)$ for some polynomial $q(t)$
11. Recall: $p(t)=(t-\lambda_1)\times\dots\times(t-\lambda_k)$. Since $m_A(t)$ divides $p(t)$ and $p(t)$ is completely factored into distinct linear factors, $m_A(t)$ must be a product of some non-empty subset of the linear factors $(t-\lambda_1), \dots, (t-\lambda_k)$
12. Since p(t) has no repeated roots, any divisor of $p(t)$, specifically, $m_A(t)$, can contain any factor in $(t-\lambda_1), \dots, (t-\lambda_k)$ with a multiplicity of at most 1. 
13. $m_A(t)$ must contain all of $(t-\lambda_1), \dots, (t-\lambda_k)$ at least once else $\lambda_i$ for all $i$ aren't eigenvalues.
	1. Suppose for contradiction that some $\lambda_x$ is an eigenvalue but $(t-\lambda_x)$ does not divide $m_A(t)$.
	2. Let v be a corresponding eigenvector to $\lambda_x$. So $v≠0$ and $Av=λ_xv$.
	3. For any polynomial $q(t)$, we have $q(A)v=q(λ_x)v$. This follows because $A^kv=λ_x^kv$ for all $k≥0$.
	4. Then, $m_A(A)v = m_A(\lambda_x)v$
	5. But $m_A(A) = 0$, so $m_A(\lambda_x)v=0$
	6. Since $v\neq 0$, we need $m_A(\lambda_x) = 0$, meaning $\lambda_x$ is a root of $m_A(t)$
	7. This contradicts our assumption. 
	8. Therefore, every eigenvalue $λ_i$​ must appear as a factor in $m_A(t)$
14. BIG HENCE: each linear factor $(t-\lambda_i)$ appears in $p(t)$ at least once (step 13) AND at most once (step 12). Therefore, it must appear exactly once in $m_A(t)$. HENCE: $m_A(t)$ cannot have repeated roots.
15. Done

### (b) Prove or disprove: any two nonzero $2 ×2$ diagonalizable matrices have minimal polynomials of the same degree.

1. I have a sneaky suspicion it is false. So, we go by counterexample
2. $A=\begin{pmatrix}1 & 0 \\ 0 & 1\end{pmatrix} = I_2$
3. $B=\begin{pmatrix}1 & 0 \\ 0 & 2\end{pmatrix}$
4. Assume $\deg(m_A(t))=\deg(m_B(t))$
5. A and B are both diagonalizable because they are already diagonal.
6. WTS A and B have minimal polynomials with different degrees
7. Find $m_A(t)$
	1. $A=I_2$ has a single eigenvalue of $\lambda= 1$
	2. We check $A-I_2=0$
	3. So, $m_A(t)=t-1$
	4. Degree = 1
8. Find $m_B(t)$
	1. $B$ has two eigenvalues of $\lambda=1$ and $\lambda=2$
	2. The minimal polynomial must have both eigenvalues as roots
	3. $m_B(t)=(t-1)(t-2)$
	4. Degree = 2
9. Since the degree of $m_A(t)=1$ and $m_B(t)=2$ and $1\neq 2$, we've shown the contrary.
10. Hence, any two nonzero $2 ×2$ diagonalizable matrices are not forced to have minimal polynomials of the same degree.