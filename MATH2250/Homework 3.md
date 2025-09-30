## Problem 1
---
### (a)  Suppose $T_1 : U \to V$ and $T_2 : V \to W$ are linear transformations. Prove that $T_2 \circ T_1$ is a linear transformation.

1. Let $a, b \in U, c \in \mathbb{F}$.
2. We want to show $T_2(T_1(a + b)) = T_2(T_1(a))+T_2(T_1(b))$
	1. Given $T_1$ is a linear transformation, $T_1(a+b)=T_1(a)+T_1(b)$
	2. Given $T_2$ is a linear transformation, $$\begin{equation}\begin{split}T_2(T_1(a+b))=T_2(T_1(a)+T_1(b))&=T_2(T_1(a))+T_2(T_1(b))\end{split}\end{equation}$$
	3. Hence, $$(T_2\circ T_1)(a+b)=(T_2 \circ T_1)(a)+(T_2\circ T_1)(b)$$
3. We want to show $T_2(T_1(ca))=cT_2(T_1(a))$
	1. Given $T_1$ is a linear transformation, $T_1(ca)=cT_1(a)$
	2. Given $T_2$ is a linear transformation, $$\begin{equation}\begin{split}T_2(T_1(ca))=T_2(cT_1(a))&=cT_2(T_1(a))\end{split}\end{equation}$$
	3. Hence, $$(T_2 \circ T_1)(ca)=c(T_2 \circ T_1)(a)$$
4. Hence, since a linear transformation is a function between vector spaces that preserves vector addition and scalar multiplication, and we've shown $T_2\circ T_1$ does just that, then $T_2 \circ T_1$ is a linear transformation. $\blacksquare$
---
### (b) Suppose $f : U →V$ is a linear bijection, and let $g : V →U$ be its inverse (i.e. $f (g(v)) = v$ for all $v ∈V$ and $g(f (u)) = u$ for all $u ∈U$). Prove that $g$ must be linear as well.

1. $f$ is bijective. That means it is both injective and surjective.
2. We want to show that for any $v_1, v_2 \in V, g(v_1 + v_2)= g(v_1) + g(v_2)$
	1. Call $f$ on $g(v_1+v_2)$ $$\begin{equation}\begin{split}f(g(v_1 + v_2))&=v_1 + v_2&\quad\text{because f is g's inverse}\end{split}\end{equation}$$
	2. Aside: Because $v=f(g(v))$ for all $v$, $$v_1+v_2=f(g(v_1))+f(g(v_2))$$
	3. Set these 2.1 and 2.2 expressions for $v_1+v_2$ equal:$$f(g(v_1+v_2))=f(g(v_1))+f(g(v_2))$$ 
	4. Since $f$ is linear, $$f(g(v_1+v_2))=f(g(v_1)+g(v_2))$$
	5. We know $f$ is injective which means $f(u_1)=f(u_2)\implies u_1=u_2$.
	6. Thus,$$g(v_1+v_2)=g(v_1)+g(v_2)$$
3. We want to show that for any $c\in \mathbb{F},v\in V, g(cv)=cg(v)$
	1. Given $f$ is linear, $$f(cu)=cf(u)$$
	2. Then,$$f(cg(v))=cf(g(v))=cv$$
	3. Call $g$ on both sides, hence $$\begin{equation}\begin{split}g(f(cg(v)))=g(cv)\\cg(v)=g(cv)\end{split}\end{equation}$$
4. Hence, since a linear transformation is a function between vector spaces that preserves vector addition and scalar multiplication, and we've shown $g$ does just that, then $g$ is a linear transformation. $\blacksquare$
---
## Problem 2
Let $U$ and $V$ be vector spaces over a field $\mathbb{F}$ and let $T1, T2 : U →V$ be linear. Suppose $S= \lbrace u_1, u_2, . . . , u_k\rbrace⊆U$ and that for all $s ∈S$ we have $T_1(s) = T_2(s)$. Prove that for all $x ∈span(S)$ we have $T_1(x) = T_2(x)$.

1. We want to show $\forall x \in span(S), T_1(x)=T_2(x)$
2. Let $x\in span(S)$
3. There must exist some $c_1, c_2, ..., c_k \in \mathbb{F}$ such that  $x =  c_1u_1+c_2u_2+...+c_ku_k$ by the definition of what it means to span (algebraically)
4. Hence, since we know $T_1$ and $T_2$ are linear transformations, we can apply the property of additivity and homogeneity to them as follows: $$\begin{equation}\begin{split}T_1(x)&=T_1(c_1u_1+c_2u_2+...+c_ku_k)\\&=T_1(c_1u_1)+T_1(c_2u_2)+...+T_1(c_ku_k)\\&=c_1T_1(u_1)+c_2T_1(u_2)+...+c_kT_1(u_k)\\\\T_2(x)&=T_2(c_1u_1+c_2u_2+...+c_ku_k)\\&=T_2(c_1u_1)+T_2(c_2u_2)+...+T_2(c_ku_k)\\&=c_1T_2(u_1)+c_2T_2(u_2)+...+c_kT_2(u_k)\end{split}\end{equation}$$
5. We are given $T_1(s)=T_2(s)$ for all $s\in \lbrace u_1, u_2, . . . , u_k\rbrace⊆U$
6. Hence, since $c_iT_1(u_i)=c_iT_2(u_i)$ for $i=1,...,k$ as we can multiply both sides by the common coefficient $c_i$ which implies, $$c_1T_1(u_1)+c_2T_1(u_2)+...+c_kT_1(u_k)=c_1T_2(u_1)+c_2T_2(u_2)+...+c_kT_2(u_k)$$
7. We then know $T_1(x)=T_2(x)$ $\blacksquare$
---
## Problem 3
Let $U$ and $V$ be vector spaces over a field $\mathbb{F}$ and let $T : U → V$ be linear. Let $S= \lbrace{u_1, u_2, . . . , u_k\rbrace}⊆U$, and define $T(S) = \lbrace{T (u) : u ∈S}\rbrace$.

---
### (a) If $S$ spans $U$ , prove that $T(S)$ spans the image of $T$.

1. We want to show $Im(T)=span(T(S))$
2. We know $Im(T)=\lbrace{T(u): u \in U}\rbrace$
3. Let $v \in Im(T)$. There exists an $x\in U$ such that some $v=T(x)$
4. Since $S$ spans $U$, the algebraic definition of spanning means for some $c_1, c_2, ..., c_k \in \mathbb{F}$, $x=c_1u_1+c_2u_2+...+c_ku_k$ 
5. Hence, by the additivity and homogeneity of $T$ since it is linear, $$\begin{equation}\begin{split}v&=T(x)\\&=T(c_1u_1+c_2u_2+...+c_ku_k)\\&=T(c_1u_1)+T(c_2u_2)+...+T(c_ku_k)\\&=c_1T(u_1)+c_2T(u_2)+...+c_kT(u_k)\end{split}\end{equation}$$
6. Hence, $v$ is a linear combination of $\lbrace T(u_1), T(u_2), ..., T(u_k) \rbrace$
7. That means $v\in span(T(S)) \implies Im(T) \subseteq span(T(S))$
8. Now, we want to show $span(T(S)) \subseteq Im(T)$ to force equality
9. Let some $w\in span(T(S))$
10. $w$ can be re-written as,  for $a_1 ... a_k \in \mathbb{F}$, by using the additivity and homogeneity of $T$.$$\begin{equation}\begin{split}w&=a_1T(u_1)+a_2T(u_2)+...+a_kT(u_k)\\&=T(a_1u_1)+T(a_2u_2)+...+T(a_ku_k)\\&=T(a_1u_1+a_2u_2+...+a_ku_k)\end{split}\end{equation}$$
11. Let $u=a_1u_1+a_2u_2+...+a_ku_k \in U$ and $w = T(u) \implies w \in Im(T)$
12. That means $span(T(S)) \subseteq Im(T)$ because we generalized $w$.
13. Since $Im(T) \subseteq span(T(S))$ and $span(T(S)) \subseteq Im(T)$, we conclude $Im(T) = span(T(S))$ $\blacksquare$

---
### (b) If $T(S)$ is linearly independent, prove that $S$ must be linearly independent.
1. We want to show $S=\lbrace u_1, u_2, ..., u_k \rbrace$ is linearly independent.
2. This means that for $c_1, ..., c_k \in \mathbb{F}$, if $c_1u_1+c_2u_2+...+c_ku_k=0$, then all $c_i$ = 0.
3. Suppose $c_1u_1+c_2u_2+...+c_ku_k=0$.
4. Call $T$ on LHS and RHS: $$T(c_1u_1+c_2u_2+...+c_ku_k)=T(0)$$
5. $T(0) = 0$. Also, $T$ is is linear, so we can apply additivity and homogeneity: $$\begin{equation}\begin{split}T(c_1u_1+c_2u_2+...+c_ku_k)&=0\\T(c_1u_1)+T(c_2u_2)+...+T(c_ku_k)&=0\\c_1T(u_1)+c_2T(u_2)+...+c_kT(u_k)&=0\end{split}\end{equation}$$
6. And we know that $T(S)$ is linearly independent, so every coefficient $c_1, ..., c_k$ must be zero.
7. Hence we've satisfied step 2 and shown $S$ is linearly independent $\blacksquare$

---
### (c) Find (with proof) a linear function $T : \mathbb{R}^2 →\mathbb{R}$ and a set $S ⊆\mathbb{R}^2$ such that $T(S)$ spans $Im(T)$ but $S$ does not span $\mathbb{R}^2$.
1. Let $T(x,y)=x$. $T$ satisfies $\mathbb{R}^2\to\mathbb{R}$.
2. Is $T$ linear?
	1. Let $x_1, x_2, y_1, y_2, c \in \mathbb{R}$
	2. Additivity is true $$\begin{equation}\begin{split}T((x_1, y_1) +(x_2,y_2))&=T(x_1,y_1)+T(x_2,y_2)\\T(x_1+x_2,y_1+y_2)&=T(x_1,y_1)+T(x_2,y_2)\\x_1+x_2&=x_1+x_2\end{split}\end{equation}$$
	3. Homogeneity is true $$\begin{equation}\begin{split}T(cx_1,cy_1)&=cT(x_1,y_1)\\cx_1&=cx_1\end{split}\end{equation}$$
	4. Hence, $T$ is linear.
3. $\forall r \in \mathbb{R}, T(r, 0)=r \implies Im(T) = \mathbb{R}$ because every real number is in the image
4. Let $S=\lbrace (x,0) : x \in \mathbb{R}\rbrace$. $S \subseteq \mathbb{R}^2$ 
5. $T(S)={T(x,0):x∈\mathbb{R}}={x:x∈\mathbb{R}}=\mathbb{R}$
6. $T(S) = \mathbb{R}\implies T(S)$ spans $Im(T)$
7. $S$ can be thought of as the x axis, but the x axis does not span $\mathbb{R}^2$ because every y-coordinate in $S=0$. So vectors like $(1, 1)$ in $\mathbb{R}^2$ cannot be expressed by linear combinations in $S$.
8. Hence, we're done. $\blacksquare$

---
## (d) Find (with proof) a linear function $T : \mathbb{R}^2 → \mathbb{R}^2$ and a set $S ⊆\mathbb{R}^2$ such that $S$ is linearly independent, but $T (S)$ is not.
1. Let $T(x,y)=(x,0)$. $T$ satisfies $\mathbb{R}^2\to\mathbb{R}^2$.
2. Is $T$ linear?
	1. Let $x_1, x_2, y_1, y_2, c \in \mathbb{R}$
	2. Additivity is true $$\begin{equation}\begin{split}T((x_1, y_1) +(x_2,y_2))&=T(x_1,y_1)+T(x_2,y_2)\\T(x_1+x_2,y_1+y_2)&=T(x_1,y_1)+T(x_2,y_2)\\(x_1+x_2,0)&=(x_1+x_2,0)\end{split}\end{equation}$$
	3. Homogeneity is true $$\begin{equation}\begin{split}T(cx_1,cy_1)&=cT(x_1,y_1)\\(cx_1,0)&=(cx_1, 0)\end{split}\end{equation}$$
	4. Hence, $T$ is linear.
3. Let $S=\lbrace(1,0), (0,1)\rbrace$. $S \subseteq \mathbb{R}^2$ 
4. Is $S$ linearly independent?
	1. For $v_i \in S$, we expect every coefficient $c_i=0$ when we get a linear combination $(0,0)$:$$c_1v_1+c_2v_2=(0,0)$$
	2. If $c_1(1, 0)+c_2(0, 1)=(0,0)$, then $(c_1, c_2)=(0,0)$
	3. $\implies c_1 = c_2 =0$ 
	4. Hence $S$ is linearly independent
5. Is $T(S)$ linearly independent?
	1. $T(S)=\lbrace(1, 0), (0, 0)\rbrace$
	2. For $v_i \in T(S)$, we expect every coefficient $c_i=0$ when we get a linear combination $(0,0)$:$$c_1v_1+c_2v_2=(0,0)$$
	3. If $c_1(1, 0)+c_2(0,0)=(0,0)$, then $(c_1, 0)=(0,0)$
	4. BUT look. $c_2$ can be any nonzero number and the equality will still hold. This violates the definition of linear independence.
	5. So, $T(S)$ is not linearly independent
6. Hence, we're done. $\blacksquare$

---
### (e) If $T$ is injective and $S$ is linearly independent, prove $T(S)$ is linearly independent.

1. We want to show that $T(S)$ is linearly independent
2. Let unique $u_1, u_2, ..., u_k \in S$ and Let $c_1, c_2, ..., c_k \in \mathbb{F}$
3. Suppose we have some a linear combination of vectors in $T(S)$ such that $c_1T(u_1)+c_2T(u_2)+...+c_kT(u_k)=0$
4. Because $T$ is linear, we can use its additive and homogeneity properties: $$\begin{equation}\begin{split}0&=c_1T(u_1)+c_2T(u_2)+...+c_kT(u_k)\\&=T(c_1u_1)+T(c_2u_2)+...+T(c_ku_k)\\&=T(c_1u_1+c_2u_2+...+c_ku_k)\end{split}\end{equation}$$
5. We know $T(0)=0$, so $$T(0)=T(c_1u_1+c_2u_2+...+c_ku_k)$$
6. If $T$ is injective, then we know,$$0=c_1u_1+c_2u_2+...+c_ku_k$$
7. But we know $S$ is linearly independent. So, $c_1, ..., c_k$ must all = zero.
8. Hence, $T(S)$ is linearly independent $\blacksquare$

----
## Problem 4
Let $V$ be a vector space over $F$ and $S= \lbrace{v_1, . . . , v_k}\rbrace⊆V$.

---
### (a) For every $x∈V$, prove that $x∈span(S)$ iff $span(S) = span(S ∪\lbrace{x\rbrace})$.
1. Suppose $x\in span(S)$
2. We want to show $span(S)=span(S\cup\lbrace{x}\rbrace)$
3. $S \subseteq S\cup\lbrace{x}\rbrace \implies span(S) \subseteq span(S\cup\lbrace{x}\rbrace)$
4. Let $y \in span(S\cup \{x\})$.
5. Hence, $y= c_1v_1+c_2v_2+...+c_kv_k+bx$ where $c_i, b \in \mathbb{F}$.
6. Since $x \in span(S)$, Let $x=a_1v_1+a_2v_2+...+a_kv_k$ where $a_i\in\mathbb{F}$.
7. Hence,$$\begin{equation}\begin{split}y &= c_1v_1+c_2v_2+...+c_kv_k+b(a_1v_1+a_2v_2+...+a_kv_k)\\&= v_1(c_1+ba_1)+...+v_k(c_k+ba_k)\end{split}\end{equation}$$


8. Hence, every element of $span(S∪{x})$ is a linear combination of elements in $S$
9. Hence, $span(S \cup \lbrace x \rbrace) \subseteq span(S)$
10. Hence, since $span(S \cup \lbrace x \rbrace) \subseteq span(S)$ and $span(S) \subseteq span(S\cup\lbrace{x}\rbrace)$, $span(S \cup \lbrace x \rbrace) = span(S)$
11. So, if $x\in span(S)$, $span(S) = span(S ∪\lbrace{x\rbrace})$
12. Now, we want to show if $span(S) = span(S ∪\lbrace{x\rbrace})$, $x\in span(S)$
13. Let $x \in (S \cup \{x\}) \implies x \in span(S \cup \{x\})$.
14. We're assuming $span(S) = span(S ∪\lbrace{x\rbrace})$. Hence,$$x\in span(S)$$
15. Because we've shown:
	1. IF $span(S) = span(S ∪\lbrace{x\rbrace})$, $x\in span(S)$
	2. IF $x\in span(S)$, $span(S) = span(S ∪\lbrace{x\rbrace})$
16. ... we can prove $x∈span(S)$ IF AND ONLY IF $span(S) = span(S ∪\lbrace{x\rbrace})$ $\blacksquare$

---
### (b) Suppose that $w ∈V$ but $w \notin S$. Further suppose that S is linearly independent. Prove that $S ∪{w}$ is linearly independent iff $w \notin span(S)$.

1. Assume $S∪{w}$ is linearly independent
2. Then, suppose $w\in span(S)$.
3. Then, for  $c_1, c_2, ..., c_k \in \mathbb{F}$, $w$ can be expressed as:$$w=c_1v_1+c_2v_2+...+c_kv_k$$
4. If we move $w$ to the other side we can get a linear combination of $v_1, v_2, ..., v_k, w$, hence $$0=c_1v_1+c_2v_2+...+c_kv_k+(-1)w$$
5. But $w$ has a coefficient of negative one so not all coefficients are zero, and $S \cup w$ is not linearly independent by definition.
6. Thus, if $S∪{w}$ is linearly independent, $w \notin span(S)$
7. Now, we have to show if $w \notin span(S)$, then $S \cup w$ is linearly independent
8. Assume $w \notin span(S)$.
9. Imagine for  $c_1, c_2, ..., c_k, a \in \mathbb{F}$, some equation exists such that $$0=aw+c_1v_1+c_2v_2+...+c_kv_k$$
10. If a is not zero,$$\begin{equation}\begin{split}-aw&=c_1v_1+c_2v_2+...+c_kv_k\\w&=-\frac{c_1v_1+c_2v_2+...+c_kv_k}{a}\\\\w&=-\frac{c_1}{a}v_1-\frac{c_2}{a}v_2 - \text{...} -\frac{c_k}{a}v_k\end{split}\end{equation}$$
11. But that makes $w$ a linear combination of S, which contradicts Step 8
12. Hence a = 0 bc it can't be nonzero
13. That means $aw=0$, such that$$0=c_1v_1+c_2v_2+...+c_kv_k$$
14. And we know $S$ is linearly independent, so $c_1=c_2=...=c_k=0$. Recall that a=0. Therefore,  every coefficient of the linear combination is zero. 
15. Hence, $S \cup w$ is linearly independent
16. Because we've shown:
	1. If $S∪{w}$ is linearly independent, $w \notin span(S)$
	2. If $w \notin span(S)$, then $S \cup w$ is linearly independent
17. ... we can prove that $S ∪{w}$ is linearly independent iff $w \notin span(S)$.

---
### (c) We write $A ⊊ B$ to mean $A ⊆B$ and $A \neq B$. Prove that for any $k ∈ \mathbb{N}$, a set $S= \{u_1, . . . , u_k\}$ is linearly independent iff $\{0\}⊊ span(\{u_1\}) ⊊ span(\{u_1, u_2\}) ⊊···⊊ span(\{u_1, . . . , u_k\})$.

1. Let $S_k=\{u_1, ..., u_k\}$, $W_i=span⁡(\{u_1,…,u_i\})$
2. Suppose $S$ is linearly independent.
3. Then $u_1\neq 0$ by linear independence, so $\{0\}⊊W_1$
4. Adding a vector to $span(\{u_1, u_2, ...\})$ cannot shrink the span. 
5. Thus, for $1≤i<k$,  $W_i⊆W_{i+1}$
6. Suppose $W_i=W_{i+1}$
	1. Then, $u_{i+1}\in W_i$
	2. Thus, $u_{i+1}$ would be a linear combination of $u_1, ..., u_i$
	3. BUT we assumed $S$ is linearly independent, so this is impossible.
7. Hence, $W_i\neq W_{i+1}$ which makes $W_i​⊊W_{i+1​}$ for all i.
8. Hence, we've built a chain that shows: $$\{0\}⊊ span(\{u_1\}) ⊊ span(\{u_1, u_2\}) ⊊···⊊ span(\{u_1, . . . , u_k\})$$
9. Thus, if $S$ is linearly independent, $\{0\}⊊ span(\{u_1\}) ⊊ span(\{u_1, u_2\}) ⊊···⊊ span(\{u_1, . . . , u_k\})$.
10. Now, we have to show if $\{0\}⊊ span(\{u_1\}) ⊊ span(\{u_1, u_2\}) ⊊···⊊ span(\{u_1, . . . , u_k\})$, then $S$ is linearly independent.
11. Suppose $\{0\}⊊W_1⊊W_2⊊...⊊W_k$
12. Suppose $S_k$ is linearly dependent (not independent)
13. Then, $\exists c_1, ..., c_k \in \mathbb{F}$ such that:$$c_1u_1+...+c_ku_k=0$$
14. Let $j$ be the highest index st. $c_j \neq 0$.
15. Then, $$c_1u_1+...+c_ju_j=0$$
16. Since $c_j \neq 0$, we can solve for $u_j = −(c_1​/c_j​)u_1-⋯−(c_{j−1}​/c_j​)u_{j−1}$
17. Hence, $u_j \in W_{j-1}$
18. case a: If j=1, then $u_1=0$, so $W_1=\{0\}$, contradicting $\{0\}⊊W_1$​.
19. case b: If j>1, then $W_j=W_{j−1}$​, contradicting $W_{j−1}⊊W_j$​.
20. Both a & b are impossible, so $S$ must be linearly independent.
21. Therefore $S$ is linearly independent iff $\{0\}⊊ span(\{u_1\}) ⊊ span(\{u_1, u_2\}) ⊊···⊊ span(\{u_1, . . . , u_k\}) \blacksquare$