## Problem 1.
Suppose $V$ is a vector space over a field $\mathbb{F}$ . Suppose $I$ and $S$ are finite subsets of $V$,
that $I$ is linearly independent, and that $S$ spans $V$.

### (a) Show that there exists a set $B$ such that $I ⊆B ⊆I ∪S$ and $B$ is a basis for $V$.
1. We use Steinitz-Exchange Lemma to prove $B$ is a basis for $V$.
2. If $S$ is linearly independent, then $S$ is a basis of $V$ because it spans
3. If $S$ is not linearly independent, keep removing the redundant vectors in the span of others until the subset is linearly independent and still spans to get a basis
4. Let $w \subseteq S$ be a basis of $V$ by the logic in step 2 and 3, and $w=\{x_1, ..., x_n\}$
5. Let $I=\{v_1,...,v_m\}$
6. $w$ spans $V$ by def of basis
7. The Steinitz-Exchange Lemma tells us we can form a basis of $V$ by replacing vectors in $w$ (already a basis) with vectors in a linearly independent $I$. Then by the Steinitz-Exchange Lemma, there exist indices such that the following is also a basis of $V$. $$B=\{v_1,...,v_m,x_{m+1},...,x_n\}$$
8. Recall $B$ contains vectors in $S$ (the $\{x_{m+1}, ..., x_n\}$ part) as well as $I$ (the $\{v_1,...,v_m\}$ part)
9. So, all of $I$ is contained in $B$ because that's the whole point of replacing, using the Lemma:
	1. $I \subseteq B$
10. Also, $B$ is made up of vectors in either $S$ or $I$:
	1. $B \subseteq S \cup I$
11. Hence, $I \subseteq B \subseteq I \cup S \quad \blacksquare$
---
### (b) Find a space $U ≤\mathbb{R}^2$ and a set $S ⊆\mathbb{R}^2$ where $U ⊆span(S)$ but no subset of $S$ is basis for $U$ . Prove your example works.

1. We want to find essentially a very "generous" span of S and a more "constrained" U
2. A set of two nonzero perpendicular vectors (ie. (-5,5) and (-5,-5)) have a span of $\mathbb{R}^2$ because two nonzero vectors are linearly independent. It can also be visually determined; see Desmos: ![[Pasted image 20251003010750.png]]
3. But, now we can find a subspace $U$ of which $\big\{\begin{pmatrix}-5\\5\end{pmatrix}, \begin{pmatrix}-5\\-5\end{pmatrix}\big\}$ is not a basis
4. We know that $U$ has to be a line since it cannot be $\mathbb{R}^2$ itself and by the definition of a subspace.
5. Let $U$ be the x-axis ($U=\{(x,0) : x \in \mathbb{R}\}$), which is a subspace of $\mathbb{R}^2$.
6. A basis for $U$ must be inside $U$.
	1. $\{(-5, 5)\}$ is not a basis for $U$ because it does not fall on the $X$ axis.
	2. $\{(-5, -5)\}$ is not a basis for $U$ because it does not fall on the $X$ axis
7. Since $U$ is one dimensional, a basis of $U$ has one nonzero vector in $U$ (def of basis)
	1. Hence, $\big\{\begin{pmatrix}-5\\5\end{pmatrix}, \begin{pmatrix}-5\\-5\end{pmatrix}\big\}$ cannot be a basis for $U$ because it is two-dimensional!
8. An empty subset can't span the x-axis
9. Hence, no subsets of $S$ are a basis for $U$.
10. Hence, we've shown that if $U=\{(x,0) : x \in \mathbb{R}\}$ and $S=\big\{\begin{pmatrix}-5\\5\end{pmatrix}, \begin{pmatrix}-5\\-5\end{pmatrix}\big\}$, $U ⊆span(S)$ but no subset of $S$ is basis for $U$ . $\blacksquare$

---
## Problem 2.
Suppose $U$ and $V$ are vector spaces over a field $F$ and $U ≤V$. Further suppose $V$ is finite dimensional.

### (a) Prove that $dim(U ) ≤dim(V )$ and that $dim(U ) = dim(V )$ if and only if $U= V$.
1. WTS $dim(U) \leq dim(V)$
2. Let $u = \{u_1, u_2, ..., u_m\}$ be a basis of $U$. Because $U \leq V$, $u \subseteq V$.
3. $dim(U)=\text{ number of elements in } u = m$
4. Let $dim(V) = n$
5. By Steinitz Lemma, we can extend $u$ to be a basis of $V$ by adding some (or no) elements of $V$ to form:$$B=\{u_1,...,u_m,v_{m+1},...,v_n\}$$
6. Therefore any extension has exactly $n$ vectors, so $m\leq n$.
7. Hence,  $dim(U ) ≤dim(V )$
8. Now, we WTS $dim(U)=dim(V)$ iff $U=V$
9. Case 1. Let $dim(U)=dim(V)$
	1. WTS $U=V$.
	2. Since $dim⁡(U)=m=n=dim⁡(V)$, the basis $\{u_1,…,u_n\}$ of $U$ consists of n-linearly independent vectors in $V$ (since $U≤V$).
	3. Since $V$ has dimension $n$, any linearly independent set of $n$ vectors in $V$ is a basis for $V$.
	4. Therefore, $\{u_1,…,u_n\}$ spans $V$
	5. Hence $U=span({u_1,...,u_n})=V$
10. Case 2. Let $U=V$
	1. WTS $dim(U)=dim(V)$
	2. But if $U$ and $V$ are equal, then a basis of $U$ is also a basis of $V$. Hence they must have the same dimension
11. Therefore, $dim(U ) = dim(V )$ if and only if $U= V$ $\blacksquare$

---
### (b) Suppose $S ⊆V$ and $|S|= dim(V )$. Prove that the following are equivalent:

1. (i) $S$ is a basis for $V$
	1. If $S$ is a basis for $V$, then $S$ is linearly independent and also spans  (def of a basis). Easy! $\blacksquare$
2. (ii) $S$ spans $V$
	1. Every spanning set contains a basis
	2. Thus, $S$ contains some basis $B$ of $V$
	3. Any basis of $V$ has exactly $dim(V)$ elements. 
	4. So, $|B|=dim(V)$.
	5. Given $B\subseteq S$, we must have $B=S$. 
	6. Hence, $B$ is also a basis for $V$.
	7. Hence, by case (i), we're done $\blacksquare$
3. (iii) $S$ is linearly independent
	1. If $S$ is linearly independent, then it can be extended to a basis using Steinitz's lemma.
	2. Let $W=\{w_1, ..., w_n\}$ be a basis of $V$
	3. Let $S = \{v_1, ..., v_n\}$
	4. By Steinitz's Exchange Lemma, since $S$ is linearly independent and $W$ spans $V$ (def of basis), we can replace elements of $W$ with elements of $S$ to obtain a spanning set.
	5. Since $S$ and $W$ have the same size $n$, we can perform $n$ exchanges until we receive $S$ itself as a spanning set for $V$.
	6. Since $S$ is linearly independent and also spans $V$, then it must be a basis for $V$.
	7. Hence, by case (i), we're done. $\blacksquare$

---

## Problem 3. 
Consider each of the following as vector spaces over $\mathbb{R}$.

### (a) Find bases for $Im(T)$ and $ker(T)$, and find the dimension of each.
Let $T: \mathbb{R}^3 \to \mathbb{R}^4$
$$
T\begin{pmatrix}x_1\\x_2\\x_3\end{pmatrix}=\begin{pmatrix}x_1+5x_2\\2x_1+10x_2\\x_3\\6x_3\end{pmatrix}=(x_1+5x_2)\begin{pmatrix}1\\2\\0\\0\end{pmatrix}+x_3\begin{pmatrix}0\\0\\1\\6\end{pmatrix}
$$
A basis for $Im(T)$ is $\begin{Bmatrix}\begin{pmatrix}1\\2\\0\\0\end{pmatrix},\begin{pmatrix}0\\0\\1\\6\end{pmatrix}\end{Bmatrix}$. They're linearly independent so they form a basis for $Im(T)$.

$$
\begin{equation}
\begin{split}
Im(T)&=\begin{Bmatrix}\begin{pmatrix}a\\2a\\b\\6b\end{pmatrix}:a,b\in\mathbb{R}\end{Bmatrix}\\
&=span(\begin{pmatrix}1\\2\\0\\0\end{pmatrix}, \begin{pmatrix}0\\0\\1\\6\end{pmatrix})\\
\\
dim(Im(T))&=2
\end{split}
\end{equation}
$$
AND

A basis for $ker(T)$ is $\begin{Bmatrix}\begin{pmatrix}-5\\1\\0\end{pmatrix}\end{Bmatrix}$ by:
$$
\begin{equation}
\begin{split}
x_1+5x_2&=0\\
x_1&=-5x_2\\
\\
2x_1+10x_2&=0 & \text{satisfied by above}\\
\\
x_3&=0\\
\\
6x_3&=0 & \text{satisfied by above}
\end{split}
\end{equation}
$$
Setting $x_2 = a$ (free param.)
$$
\begin{equation}
\begin{split}
ker(T)&=\begin{Bmatrix}a\begin{pmatrix}-5\\1\\0\end{pmatrix}:a\in\mathbb{R}\end{Bmatrix}\\
&=span(\begin{pmatrix}-5\\1\\0\end{pmatrix})\\
\\
dim(ker(T))&=1
\end{split}
\end{equation}
$$

---

### (b) Let $V$ be the vector space of functions from $\mathbb{N}$ to $\mathbb{R}$, and let $L : V →\mathbb{R}$ denote the linear map $L(f ) = f (2)−f (1)$.

1. Describe the image of $L$.

The image of $L$ is the set of all outputs of $L$. 

$$
Im(L)=\{L(f) | f \in V\}=\{f(2)-f(1):f \in V\}
$$
Essentially, since $L$'s variable is a function itself, we can manipulate $f$ and observe how that affects $L$.

$f(2)-f(1)$ is defined everywhere that $f(2)$ and $f(1)$ are defined.

Let $y\in \mathbb{R}$. We want to show that for any arbitrary $y$, there exists an $f$ in $V$ such that $f(2)-f(1)=y$. If we can do this, the image is $\mathbb{R}$.

In class we learned about a delta function that is zero everywhere but one at a number: $\delta_n$. This inspired me to find:
$$
f_y(n)=\begin{Bmatrix}n\neq2:0\\n=2:y\end{Bmatrix}
$$
or
$$
(\delta_2)*(y) \in V
$$

hence, since $L(\delta_2y)=y$ for an arbitrary $y \in \mathbb{R}$, then the image of $L$ is $\mathbb{R}$.

2. (ii) Find, with proof, four linearly independent elements of $ker(L)$.

The kernel of $L$ are inputs to $L$ who produce outputs of 0.
In essence, what $f$ exist such that $f(2)-f(1)=0$

I'll use my idea of the delta functions from earlier:

| #   | function       |
| --- | -------------- |
| 1   | $\delta_{100}$ |
| 2   | $\delta_{101}$ |
| 3   | $\delta_{102}$ |
| 4   | $\delta_{103}$ |
These functions are all in $V$ and are zero everywhere but their respective numbers. For example, $$\delta_{100}(2)-\delta_{100}(1)=0-0=0$$
...And so on.

Proof: 
1. Let $S=\{\delta_{100},\delta_{101},\delta_{102},\delta_{103}\}$
2. WTS $S$ is linearly independent, ie given $c_1,c_2,c_3,c_4 \in \mathbb{R}$, $$c_1\delta_{100}(n)+c_2\delta_{101}(n)+c_3\delta_{102}(n)+c_4\delta_{103}(n)=0 $$we'd WTS $c_1=c_2=c_3=c_4=0, \forall n \in \mathbb{N}$
3. Let $n=100$: $c_1*1+c_2*0+c_3*0+c_4*0=0\implies c_1=0$
4. Let $n=101$: $c_2=0$
5. Let $n=102$: $c_3=0$
6. Let $n=103$: $c_4=0$
7. Since $c_1=c_2=c_3=c_4=0$ is the only solution, $S$ must be linearly independent $\blacksquare$

---

## Problem 4

_Armen and Bianca play a game in which they take turns filling out entries of an initially empty $100×100$ array. Armen plays first. At each turn, a player chooses a real number and places it in a vacant entry. The game ends when all the entries are filled. Armen wins if the columns of the resulting matrix are a basis for $\mathbb{R}^{100}$; Bianca wins otherwise. Which player has a winning strategy?_

Armen will win if the columns of the matrix are a basis for $\mathbb{R}^{100}$. This means that every column must be linearly independent.

Bianca will win if any column fails this test. So, she should try to make two columns fail linear independence. She can pick column 1 and column 2.

When Armen places a number in Column 1, Bianca should copy that number into Column 2.
When Armen places a number in Column 2, Bianca should copy that number into Column 1.

Throughout the progression of the game, Bianca will ensure that Column 1 and Column 2 have duplicate values. 

By the end of the game, Column 1 will be identical to Column 2.

Examine this scenario:
$$
\begin{equation}
\begin{split}
c_1\begin{pmatrix}1\\2\\...\\100\end{pmatrix}+c_2\begin{pmatrix}1\\2\\...\\100\end{pmatrix}+c_3\begin{pmatrix}-1\\267\\...\\70\end{pmatrix}+...=0
\end{split}
\end{equation}
$$
If $c_1 = 1$ and $c_2 = -1$, then not every $c$ must be zero in order to ensure LHS = 0

Therefore, the matrix's columns are linearly dependent. That means they cannot form a basis!!!!
$\blacksquare$.

Bianca will always win.