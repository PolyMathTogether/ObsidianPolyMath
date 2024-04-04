---
tags:
  - Special-Functions
  - Complex-Analysis
  - Mathematical-Analysis
---
# Definition
---
The **gamma function** is a **special function** defined for all complex numbers except **non-positive numbers**. It is also known as the **The Euler integral of the second kind**. It is denoted by the uppercase Greek letter "Gamma" $\Gamma$:
$$
\Gamma(z) = \int_{0}^{\infty} t^{z-1}e^{-t} \, dt \hspace{3em} \mathcal{R}(z) > 0 
$$
The **gamma function** is defined by **analytic continuation**. It is a [[Meromorphic]] function with no **zeros** and with **simple poles** of residue $\text{Res}_{z = -n}\,\Gamma(z) = (-1)^n / n!$ for every **positive integers** $n$. $1/\Gamma(z)$ is an [[Entire Function]] with simple zeros at $z=-n$. 

For every **positive integers** $n$ the gamma function is [[Factorial]] of $n-1$:
$$
\Gamma(n) = (n-1)!
$$

# Functional Relations
---

- Recurrence:
  $$\Gamma(z) = z\Gamma(z-1)$$
- Euler's reflection formula:
  $$\Gamma(1-z)\Gamma(z) = \frac{\pi}{\sin(\pi z)}$$
- Legendre duplication formula:
  $$\Gamma(2z) = \frac{2^{2z}}{2\sqrt{ \pi }} \Gamma(z)\Gamma\left( z+\frac{1}{2} \right)$$
- Gauss’s multiplication formula:
  $$\Gamma(nz) = \frac{n^{nz}}{\sqrt{ n(2\pi)^{n-1} }} \prod_{k=0}^{n-1} \Gamma\left( z+ \frac{k}{n} \right)$$
# Other Properties
---
- Complex conjugate:
  $$\overline{\Gamma(z)} = \Gamma(\overline{z})$$
- Absolute value:
  $$|\Gamma(a+bi)|^2 = |\Gamma(a)|^2 \prod_{k=0}^{\infty}\frac{1}{1 + \frac{b^2}{(a+k)^2}}$$
  $$|\Gamma(bi)|^2 = \frac{\pi}{b\sinh \pi b}$$
  $$\left|\Gamma\left( \frac{1}{2} +bi \right)\right|^2 = \frac{\pi}{\cosh \pi b}$$
- Derivative:
  $$\Gamma'(z) = \Gamma(z) \psi(z)$$