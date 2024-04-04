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
\psi (z) = \frac{d}{dz} \ln \Gamma (z) = \frac{\Gamma'(z)}{\Gamma(z)}
$$
**Digamma function** is also [[Holomorphic]] on $\mathbb{C}/\mathcal{Z}_{\leq 0}$ with simple poles where $z$ is **non-positive integer**.

# Properties
---
Using $\Gamma(z+1) = z\Gamma(z)$ we can derive a fundamental property for **digamma function**:
$$
\begin{align*}
\Gamma(z+1) &= z\Gamma(z) \, ,\\
\ln \Gamma(z+1) &= \ln z + \ln \Gamma(z) \\
\end{align*}
$$
Finally, **differentiate** both sides we get:
$$
\boxed{\psi (z+1) = \frac{1}{z} + \psi (z)} \hspace{3em} (1)
$$

By using the **recurrence relation** $(1)$ for $z = n \in \mathbb{Z}^{0+}$ we can get a relation with [[Harmonic Series]]:
$$
\psi (n+1) = \frac{1}{n} + \frac{1}{n-1} + \cdots + 1 + \psi(1) 
$$
This equivalents to:
$$
\boxed{\psi(n+1) = H_{n} + \psi(1)} \hspace{3em} (2)
$$

Applying [[Stirling’s formula]] to **log-gamma function** $\ln \Gamma(n)$:
$$
\ln \Gamma(n) \operatorname*{\sim}_{n\to\infty} \left( n+\frac{1}{2} \right)\ln n + \frac{1}{2} \ln n - n \\
$$
From this approximation, the **asymptotic behavior** of $\psi(n)$ follows:
$$\begin{align*}
\psi(n) &\operatorname*{\sim}_{n\to\infty} \ln n + \frac{1}{2n} \\ 
&\operatorname*{\sim}_{n\to\infty} \ln n
\end{align*}$$
Then taking the limit as $n$ approaches to infinity, we get:
$$
\lim_{ n \to \infty } \psi (n) = \lim_{ n \to \infty } \ln n  \hspace{3em} (3)
$$
From $(2), (3)$, we have the popular [[Euler–Mascheroni Constant]]:
$$
\boxed{\gamma = \lim_{ n \to \infty } (H_{n} - \ln n)}
$$