## Problem 1
### (a) Express $f$, $g$, and $g \circ f$ in set-builder notation as subsets of $A \times B$, $B \times C$, and $A \times C$ respectively.

$$
\begin{equation}
\begin{split}
f&=\lbrace (a, b) | (a, b)\in A\times B, b=f(a)\rbrace \subseteq A \times B  \\
g&=\lbrace (b, c) | (b, c)\in B\times C, c=g(b)\rbrace \subseteq B \times C \\
(g \circ f)&=\lbrace (a, c) | (a, b) \in A\times C,c=(g\circ f)(a)\rbrace \subseteq A\times C
\end{split}
\end{equation}
$$
### (b) Give an example of a subset of the set {□, △}×{□, △}which is not a function.
$$
\begin{equation}
\begin{split}
\lbrace\square,\triangle\rbrace\times\lbrace\square,\triangle\rbrace &= \lbrace (\square, \square), (\square,\triangle),(\triangle,\square),(\triangle,\triangle)\rbrace \\ 
\\
\lbrace(\square, \square), (\square, \triangle)\rbrace & \subset\lbrace\square,\triangle\rbrace\times\lbrace\square,\triangle\rbrace
\end{split}
\end{equation}
$$

$\lbrace(\square, \square), (\square, \triangle)\rbrace$ is a subset of the set $\lbrace\square, \triangle\rbrace\times\lbrace\square, \triangle\rbrace$. It is not a well-defined function because there exists an input shape ($\square$) that provides two outputs ($\square, \triangle$).

### (c) If $f$ and $g$ are injective, show $g\circ f$ is injective.

1. Suppose:
$$
\begin{equation}
\begin{split}
g(f(a_1))&=g(f(a_2))
\end{split}
\end{equation}
$$
2. We want to show:
$$
a_1 = a_2
$$
3. Given $g: B \to C$ is injective, by definition,
$$
\begin{equation}
\begin{split}
        g(b_1)&=g(b_2)& \quad\forall b_1,b_2 \in B\\
\implies \quad b_1 &=b_2  \\
\end{split}
\end{equation}
$$
4. So,
$$
\begin{equation}
\begin{split}
g(f(a_1))&=g(f(a_2))\\
\implies \quad f(a_1)&=f(a_2)
\end{split}
\end{equation}
$$
5. Given $f: A\to B$ is injective, by definition,
$$
\begin{equation}
\begin{split}
        f(a_1)&=f(a_2)& \quad\forall a_1,a_2 \in A\\
\implies \quad a_1 &=a_2  \\
\end{split}
\end{equation}
$$
6. Hence, $g \circ f$ is injective $\blacksquare$

### (d) If $f$ and $g$ are surjective, show $g\circ f$ is surjective.

1. Let $c \in C$
2. Given $g: B\to C$ is surjective, by definition,
$$
\exists b \in B : g(b)=c
$$
3. Given $f: A \to B$ is surjective, by definition,
$$
\exists a\in A : f(a)=b
$$
4. So,
$$
g(f(a)) = g(b)=c
$$
5. Which implies
$$
\forall c \in C,\exists a \in A : (g \circ f)(a) =c
$$
6. So, $g \circ f$ is surjective $\blacksquare$

---
## Problem 2

### (a) Suppose there is a function $g : B \to A$ such that for all $a \in A, g(f (a)) = a$. Prove $f$ is injective.

1. Let $a_1, a_2 \in A$.
2. Suppose: 
$$
\begin{equation}
\begin{split}
f(a_1)&=f(a_2)
\end{split}
\end{equation}
$$
3. Then, apply $g$ to both sides.
$$
\begin{equation}
\begin{split}
g(f(a_1))&=g(f(a_2)) \\
a_1 &= a_2
\end{split}
\end{equation}
$$
4. Hence, by the definition of an injective function, $f$ is injective $\blacksquare$.

### (b) Suppose there is a function $h : B →A$ such that for all $b ∈B, f (h(b)) = b$. Prove $f$ is surjective.

1. We want to show $$\forall b \in B, \exists a \in A : f(a)=b$$
2. Let $a=h(b):b \in B, h(b) \in A$
3. So,
$$
\begin{equation}
\begin{split}
\forall b \in B, f(h(b))&=b \\
\implies \quad \forall b \in B, \exists a\in A : f(a) &= b
\end{split}
\end{equation}
$$
4. Hence, by the definition of a surjective function, $f$ is surjective $\blacksquare$.

### (c) Suppose there is a function $φ : B →A$ such that for all $a ∈A$ we have $φ(f (a)) = a$ and for all $b ∈B$ we have $f (φ(b)) = b$. Prove that $f$ is bijective.

1. We want to show that:
	a) $f(a_1)=f(a_2) \implies a_1 = a_2 : a_1, a_2 \in A$
	b) $\forall b \in B, \exists a \in A : f(a)=b$
2. Is $f$ surjective test
	1. Let $a = φ(b): b \in B, φ(b)\in A$
	2. So, given: $$\begin{equation}
\begin{split}
\forall b \in B, f(φ(b))&=b \\
\forall b \in B, f(a)&= b
\end{split}
\end{equation}$$
	3. We can imply: $$	\implies \quad \forall b \in B, \exists a \in A:f(a) = b$$
	4. Hence, by the definition of a surjective function, $f$ is surjective.
3. Is $f$ injective test
	1.  Let $a_1, a_2 \in A$.
	2. Suppose: 
$$
\begin{equation}
\begin{split}
f(a_1)&=f(a_2)
\end{split}
\end{equation}
$$
	3. Then, apply $φ$ to both sides.
$$
\begin{equation}
\begin{split}
φ(f(a_1))&=φ(f(a_2)) \\
a_1 &= a_2
\end{split}
\end{equation}
$$
	4. Hence, by the definition of an injective function, $f$ is injective.
4. Hence, since $f$ is both injective and surjective, it is bijective  $\blacksquare$
---
## Problem 3
### (a) Let $E= \lbrace f ∈F : ∀x ∈ \mathbb{R}, f (x) = f (−x)\rbrace$ denote the set of even functions. Prove $E$ is a subspace of $F$.

We want to show $E \le F$. By the definition of a subspace, $E$ must contain zero and be closed under addition and scalar multiplication. So, we prove each condition.
#### Proof: $0\in E$.
1. Let $z(x)=0$. We want to show $z \in E$
2. Then, $z(x)=z(-x)$ must hold true $\forall x \in \mathbb{R}$
3. $0=0 \implies z(x)=z(-x) \implies z \in E$
#### Proof: $E$ is closed under addition
1. Let $a \in E, b \in E$
2. Let $(a + b)(x) = a(x) + b(x) : \forall x \in \mathbb{R}$
3. Let $s(x) = (a+b)(x)$
4. We want to show $s \in E$ 
5. Then, $s(x)=s(-x)$ must hold true $\forall x \in \mathbb{R}$
6. Then, the following must hold: $$
\begin{equation}\begin{split}s(x)&=s(-x)\\(a+b)(x)&=(a+b)(-x)\\a(x)+b(x)&=a(-x)+b(-x) \\\end{split} \end{equation} $$
7. Given $a(x)=a(-x)$ and $b(x)=b(-x)$, substitute:$$a(x)+b(x)=a(x)+b(x)$$
8. Hence, $s \in E \implies E$ is closed under addition
#### Proof: $E$ is closed under scalar multiplication
1. Let $a \in E$, $k\in F$
2. Let $m(x) = ka(x)$
3. We want to show $m \in E$
4. Then, $m(x)=m(-x)$ must hold true $\forall x \in \mathbb{R}$
5. Then, the following must hold: $$\begin{equation}\begin{split}m(x)&=m(-x) \\ka(x)&=ka(-x) \\a(x)&=a(-x)\end{split}\end{equation}$$
6. $a(x)=a(-x)$ holds because $a\in E$.
7. Hence, $m\in E \implies E$ is closed under scalar multiplication

#### Big Proof
1. Since $0\in{E}$, and $E$ is closed under addition and scalar multiplication, $E$ is a subspace of $F$. $\blacksquare$

### (b) Let $D= \lbrace f ∈F : ∀x ∈R, f (x) =−f (−x)\rbrace$ denote the set of odd functions. Prove $D$ is a subspace of $F$.

We want to show $D \le F$. By the definition of a subspace, $D$ must contain zero and be closed under addition and scalar multiplication. So, we prove each condition.

#### Proof: $0\in D$.
1. Let $z(x)=0$. We want to show $z \in D$
2. Then, $z(x)=-z(-x)$ must hold true $\forall x \in \mathbb{R}$
3. $0=0 \implies z(x)=-z(-x) \implies z \in D$
#### Proof: $D$ is closed under addition
1. Let $a \in D, b \in D$
2. Let $(a + b)(x) = a(x) + b(x) : \forall x \in \mathbb{R}$
3. Let $s(x) = (a+b)(x)$
4. We want to show $s \in D$ 
5. Then, $s(x)=-s(-x)$ must hold true $\forall x \in \mathbb{R}$
6. Then, the following must hold: $$
\begin{equation}\begin{split}s(x)&=-s(-x)\\(a+b)(x)&=-(a+b)(-x)\\a(x)+b(x)&=-a(-x)-b(-x) \\\end{split} \end{equation} $$
7. Given $a(x)=-a(-x)$ and $b(x)=-b(-x)$, substitute:$$a(x)+b(x)=a(x)+b(x)$$
8. Hence, $s \in D \implies D$ is closed under addition

#### Proof: $D$ is closed under scalar multiplication
1. Let $a \in D$, $k\in F$
2. Let $m(x) = ka(x)$
3. We want to show $m \in D$
4. Then, $m(x)=-m(-x)$ must hold true $\forall x \in \mathbb{R}$
5. Then, the following must hold: $$\begin{equation}\begin{split}m(x)&=-m(-x) \\ka(x)&=-ka(-x) \\a(x)&=-a(-x)\end{split}\end{equation}$$
6. $a(x)=-a(-x)$ holds because $a\in D$.
7. Hence, $m\in D \implies D$ is closed under scalar multiplication

#### Big proof
1. Since $0 \in{D}$ and $D$ is closed under addition and scalar multiplication, $D$ is a subspace of $F$. $\blacksquare$

### (c) Prove there is only one function in the set $E\cap D$.
1. Let $u \in (E \cap D)$
2. If $u\in (E\cap D)$, then $u \in E$, and $u(x)=u(-x) : \forall x \in \mathbb{R}$
3. If $u\in (E\cap D)$, then $u \in D$, and $u(x)=-u(-x) : \forall x \in \mathbb{R}$
4. Then, from steps 2 and 3 we have $u(-x)=u(x)=-u(-x)$.
5. Then, $$\begin{equation}\begin{split}u(-x) &=-u(-x)\\2u(-x)&=0\\u(-x)&=0\end{split}\end{equation}$$
6. Since $u(-x) = 0 :\forall x \in \mathbb{R}$, then $u(x)=0 : \forall x \in \mathbb{R}$. 
7. Since $E$ and $D$ are subspaces, $0\in E$ and $0 \in D$, so $0 \in E \cap D$.
8. $(E \cap D)=\lbrace 0\rbrace$ $\quad\blacksquare$

## Problem 4
### (a) Prove that the intersection $U \cap W$ is a subspace of $V$.

We want to show $(U \cap W) \le V$. By the definition of a subspace, $(U \cap W)$ must contain zero and be closed under addition and scalar multiplication. So, we prove each condition.
#### Proof: $0\in (U \cap W)$
1. Given $U \le V$ and $W \le V$, $0 \in U$ and $0 \in W$ by property (i).
2. Hence, $0 \in U \cap W$
#### Proof: $(U \cap W)$ is closed under addition
1. Let $a, b \in (U \cap W)$
2. If $a \in U \cap W$, then $a \in U$ and $a \in W$
3. If $b \in U \cap W$, then $b \in U$ and $b \in W$
4. Because $U$ and $W$ are subspaces, they are closed under addition:$$\begin{equation}\begin{split}a+b&\in U\\a+b&\in W\end{split}\end{equation}$$
5. Because $a+b$ is in $U$ and $W$, $a+b \in (U \cap W)$
6. Hence, $U \cap W$ is closed under addition

#### Proof: $(U \cap W)$ is closed under scalar multiplication
1. Let $k \in F, a \in (U \cap W)$. 
2. If $a \in U \cap W$, then $a \in U$ and $a \in W$
3. Because $U$ and $W$ are subspaces, they are closed under scalar multiplication:$$\begin{equation}\begin{split}ka&\in U\\ka&\in W\end{split}\end{equation}$$
4. Because $ka$ is in $U$ and $W$, $ka \in (U \cap W)$
5. Hence, $U \cap W$ is closed under scalar multiplication.
#### Big Proof
1. Since $0 \in{U \cap W}$ and $U \cap W$ is closed under addition and scalar multiplication, $U \cap W$ is a subspace of $V$. $\blacksquare$

### (b) Define $U + W= \lbrace{u + w : u ∈U, w ∈W }\rbrace$. Prove $U + W ≤V$.

We want to show $(U + W) \le V$. By the definition of a subspace, $(U + W)$ must contain zero and be closed under addition and scalar multiplication. So, we prove each condition.
#### Proof: $0\in (U + W)$
1. Given $U \le V$ and $W \le V$, $0 \in U$ and $0 \in W$ by property (i).
2. Hence, $\exists u \in U, \exists w \in W : u + w = 0$ because $0+0=0$.
3. Hence, $0 \in U + W$
#### Proof: $(U + W)$ is closed under addition
1. Let $a, b \in (U + W)$
2. Then, $a=u_1+w_1$ and $b=u_2+w_2$ for $u_1, u_2 \in U$ and $w_1, w_2 \in W$
3. $a+b = (u_1+u_2)+(w_1+w_2)$
4. Because $U$ and $W$ are subspaces, they are closed under addition:$$\begin{equation}\begin{split}u_1+u_2&\in U\\w_1+w_2&\in W\end{split}\end{equation}$$
5. Because $u_1 + u_2$ is in $U$ and $w_1 + w_2$ is in $W$, $a+b \in (U + W)$
6. Hence, $U + W$ is closed under addition

#### Proof: $(U + W)$ is closed under scalar multiplication
1. Let $k \in F, a \in (U + W)$. 
2. Then, $a=u_1+w_1$ for $u_1 \in U$ and $w_1 \in W$
3. $ka = (ku_1)+(kw_1)$
4. Because $U$ and $W$ are subspaces, they are closed under scalar multiplication:$$\begin{equation}\begin{split}ku_1&\in U\\kw_1&\in W\end{split}\end{equation}$$
5. Because $ku_1$ is in $U$ and $kw_1$ is in $W$, $ka \in (U + W)$
6. Hence, $U + W$ is closed under scalar multiplication
#### Big Proof
1. Since $0 \in{U + W}$ and $U + W$ is closed under addition and scalar multiplication, $U + W$ is a subspace of $V$. $\blacksquare$

### (c) Find (with proof) two subspaces of $\mathbb{R}^2$ whose union is not a subspace of $\mathbb{R}^2$
1. Let $A$ = "the x axis" and $B$ = "the Y axis"
$$
\begin{equation}
\begin{split}
A&= \lbrace{(x, 0) : x \in \mathbb{R}}\rbrace \\
B&= \lbrace{(0, y) : y \in \mathbb{R}}\rbrace
\end{split}
\end{equation}
$$
2. The x-axis is a subspace of $\mathbb{R}^2$
	1. Zero: $(0, 0) \in A$
	2. Closed under addition:
		1. Let $A_1 = (a, 0)$ and $A_2 = (b, 0)$ $: a,b \in \mathbb{R}$
		2. $A_1+A_2 = (a+b, 0)$
		3. Addition is closed under $\mathbb{R}$; hence $a+b \in \mathbb{R}$ 
		4. Hence, ($A_1 + A_2) \in A$
		5. Hence, $A$ is closed under addition
	3. Closed under scalar multiplication
		1. Because $\mathbb{R}$ is closed under multiplication, for any $k∈\mathbb{R}$ and $(a,0)∈A$, $k(a,0)=(ka,0)$
		2. Hence, $ka \in \mathbb{R}$
		3. Hence, $A$ is closed under scalar multiplication
	4. Thus $A$ is subspace of $\mathbb{R}^2$ because it satisfies properties (i), (ii), and (iii).
3. The y-axis is a subspace of $\mathbb{R}^2$
	1. Zero: $(0, 0) \in B$
	2. Closed under addition:
		1. Let $B_1 = (0, a)$ and $B_2 = (0, b)$ $: a,b \in \mathbb{R}$
		2. $B_1+B_2 = (0, a+b)$
		3. Addition is closed under $\mathbb{R}$; hence $a+b \in \mathbb{R}$ 
		4. Hence, ($B_1 + B_2) \in B$
		5. Hence, $B$ is closed under addition
	3. Closed under scalar multiplication
		1. Because $\mathbb{R}$ is closed under multiplication, for any $k∈\mathbb{R}$ and $(0, a)∈B$, $k(0,a)=(0, ka)$
		2. Hence, $ka \in \mathbb{R}$
		3. Hence, $B$ is closed under scalar multiplication
	4. Thus $B$ is subspace of $\mathbb{R}^2$ because it satisfies properties (i), (ii), and (iii).
#### Now we prove that $A∪B$ is not a subspace of $\mathbb{R}^2$
1. We go by contradiction.
2. Suppose that $A\cup B$ is a subspace of $\mathbb{R}^2$
3. Consider $a=(1, 0) \in A$ and $b=(0, 1) \in B$. 
4. $(1, 0) \in A∪B$
5. $(0, 1) \in A∪B$
6. $a+b = (1,1)$
7. However, $(1, 1)$ is not included in $A$ and $(1,1)$ is not included in $B$
8. Thus, $A∪B$ is not closed under addition and hence not a subspace of $\mathbb{R}^2$ $■$


