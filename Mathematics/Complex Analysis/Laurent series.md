_Laurent series_ or Laurent expansion is a <u>representation</u> of function $f(z)$. It is normally used for complex function if _Taylor series_ doesnt work.
$$f(z) = \frac{1}{2\pi i} \sum_{-\infty}^{\infty} a_{n} (z - c)^n$$
Where:
- $c$ and $a_n$ are constants.
- $a_{n} =\frac{1}{2\pi i} \oint_{\gamma} \frac{f(z)}{(z-c)^{n+1}} \, dz$.

We also can write the infinite sum with:
$$f(z) = \frac{1}{2\pi i}\left[\sum_{n = 0}^{\infty} a_{n} (z - c)^n + \sum_{n = 1}^{\infty} \frac{b_{n}}{(z-c)^n}\right] \hspace{3em} (*)$$
Where:
- $b_n = a_{-n}$

The negative powers of $z-c$:
$$\sum_{n = 1}^{\infty} \frac{b_{n}}{(z-c)^n} = \frac{b_{1}}{z-c} + \frac{b_{2}}{(z-c)^2} + \cdots$$
is called **_Principle Part_** of $f$ at $c$. The other sum is called _**Analytic Part**_.

If there exists a number $k \in \mathcal{N}^+$ such that
$$b_{k} \neq 0 \text{ and } b_{n} = 0 \text{ for every } n > k$$
then $c$ is called a [[Pole]] of order $k$ a.k.a the isolated singularity of $f$.