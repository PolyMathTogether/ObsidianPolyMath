---
tags:
  - Complex-Analysis
  - Mathematical-Analysis
---

Definition (Residue). Let $f: U \to \mathbb C$ be [[Holomorphic]], and let $z_0 \in \mathbb C$. We define $$\mathrm{Res}(f, z_0) = \frac{1}{2\pi i} \int_\gamma f \, dz$$ where $\gamma$ is a positively oriented simple closed curve enclosing $z_0$.

# Residue theorem
Definition: The Residue theorem  states that the line integral of curve $\gamma$ is the sum of it's residues inside $\gamma$
$$\int_\gamma=2\pi{i}\sum \text{Res}(f,a_k),\text{ whereas } a_k \text{ is the residues}$$
# Applications to computing integrals
Example 1. Consider $$\int_{-\infty}^\infty \frac{1}{1+x^2}\, dx$$ This is perhaps not the best example of the power of the Residue theorem, considering we know from elementary calculus that $\frac{d}{dx} \arctan x = \frac{1}{1+x^2}$ and therefore $$\int_{-\infty}^{\infty} (1+x^2)^{-1}\, dx = \arctan(\infty) - \arctan(-\infty) = \pi/2 + \pi/2 = \pi.$$ However, the method we will describe does not rely on the fundamental theorem of calculus (namely, the statement that $\int_a^b \frac{d}{dx} f(x) \, dx = f(b)-f(a)$), and therefore can be used to compute integrals in scenarios when the anti-derivative of a function cannot be expressed in terms of "elementary functions." Here, *elementary functions* refer to the canon of functions we deem "elementary" (composition, sums, and products of functions like $e^x$, $\log x$, polynomials, rational functions, trig/hyperbolic functions).

As a first step, we note that $f(z) = (1 + z^2)^{-1}$ is holomorphic wherever it is defined, and has simple poles (i.e. poles of order 1) at $z = \pm i$. Now, we just need to bring our integral into a setting in which the Residue theorem applies. We define a simple closed curve $C_R$ to be a semicircle in the upper-half plane with diameter running along the real axis. To be precise, we define $\gamma_{\text{arc}, R}(t) = Re^{it}$ for $0 \leq t \leq \pi$ and define $\gamma_{[-R,R]}(t) = t$ for $-R \leq t \leq R$. This curve will enclose the pole at $+i$ for $R > 1$.
![[contour_ex1.png]]
We have that $$\int_{C_R} f(z) \,dz = \int_{\gamma_{\text{arc}, R}} f + \int_{\gamma_{[-R,R]}} f = \int_{\gamma_{\text{arc}, R}} f + \int_{-R}^R f(x) \, dx$$ and for $R > 1$, we have by the residue theorem that $$\int_{C_R} f(z) \, dz = 2\pi i\,\mathrm{Res}(f, i).$$ Now, let $R \to \infty$. The idea is that *if* $\int_{\gamma_{\text{arc}, R}} f \to 0$ then $$2\pi i\,\mathrm{Res}(f, i) = \int_{-\infty}^\infty f(x)\, dx.$$ Thus, we have reduced computing this integral to computing the residue of $f$ at $i$. There are many methods for computing the residue of poles (see [wikipedia](https://en.wikipedia.org/wiki/Residue_theorem)). Here, I'll compute the residue of $f$ at the simple pole $i$ as $$\mathrm{Res}(f, i) = \lim_{z \to i} (z-i)f(z) = \lim_{z \to i} \frac{z-i}{(z+i)(z-i)} = \frac{1}{2i}.$$ Thus, $$\pi = 2\pi i \left(\frac{1}{2i}\right) = 2\pi i\,\mathrm{Res}(f, i) = \int_{-\infty}^\infty f(x)\, dx = \int_{-\infty}^\infty \frac{1}{1+x^2}\, dx.$$
## Details
Above is a good outline of the typical integral computation using residues. However, I skipped the proof that $\int_{\gamma_{\mathrm{arc}, R}} f \to 0$ as $R \to \infty$, as well as the necessary steps to make the argument that $2\pi i\, \mathrm{Res}(f, i) = \int_{-\infty}^\infty f(x)\, dx$ rigorous.

By definition of the line integral,
$$\int_{\gamma_{\mathrm{arc}, R}} \frac{1}{1+z^2} \, dz = \int_0^\pi \frac{iRe^{it}}{1 + R^2e^{2it}}\, dt.$$
It follows that $$\left|\int_{\gamma_{\mathrm{arc}, R}} \frac{1}{1+z^2} \, dz\right| \leq \int_0^\pi \left|\frac{iRe^{it}}{1 + R^2e^{2it}}\right|\, dt = \int_0^\pi \frac{|iRe^{it}|}{|1 + R^2e^{2it}|}\, dt \leq \int_0^\pi \frac{R}{|1-R^2|}\, dt = \frac{\pi R}{|1-R^2|}.$$ Hence, $$\lim_{R\to \infty} \int_{\gamma_{\textrm{arc}, R}}f \leq \lim_{R\to \infty} \frac{\pi R}{|1-R^2|} = 0.$$ It follows that we can say $$2\pi i\,\mathrm{Res}(f, i) = \lim_{R\to \infty}2\pi i\,\mathrm{Res}(f, i) = \lim_{R\to \infty} 
\left(\int_{\gamma_{\text{arc}, R}} f + \int_{-R}^R f(x) \, dx\right).$$ Since the limits of the summands in the RHS converge, $$\lim_{R\to \infty} 
\left(\int_{\gamma_{\text{arc}, R}} f + \int_{-R}^R f(x) \, dx\right) = \lim_{R\to \infty}\int_{\gamma_{\text{arc}, R}} f + \lim_{R\to \infty}\int_{-R}^R f(x) \, dx = 0 + \int_{-\infty}^\infty f(x)\, dx$$ and finally putting it all together, $$2\pi i\,\mathrm{Res}(f, i) = \int_{-\infty}^\infty f(x)\, dx.$$
