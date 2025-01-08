# Algorithms 算法

An algorithm is a finite sequence of presice instructions for performing a computatio of for solving a problem. 算法是解决问题或执行计算的一系列精确指令。

## Big-O Notation 大O记号

$f(n)$ is $O(g(n))$ if there exists a positive constant c and an integer constant $n_0$ such that $0\leq f(n)\leq cg(n)$ for all $n\geq n_0$.

### Big-O Estimates for Some Functions

- $1+2+\cdots+n=\frac{n(n+1)}{2}=O(n^2)$
- $n!=O(n^n)$
- $log n!=O(n\log n)$
- $log_a n=O(n)$ for any constant $a\geq 2$
- $n^a=O(n^b)$ for integers $a\leq b$
- $n^a=O(b^n)$ for any constants $a>0$ and $b>1$

## Combinations of Functions 

If $f_1(x)\ is\ O(g_1(x))\ and\ f_2(x)\ is\ O(g_2(x))$, then

- $ f_1(x)+f_2(x)\ is\ O(max(g_1(x),g_2(x)))$
- $(f_1f_2)(x)\ is\ O(g_1(x)g_2(x))$.

## Big-Omega and Big-Theta Notation 大Ω和大Θ记号

$f(n)$ is $Ω(g(n))$ if there exists a positive constant c and an integer constant $n_0$ such that $0\leq cg(n)\leq f(n)$ for all $n\geq n_0$.

$f(n)$ is $Θ(g(n))$ if $f(n)$ is $O(g(n))$ and $f(n)$ is $Ω(g(n))$.

## Time and Space Complexity 时间和空间复杂度

- Time complexity: the number of operations performed by an algorithm. 时间复杂度：算法执行的操作次数。
- Space complexity: the amount of memory used by an algorithm. 空间复杂度：算法使用的内存量。

### Horner's Algorithm and Its Complexity 霍纳算法及其复杂度

1. Example: $f(x)=1+2x+3x^2+4x^3+5x^4$.

It takes 4 additions and 10 multiplications to evaluate $f(x)$ using the direct method.

Apply Horner's algorithm: $f(x)=1+x(2+x(3+x(4+5x)))$.

It takes 4 additions and 4 multiplications to evaluate $f(x)$ using Horner's algorithm.

#### 步骤：

- Step1: set S=$a_n$.
- Step2: for i=n-1 to 0 do S=$a_i+S\cdot x$.
- output S.

The number of operations needed in this algorithm is $1+3n+1=3n+2$. So the time complexity of Horner's algorithm is $O(n)$.



