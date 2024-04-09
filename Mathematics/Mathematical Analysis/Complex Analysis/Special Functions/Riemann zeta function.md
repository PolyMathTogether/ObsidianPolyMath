---
tags:
  - Special-Functions
  - Complex-Analysis
  - Mathematical-Analysis
---
**Riemann Zeta function**, denoted by **Greek letter** $\zeta$, is defined as
$$
\zeta(s) = \sum_{n=1}^{\infty} \frac{1}{n^s} \hspace{3em}  \tag*{$\mathcal{Re}(s) > 1$}
$$
Elsewhere $\zeta(s)$ is defined by [[Analytic Continuation]]. It is a [[Meromorphic]] function on $\mathbb{C}$ or [[Holomorphic]] everywhere except only simple pole at $s=1$ with [[Residue]] $1$.

# Integral Representation
---
The zeta function can be represented as
$$\boxed{\zeta(s) = \frac{1}{\Gamma(s)}\int_{0}^{\infty} \frac{x^{s-1}}{e^x-1} \, dx}  \tag*{$\mathcal{Re}(s) > 1$}$$
Where $\Gamma(s)$ is [[Gamma Function]]
$$
\Gamma(s) = \int_{0}^{\infty} x^{s-1}e^{-x} \, dx \tag*{}
$$
**Contour integral** representation:
$$\zeta(s) = \frac{\Gamma(s-1)}{2\pi i} \int_{C} \frac{(-z)^s}{e^z - 1} \, \frac{dz}{z} $$
Where $C$ is **Hankel Contour**.

# Euler Product
---
In 1937, Euler found a **marvellous equality** between infinite sum and an infinite product. It is the important bridge connecting **prime numbers** and **the riemann zeta function** in **Analytic Number Theory**. This formula is known as Euler Product:
$$\boxed{\sum_{n} \frac{1}{n^s} = \prod_{p} \frac{1}{1-p^{-s}}} \tag{$\star$}$$
Where $n$ ranges over all **positive numbers** and $p$ ranges over all **primes**.

Each factor on the right of $(\star)$ is the sum of a [[Geometric Series]]:
$$
\frac{1}{1-p^{-s}} = 1 + \frac{1}{p^s} + \frac{1}{p^{2s}} + \dots \tag*{}
$$
Thus formula $(\star)$ can be rewritten as,
$$
\sum_{n} \frac{1}{n^s} = \prod_{n} \sum_{k=0}^{\infty} \frac{1}{p^{ks}} = \prod_{p} \left( 1 + \frac{1}{p^s} + \frac{1}{p^{2s}} + \dots  \right) \tag*{}
$$

**Euler product** is also the easy way to prove the **Infinitude of Primes**.

# Bernoulli Numbers
---
[[Bernoulli Number]] has **many applications** in mathematics such as summing powers of integers, finding asymptotics of [[Stirling’s formula]], and estimating the [[Harmonic Series]], ... And it also frequently pop up in considerations involving the **zeta function**.

## Definition
---
The **Bernoulli Numbers** $B_{n}$ are defined to be the coefficients in the series expansion

$$\boxed{\frac{z}{e^z-1} = \sum_{n=0}^{\infty} \frac{B_{n}z^n}{n!}} \tag{1}$$
Replacing $e^z - 1$ with its [[Taylor Series]] to $(1)$ we can see that
$$
z = \left(\sum^{\infty}_{n=1} \frac{z^n}{n!}\right)\left(\sum_{n=0}^{\infty} \frac{B_{n}z^n}{n!}\right) = \sum_{n=0}^{\infty} \left(\sum_{k=0}^{n-1}\binom{n}{k}B_{k}\right) \frac{z^n}{n!} \tag{2}
$$
Comparing the coefficients of power of $z$ both sides of $(2)$, we get
$$z^n: \hspace{1em} [n=1] = \sum_{k=0}^{n-1}\binom{n}{k} B_{k} \tag*{}$$
Replacing $n-1$ with $n$, we have formula
$$
\boxed{\sum_{k=0}^{n}\binom{n+1}{k} B_{k} = [n=0]} \tag*{}
$$
Where $[P]$ is **Iverson bracket**.

The first few **Bernoulli numbers** are
$$
\begin{array}{cccccccc}
B_0 & = & 1, & B_1 & = & -\frac{1}{2}, & B_2 & = \frac{1}{6}, \\
B_3 & = & 0, & B_4 & = & -\frac{1}{30}, & B_5 & = 0, \\
B_6 & = & \frac{1}{42}, & B_7 & = & 0 \\
\end{array}
\tag*{}$$
## Relationship to Zeta Function
---
**Euler** also discoveried the formula for exact values of $\zeta(2n)$ for $n \in \mathbb{N}$
$$
\boxed {\zeta(2n) = - \frac{(2\pi i)^{2n} B_{2n}}{2(2n)!}} \tag{3}
$$

By **Euler's reflection formula** for [[Gamma Function]] we have
$$
\Gamma(1-z)\Gamma(z) = \frac{\pi}{\sin(\pi z)} \tag*{}
$$
Replacing $s \mapsto \frac{s+1}{2}$
$$\Gamma\left( \frac{1+s}{2} \right)\Gamma\left( \frac{1-s}{2} \right) = \frac{\pi}{\cos\left( \frac{\pi s}{2} \right)} \tag{4}$$Also for **Legendre duplication formula**
$$\Gamma(2z) = \frac{2^{2z}}{2\sqrt{ \pi }} \Gamma(z)\Gamma\left( z+\frac{1}{2} \right) \tag*{}$$
Replacing $s \mapsto \frac{s}{2}$
$$ \Gamma\left( \frac{1+s}{2} \right) \Gamma\left( \frac{s}{2} \right) = 2^{1-s}\sqrt{ \pi }\, \Gamma(s) \tag{5}$$

Dividing both sides from $(5)$ to $(4)$ 
$$\frac{\Gamma\left( \frac{s}{2} \right)}{\Gamma\left( \frac{1-s}{2} \right)} = \frac{2^{1-s}}{\sqrt{ \pi }} \Gamma(s)\cos\left( \frac{\pi s}{2} \right) \tag{6}$$
By **Functional Equation** for **Riemann Zeta Function**
$$\pi^{-s/2}\Gamma\left(\frac{s}{2}\right)\zeta(s) = \pi^{s/2 - 1/2}\Gamma\left(1 - \frac{s}{2}\right)\zeta(1-s) \tag{7}$$
Substituting $(6)$ to $(7)$, we finally get the **Unsymmetric Functional Equation** for **Riemann Zeta Function**
$$\boxed{\zeta(1-s) = \pi^{-s} \, 2^{1-s} \, \cos\left(\frac{\pi s}{2}\right) \, \Gamma(s) \, \zeta(s)} \tag{8}$$
Now for $s = 2n$ with $n \in \mathbb{N}$, $\cos\left( \frac{\pi s}{2} \right) = (-1)^n$ and $\Gamma(2n) = (2n-1)!$, substitute the value of $(3)$ to $(8)$
$$
\boxed{\zeta(1-2n) = - \frac{B_{2n}}{2n}} \tag*{} 
$$

# References
---
1. https://www.whitman.edu/documents/academics/majors/mathematics/2019/Larson-Balof.pdf
2. https://en.wikipedia.org/wiki/Bernoulli_number
3. https://math.osu.edu/sites/math.osu.edu/files/Bernoulli_numbers.pdf
4. https://arxiv.org/abs/1812.02574
5. https://mikespivey.wordpress.com/2015/03/09/proof-of-the-recursive-identity-for-the-bernoulli-numbers/
6. https://en.wikipedia.org/wiki/Euler_product
7. https://en.wikipedia.org/wiki/Riemann_zeta_function
8. https://proofwiki.org/wiki/Unsymmetric_Functional_Equation_for_Riemann_Zeta_Function
9. https://people.reed.edu/~jerry/361/lectures/bernoulli.pdf
10. https://www.cut-the-knot.org/proofs/AfterEuler.shtml