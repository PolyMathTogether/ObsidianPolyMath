---
tags:
  - Special-Functions
  - Complex-Analysis
  - Mathematical-Analysis
---
# Definition
---
The **digamma function**, denoted as $\psi(z)$, is the **logarithm derivative** of the [[Gamma Function]]. It is also the **polygamma function** of first order:
$$
\psi (z) = \frac{d}{dz} \ln \Gamma (z) = \frac{\Gamma'(z)}{\Gamma(z)} \tag*{}
$$
**Digamma function** is also [[Holomorphic]] on $\mathbb{C}/\mathcal{Z}_{\leq 0}$ with simple poles where $z$ is **non-positive integer**.

# Properties
---
Using $\Gamma(z+1) = z\Gamma(z)$ we can derive a fundamental property for **digamma function**:
$$
\begin{align*}
\Gamma(z+1) &= z\Gamma(z) \, ,\\
\ln \Gamma(z+1) &= \ln z + \ln \Gamma(z) \\
\end{align*} \tag*{}
$$
Finally, **differentiate** both sides we get:
$$
\boxed{\psi (z+1) = \frac{1}{z} + \psi (z)} \tag{1}
$$

By using the **recurrence relation** $(1)$ for $z = n \in \mathbb{Z}^{0+}$ we can get a relation with [[Harmonic Series]]:
$$
\psi (n+1) = \frac{1}{n} + \frac{1}{n-1} + \cdots + 1 + \psi(1) \tag*{}
$$
This equivalents to:
$$
\boxed{\psi(n+1) = H_{n} + \psi(1)} \tag{2}
$$

Applying [[Stirling’s formula]] to **log-gamma function** $\ln \Gamma(n)$:
$$
\ln \Gamma(n) \operatorname*{\sim}_{n\to\infty} \left( n+\frac{1}{2} \right)\ln n + \frac{1}{2} \ln n - n \tag*{}
$$
From this approximation, the **asymptotic behavior** of $\psi(n)$ follows:
$$\begin{align*}
\psi(n) &\operatorname*{\sim}_{n\to\infty} \ln n + \frac{1}{2n} \\ 
&\operatorname*{\sim}_{n\to\infty} \ln n
\end{align*} \tag*{}$$
Then taking the limit as $n$ approaches to infinity, we get:
$$
\lim_{ n \to \infty } \psi (n) = \lim_{ n \to \infty } \ln n  \tag{3}
$$
From $(2)$ and $(3)$, we have the popular [[Euler–Mascheroni Constant]]:
$$
\boxed{\gamma = \lim_{ n \to \infty } (H_{n} - \ln n)} \tag*{}
$$
The same way we did for $(2)$ from $(1)$:
$$
\psi(z+n) = \frac{1}{z+n} + \frac{1}{z+n-1} + \cdots + \frac{1}{z} + \psi(x) \tag{4}
$$
Substracting $(4)$ from $(2)$:
$$
\psi(z+n) - \psi(n+1) = \sum_{k=0}^{n-1} \left(\frac{1}{z+k} - \frac{1}{k+1}\right) + \gamma + \psi(z) \tag{5}
$$
By doing the same with $(3)$ for $\psi(z+n)$:
$$
\lim_{ n \to \infty } (\psi(z+n) - \psi(n+1)) = 0 \tag*{}
$$
Taking the limit both sides of eq $(5)$ to obtain:
$$\boxed{\psi(z) = -\sum_{k=0}^{\infty} \left(\frac{1}{z+k} - \frac{1}{k+1}\right) - \gamma} \tag{6}$$
Thanks to $(6)$ [[Trigamma Function]] a.k.a $\psi'(x)$ can be defined as:
$$\boxed{\psi'(z) = \sum_{k=0}^{\infty} \frac{1}{(z+k)^2}} \tag{7}$$
Putting $z=1$ to $(7)$:
$$\psi'(1) = \zeta(2) = \frac{\pi^2}{6} \tag*{}$$
Where $\zeta(z)$ is [[Riemann Zeta Function]].
