# Introduction
---
Another method to calculate **integrals** is using **approximate numerical methods**, which you may see *somewhere* in **Calculus**, such as [[Riemann Sums]]. **Newton-Cotes formulas** are a class of methods to achieve that purpose. These include popular rules like **Simpson's rule**, **midpoint rule**, **Trapezoidal rule**, ...

# Euclidean Division
---
Given **2 polynomials** $a$ and $b \neq 0$, there exist **2 polynomial** $q$ (quotient) and $r$ (remainder) which statisfy
$$
\boxed{a = qb + r} \tag{1}
$$
and
$$
\deg(r) < \deg(q) \tag*{}
$$

# Polynomial Remainder Theorem
---
Given number $r$ and polynomial $f(x)$, by using **Euclidean Division theorem** $(1)$ for $f(x)$ and $(x-r)$
$$
f(x) = Q(x)(x-r) + R(x) \tag*{}
$$

Then replacing $x=r$, we get
$$
f(r) = R(r) \tag*{}
$$
which is the remainder. Thus we can rewrite the formula as
$$
\boxed{
f(x) = Q(x)(x-r) + f(r)} \tag{2}
$$

# Chinese Remainder Theorem
---
Given **pairwise coprime** positive numbers $\{n_i\}$ and integers $\{a_{i}\}$ such that $0 \leq a_{i} < n_{i}$ with $1 \leq i \leq k$ then
$$
\begin{aligned}
x &\equiv a_{1} \hspace{1em} (\operatorname{mod} n_{1} ) \\
& \vdots \\
x &\equiv a_{k} \hspace{1em} (\operatorname{mod} n_{k} ) \\
\end{aligned}
$$
has a solution.

## Bézout's Identity
---
Let $a$ and $b$ be integers and $d$ is the **greatest common divisor** of $a$ and $b$. Then there exists $x$ and $y$ such that $ax + by = d$

## Solution
---
Let $N_i = \prod_{m\neq i} n_{m}$ so $\gcd(N_{i}, n_{i})=1$ thus by **Bézout's identity** we have
$$
M_{i} N_{i} + m_{i} n_{i} = 1
$$
then the solution of the system $()$ is 
$$
\boxed{x = \sum_{i=1}^k a_{i}M_{i}N_{i}}
$$
## Lagrange Interpolation
---
Rewrite the system $()$ for polynomial $P_{n}(x)$ we have
$$
\begin{aligned}
P_{n}(x) &\equiv y_{0} \hspace{1em} (\operatorname{mod} x-x_{0} ) \\
& \vdots \\
P_{n}(x) &\equiv y_{n} \hspace{1em} (\operatorname{mod} x-x_{n} ) \\
\end{aligned}
$$
thus the solution of $P_n(x)$ is 
$$
P_{n}(x) = \sum_{m=0}^n M_{m}N_{m} f(x_{m})
$$
where $M_{m} = \prod_{j \neq m} (x-x_{j})$ and $N_{m} = \prod_{j\neq m}(x_{m}-x_{j})^{-1}$ 
# Polynomial Interpolation
---
**Interpolating polynomial** is defined to be a polynomial that fits a set of given **data points of a function** and give the **exact value** corresponding the value of the function being approximated.
## Lagrange Interpolation
---
Let $P_{n}(x)$ be the **Lagrange Polynomial** order of $n$ that passes through **set of data points** $\{\,(x_{0}, f(x_{0})), (x_{1}, f(x_{1})), \dots, (x_{n}, f(x_{n}))\,\}$ and is defined as

$$
\boxed{P_{n}(x) = \sum_{m=0}^n \ell_{m}(x) f(x_{m})} \tag{1} 
$$
where $\ell_{m}(x) = \prod_\limits{\substack{j=1 \\ j \neq m}}^n \frac{x-x_{j}}{x_{m}-x_{j}}$ is **the Lagrange basis polynomial**.
Let $\ell(x)=\prod_{j}(x-x_{j})$ then the **basis** can be also represented as
$$
\ell_{m}(x) = \frac{\ell(x)}{\ell'(x_{m})(x-x_{m})} \tag{2}
$$
## Newton Interpolation
---
Instead of using **Lagrange Polynomial**, you can use **Newton Polynomial** form which is defined as
$$
\boxed{P_{n}(x) = \sum_{m=0}^n c_{m}w_{m}(x)}
$$
or by **the recursive relation**
$$
P_{n}(x) = P_{n-1}(x) + c_{n}w_{n}(x)
$$

where $c_m$ is **divided difference** $[y_{0},\dots,y_{m}]$ and $w_m=\prod_{j=0}^{m-1}(x-x_{j})$ with $w_{0} = 1$ is **the Newton basis polynomial**.

The **forward divided differences** can be defined as
$$
\begin{aligned}
\mathopen{[y_{k}]} &:=y_{k} \\
\mathopen{[y_{k},\dots,y_{k+j}]} &:= \frac{\mathopen{[y_{k+1},\ldots ,y_{k+j}]-[y_{k},\ldots ,y_{k+j-1}]}}{x_{k+j}-x_{k}}
\end{aligned}
$$
It can be also represented by using **Newton tableau**
$$
\begin{matrix}
x_{0} & y_{0} = [y_{0}] \\ 
& &[y_{0},y_{1}] & \\ 
x_{1} & y_{1} = [y_{1}] & & [y_{0},y_{1},y_{2}] \\ 
& &[y_{1},y_{2}] & & [y_{0},y_{1},y_{2},y_{3}]\\
x_{2} & y_{2} = [y_{2}] & & [y_{1},y_{2},y_{3}]\\ 
& &[y_{2},y_{3}] \\
x_{3} & y_{3} = [y_{3}]
\end{matrix}
$$

By putting the point $x_{n+1}=x$ we get
$$
\begin{aligned}
P_{n+1}(x) &= P_{n}(x) + [y_{0},\dots,y_{n},y] \ell(x) \\
P_{n+1}(x) - P_{n}(x) &= [y_{0},\dots,y_{n},y] \ell(x) \\
f(x) - P_{n}(x) &= [y_{0},\dots,y_{n},y] \ell(x)
\end{aligned}
$$
where $\ell(x) = w_{n+1}(x)$

This is also called the **remainder of the interpolation polynomial**.
## Hermite Interpolation Formula
---
![[HermiteFormula.excalidraw|center]]

Let $\Gamma_{m}$ be the **contour** around **only one point** $x_{m}$ in a **counterclockwise** manner then $(2)$ can be rewritten
$$
\ell_{m}(x) = \frac{1}{2\pi i}\int_{\Gamma_{m}}  \frac{\ell(x)}{\ell(z)(x-z)} \, dz  \tag{3}
$$
This can be verified by taking the [[Residue]]
$$
\operatorname{Res}\left( \frac{1}{\ell(z)(x-z)}, x_{m} \right) = \lim_{ z \to x_{m} } \frac{1}{\ell'(z)(x-z) - \ell(z)} =  \frac{1}{\ell(x_{m})(x-x_{m})} \tag*{}
$$
Let $\Gamma'$ be the **closed contour** that contains $x_m$ except the point $x$ then from $(1)$ and $(3)$ we have
$$
P_{n}(x) = \frac{1}{2\pi i}\sum_{m} \int_{\Gamma_{m}}  \frac{\ell(x)f(z)}{\ell(z)(x-z)} \, dz = \frac{1}{2\pi i} \int_{\Gamma'}  \frac{\ell(x)f(z)}{\ell(z)(x-z)} \, dz
$$
Now by extending the contour to $\Gamma$ which contains the points $x$ and $x_m$
$$
\begin{aligned}
\frac{1}{2\pi i} \int_{\Gamma}  \frac{\ell(x)f(z)}{\ell(z)(x-z)} \, dz &= \operatorname{Res}\left( \ell(x)\frac{f(z)}{\ell(z)(x-z)}, x \right) + \frac{1}{2\pi i} \int_{\Gamma'}  \frac{\ell(x)f(z)}{\ell(z)(x-z)} \, dz \\
&= \lim_{ z \to x } \frac{\ell(x)f(z)}{\ell'(z)(x-z) - \ell(z)} + \frac{1}{2\pi i} \int_{\Gamma'}  \frac{\ell(x)f(z)}{\ell(z)(x-z)} \, dz \\ 
&= P_{n}(x) - f(x) 
\end{aligned} \tag*{}
$$
or
$$
\boxed{f(x)-P_{n}(x) = \frac{1}{2\pi i} \int_{\Gamma}  \frac{\ell(x)f(z)}{\ell(z)(z-x)} \, dz } \tag{4}
$$
which is also the **remainder term of lagrange polynomial**.

So the **contour integral** representation on contour $\Gamma$ for **lagrange polynomial** can be written as
$$
P_{n}(x) = f(x) - \frac{1}{2\pi i} \int_{\Gamma}  \frac{\ell(x)f(z)}{\ell(z)(z-x)} \, dz 
$$
or
$$
\boxed{P_{n}(x) = \frac{1}{2\pi i}\int_{\Gamma} \frac{f(z)(\ell(z)-\ell(x))}{\ell(z)(z-x)}  \, dz }
$$
This is also known as **Hermite interpolation formula**

## Approximation Error
---
Consisder **remainder term** $R_n(x)$ which is the **approximation error** when approximating function $f$ with **Interpolation Polynomial**
$$\boxed{R_{n}(x) = f(x) - P_{n}(x)} \tag{2}$$
Because the **Interpolation Polynomial** itself gives the exact value of point $x_m$ thus
$$
R_{n}(x_{m}) = 0 \tag*{}
$$
Contour integral form of the remainder
$$
R_{n}(x) = \frac{\ell(x)}{2\pi i} \int_{\Gamma}  \frac{f(z)}{\ell(z)(z-x)} \, dz 
$$
Lagrange form of the remainder
$$
R_{n}(x) = \ell(x)\left( \frac{f(x)}{\ell(x)} - \sum_{m}^{n} \frac{f(x_{m})}{\ell'(x_{m})(x-x_{m})}  \right)
$$
Newton form of the remainder
$$
R_{n}(x) = \ell(x)[y_{0},\dots,y_{n},y]
$$
Thus we can observe that $R_{n}(x)$ has at least $n+1$ distinct zeros at $x_{0},\dots,x_{n}$. By **Rolle's theorem** between distict $x_m$ and $x_{m+1}$, there exists at least one of $R_n'(x)$. Thus, $R'_n(x)$ has at least $n$ zeros between $x_0$ and $x_n$. So on, we can conclude that $R^{(n+1)}(x)$ has at least one zero $\xi \neq x_{m}$ in the interval $(x_{0}, x_{m})$
$$
 f^{(n)}(\xi) - P_{n}^{(n)}(\xi) = 0
$$
Now by the newton interpolation, we know that $P_{n}(x) = [y_{0},\dots,y_{n}]x^n+\dots$ Hence, we obtain the **mean value theorem** for **Divided Differences**
$$
 [y_{0}, \dots, y_{n}] =\frac{f^{(n)}(\xi)}{n!}
$$
Finally we can rewrite the remainder as
$$
\boxed{R_{n}(x)= \frac{f^{(n+1)}(\xi(x))}{(n+1)!}\ell(x)}
$$
where $\xi(x) \in (\min\{x_{0}, x\} , \max\{x_{n}, x\})$
# Newton–Cotes Formulas
---
After constructing the **Lagrance polynomial**, **Newton–Cotes formulas** can be defined as follows
$$
\int_{a}^b f(x) \, dx \approx \int_{a}^b P_{n}(x) \, dx = \sum_{m} f(x_{m}) \int_{a}^b  \ell_{m}(x) \, dx \tag{2}
$$
where 
- $x_m = a + mh$ with $h = \frac{b-a}{n}$ for closed formula.
- $x_m = a + (m+1)h$ with $h = \frac{b-a}{n+2}$ for closed formula.

To be able to use $(2)$ we need to calculate the weights $w_k$
$$
w_{m} = \int_{a}^b  \ell_{m}(x) \, dx, \hspace{3em} k = 0,\dots,n \tag*{}
$$
Then $(2)$ can be rewritten as
$$
\boxed{\int_{a}^b f(x) \, dx \approx w_{0}f(x_{0}) + w_{1}f(x_{1})+ \dots + w_{n}f(x_{n})} \tag*{}
$$
## Error Analysis
---
The error of the **Newton–Cotes formulas** $E_{n}(x)$ is defined as 
$$
\left| \int R_{n}(x) \, dx \right| \leq E_{n}(x)
$$
So using $(*)$ we obtain
$$
\left| \int_{a}^b R_{n}(x) \, dx \right| = \left| \int_{a}^b \frac{f^{(n+1)}(\xi(x))}{(n+1)!}\ell(x) \, dx  \right| \leq \frac{M_{n+1}}{(n+1)!} \left|\int_{a}^b \ell(x) \, dx \right|
$$

where $|f^{(n+1)}(\xi(x))| \leq M_{n+1}$. Thus we obtain
$$
E_{n} = \frac{M_{n+1}}{(n+1)!} \left|\int_{a}^b \ell(x) \, dx \right|
$$
substitute $x = ht + a$ we get the form
$$
E_{n}= h^{n+2} \frac{M_{n+1}}{(n+1)!} \left|\int_{0}^n \prod_{m} (t-m) \, dt \right|
$$
For $n=0$ with $x_0 = a$ it is known as **the rectangle rule**
$$
E_{0}=h^2 M_{1}\left|\int_{0}^1 t \, dt \right| = \frac{M_{1}}{2}h^2
$$
For $n=1$ with $x_{0}=a$ and $x_{1}=b$ we get **the trapiozal rule**
$$
E_{1}= h^3\frac{M_{2}}{2}\left|\int_{0}^1 t(t-1) \, dt \right| = \frac{M_{2}}{12}h^3
$$
For $n=2$ with points $a$, $\frac{a+b}{2}$, and $b$ it becomes the **1/3 Simpson's rule**
$$
E_{2}= h^4\frac{M_{3}}{6}\left|\int_{0}^2 t(t-1)\left( t-2 \right) \, dt\right|  = 0
$$
Oops zero appears!! But it doesnt mean the error is zero. It is just because the cubic term is zero. Instead, we can use the next term of the newton polynomial by adding one more interpolation point to calculate it
$$
E_{2}= h^5\frac{M_{4}}{24}\left|\int_{0}^2 t(t-1)( t-2 )(t-3) \, dt\right|  = \frac{M_{4}}{90}h^5
$$

# References
---
- **Divided Differences**
  1. https://en.wikiversity.org/wiki/Numerical_Analysis/Divided_differences
  2. https://en.wikipedia.org/w/index.php?title=Mean_value_theorem_(divided_differences)
  3. https://en.wikipedia.org/wiki/Divided_difference
- **Newton-Cotes Formulas**
  1. https://www.ndsu.edu/pubweb/~novozhil/Teaching/488%20Data/14.pdf
  2. https://en.wikipedia.org/wiki/Newton–Cotes_formulas
  3. https://mathworld.wolfram.com/Newton-CotesFormulas.html
  4. https://pages.cs.wisc.edu/~amos/412/lecture-notes/lecture19.pdf