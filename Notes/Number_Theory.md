# Number Theory 数论

Number theory is a branch of mathematics that explores integers and their properties, is the basis of cryptography, coding theory, computer security, e-commerce, etc.

数论是研究整数及其性质的数学分支，是密码学、编码理论、计算机安全、电子商务等领域的基础。

## Divisibility 整除性

If $a$ and $b$ are integers and $a\neq 0$, we say that $a$ divides $b$ if there is an integer $k$ such that $b=ak$. We write $a|b$. If $a$ does not divide $b$, we write $a\nmid b$.

如果$a$和$b$是整数且$a\neq 0$，我们说$a$整除$b$，如果存在整数$k$使得$b=ak$。我们写作$a|b$。如果$a$不能整除$b$，我们写作$a\nmid b$。

- All integers divisible by $d>0$ can be enumerated as $$\cdots -kd,\dots ,-2d,-d,0,d, 2d, 3d, \cdots, kd ,\cdots $$.

### Properties of Divisibility 整除性质

1. If $a|b$ and $a|c$, then $a|(b+c)$. 整除具有线性性。
2. If $a|b$ then $a|bc$ for any integer $c$. 整除具有乘法性。
3. If $a|b$ and $b|c$, then $a|c$. 整除具有传递性。

## Division Algorithm 除法算法

If $a$ and $b$ are integers and $d>0$, then there exist unique integers $q$ and $r$ such that $a=dq+r$ and $0\leq r<d$. The a is called **divident(被除数)** and d is called **divisor(除数)**. The integers $q$ is called **quotient(商)** and $r$ is called **remainder(余数)**.

### notation

- q=a div d 求商
- r=a mod d 求余

### Congruence relation 同余

If $a$ and $b$ are integers and $m$ is a positive integer, we say that $a$ is congruent to $b$ modulo $m$ if $m|(a-b)$. We write $a\equiv b\pmod{m}$.

如果$a$和$b$是整数，$m$是正整数，我们说$a$与$b$模$m$同余，如果$m|(a-b)$。我们写作$a\equiv b\pmod{m}$。

- a ≡ b (mod m) and a mod m = b are different. The former is a **relation**, the latter is an **operation**.
- Let a and b be integers, and let m be a positive integer. Then a ≡ b mod m if and only if a mod m = b mod m.

$$
\begin{aligned}
    a&=q_1m+r_1 \\
    b&=q_2m+r_2 \\
    a \equiv b \pmod{m} &\Leftrightarrow m|(a-b) \\
    &\Leftrightarrow m|(q_1m+r_1-q_2m-r_2) \\
    &\Leftrightarrow m|(q_1-q_2)m+(r_1-r_2) \\
    &\Leftrightarrow r_1\equiv r_2 \pmod{m} \\
    and -m&<r_1-r_2<m \\
    &\rightarrow r_1=r_2 \\
    &\rightarrow a\ mod\ m=r_1=r_2=b\ mod\ m
\end{aligned}
$$

- If $a \equiv b \pmod{m}$ and $c \equiv d \pmod{m}$, then $a+c \equiv b+d \pmod{m}$ and $ac \equiv bd \pmod{m}$.

## Arithmetic Modulo m 算术模

- Closure property 封闭性: If $a$ and $b$ are integers, then $a+b$ and $ab$ are integers. If $a$ and $b$ are congruent modulo $m$, then $a+b$ and $ab$ are congruent modulo $m$. 如果$a$和$b$是整数，那么$a+b$和$ab$也是整数。如果$a$和$b$模$m$同余，那么$a+b$和$ab$也模$m$同余。
- Associative property 结合律: If $a,b,c \in Z_m$, then $(a+_mb)+_mc=a+_m(b+_mc)$ and $(a\cdot_m b)\cdot_m c=a\cdot_m (b\cdot_m c)$.
- Identity property 恒等性: $a+_m0=a$ and $a\cdot_m 1=a$.
- Additive inverse property 加法逆元: For each $a\in Z_m$, then m-a is the additive inverse of a modulo m.
- Commutative property 交换律: If $a,b \in Z_m$, then $a+_m b=b+_m a$ and $a\cdot_m b=b\cdot_m a$.
- Distributive property 分配律: If $a,b,c \in Z_m$, then $a\cdot_m (b+_m c)=a\cdot_m b+_m a\cdot_m c$.

> 单位元（幺元）：对于一个集合，如果存在一个元素，使得它与集合中的任意一个元素进行某种运算后，得到的结果仍然是这个元素，那么这个元素就是这个集合关于这种运算的单位元。写作$e$或$1_e$。

## Group 群

A set $G$ with a binary operation $*$ is called a group if the following properties hold:

- Closure: For all $a,b\in G$, $a*b\in G$.
- Associative: For all $a,b,c\in G$, $(a*b)*c=a*(b*c)$.
- Identity: There exists an element $e\in G$ such that for all $a\in G$, $a*e=e*a=a$.
- Inverse: For each $a\in G$, there exists an element $a^{-1}\in G$ such that $a*a^{-1}=a^{-1}*a=e$.

## Permutation Group 置换群

Let $S_n$ denotes a sequence of integers 1 through n. Denoted by $P_n$ the set of all permutations of $S_n$. The set $P_n$ is a group under the operation of composition of permutations.

### permutation 置换

Define a binary operation ◦ on the elements of Pn: for ρ, π ∈ Pn, π ◦ ρ denotes a re-permutation of the elements of ρ according to the elements of π.
TODO

### Abelian Group 交换群

If a group G has the property that for all a, b ∈ G, a ∗ b = b ∗ a, then G is called an abelian group.

## Ring 环

A set R with two binary operations + and · is called a ring if the following properties hold:

- R is an abelian group under addition.
- Closure. 封闭性
- Associative. 结合律
- Distributive. 分配律

## Commutative Ring 交换环，Integral Domain 整环

A ring is commutative if the multiplication operation is commutative for all elements in the ring. (ab = ba).

An integral domain is a **commutative ring** with two additional property that 

1. Identity element for multiplication: a1 = 1a = a
2. Nonzero product: If a · b = 0, then either a = 0 or b = 0.

## Field 域

A field ,denoted by $(F,+,\times)$, is a Integer ring with a additional properties:

1. Inverse for multiplication: For each $a\in F$, there exists an element $a^{-1}\in F$ such that $a\cdot a^{-1}=a^{-1}\cdot a=1$. 

> 有限域的元素个数为素数的幂次方。