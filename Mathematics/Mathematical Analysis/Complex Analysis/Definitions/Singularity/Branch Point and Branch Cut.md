---
tags:
  - Complex-Analysis
  - Mathematical-Analysis
---
# The Complex Logarithm
---
Recall that $\log$ is the **unique function** with the property that 
$$
\begin{aligned}
x = \log e^x = e^{\log x}
\end{aligned}
$$In other words, it is the inverse to $e^x$. First, note that the logarithm exists because $e^x$ is a **bijection** $\mathbb R \to (0,\infty)$, or in other words, for each and every $y \in (0,\infty)$, there exists a unique $x \in \mathbb R$ such that $y = e^x$. It follows that $\log(y) = x$.

The **complex exponential function** is a bit less straightforward. We know that there is a polar coordinate parametrization of $\mathbb C \setminus \{0\}$ given by the map $(0, \infty) \times [0, 2\pi) \to \mathbb C \setminus \{0\}$ defined by$(r, \theta) \mapsto re^{i\theta}$. As this is a parametrization, it is a bijection and therefore has a well-defined inverse $z\mapsto (|z|, \operatorname{arg} z)$, where by "$\operatorname{arg} z$" I just mean the unique angle $\theta \in [0, 2\pi)$ that $z$ makes with the $+\operatorname{Re}$ axis. However, we could have instead defined a parametrization  $(0, \infty) \times [2\pi, 4\pi) \to \mathbb C \setminus \{0\}$ or a parametrization $(0, \infty) \times [-\pi, \pi) \to \mathbb C \setminus \{0\}$, or any other conceivable way to parametrize the complex plane with polar coordinates. If $\theta \in [2\pi, 4\pi)$ and $\phi \in [-\pi, \pi)$, then $(r, \theta)$ and $(r, \phi)$ will represent the same complex number if $\theta - \phi = 2\pi n$ for some $n \in \mathbb Z$. In other words, if $\theta - \phi = 2\pi n$, then $re^{i\theta} = re^{i\phi}$.

Here's the punchline. Let $z = re^{i\theta} = re^{i\phi}$. Does $\log z = \log r + i\theta$ or does $\log z = \log r + i\phi$? The fact that $e^{i\theta} = e^{i\phi}$ entails that $z\mapsto e^z$ is *not* an injective function $\mathbb C \to \mathbb C$, and therefore not exactly **invertible** on $\mathbb C$. However, we may still define a *right inverse* to $e^z$ by making some choices. Define the map $\operatorname{Log}$ by $\operatorname{Log(z)} = \log r + i\theta$ where $z = re^{i\theta}$ for $r > 0$ and $\theta \in (-\pi, \pi)$. Because the **polar coordinate representation** is unique, $\operatorname{Log}$ is well-defined. By picking different intervals of width $2\pi$ for $\theta$ we may obtain different (but valid) logarithms. We call $\operatorname{Log}$ with $\theta \in (-\pi, \pi)$ the *principal branch logarithm*.
# Continuity and Branches
---
The careful reader may notice that because complex numbers with $\arg z = \pi$ are not accounted for in the definition of the principal branch logarithm, the definition of $\operatorname{Log}$ is valid only on the set $G:=\mathbb C \setminus (-\infty, 0]$. This is the complex plane with a "slit" cut out of it on the non-positive real axis. We could have defined the principal branch logarithm on $\mathbb C - \{0\}$, but that would lead to an issue: $\operatorname{Log}$ would not be continuous. To see why, let us compute some limits.
![[LogLimit.excalidraw|500|center]]
Approaching $-1$ from the imaginary positive axis, we have $$\lim_{n\to\infty} \operatorname{Log}(-1 + i/n)$$ and approaching $-1$ from the imaginary negative axis, we have $$\lim_{n\to\infty} \operatorname{Log} (-1 - i/n).$$ Intuitively, because our angles are restricted to the interval $(-\pi, \pi)$, the first limit will give us $\pi$ and the second limit will give us $-\pi$. This shows that $\operatorname{Log}$ cannot be continuous defined at $-1$. By similar reasoning, the principal branch logarithm cannot be continuous defined anywhere on the negative real axis.
## Definition of a branch
---
A $branch$ of the logarithm is a choice of open set $G$ and continuous right inverse to $e^z$ defined on $G$. For the principal branch logarithm, $G = \mathbb C - [0, \infty)$. Of course, because $e^z \neq 0$ for all $z \in \mathbb C$, there is no branch of the logarithm which is defined at $0$. We call such a point a *branch point*. There is no branch of the logarithm defined on all of $\mathbb C -\{0\}$ either. Intuitively, if we had such a function, we could arrive at a discontinuity by "winding around" the origin until we hit a complex number $z$ with $\arg(z) = \theta$ where $\operatorname{Im}\log (z)$ "jumps" from $\theta$ to $\theta - 2\pi$, just as we had the "jump" from $\pi$ to $-\pi$ when traversing the negative real axis with the principal branch logarithm.