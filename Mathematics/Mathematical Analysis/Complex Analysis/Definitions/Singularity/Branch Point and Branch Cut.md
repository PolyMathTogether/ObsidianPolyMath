---
tags:
  - Complex-Analysis
  - Mathematical-Analysis
---
## The complex logarithm
Recall that $\log$ is the unique function with the property that $\log{e^x} = x = e^{\log x}$. In other words, it is the inverse to $e^x$. First, note that the logarithm exists because $e^x$ is a bijection $\mathbb R \to (0,\infty)$, or in other words, for each and every $y \in (0,\infty)$, there exists a unique $x \in \mathbb R$ such that $y = e^x$. It follows that $\log(y) = x$.

The complex exponential function is a bit less straightforward. We know that there is a polar coordinate parametrization of $\mathbb C - \{0\}$ given by the map $(0, \infty) \times [0, 2\pi) \to \mathbb C - \{0\}$ defined by$(r, \theta) \mapsto re^{i\theta}$. As this is a parametrization, it is a bijection and therefore has a well-defined inverse $z\mapsto (|z|, \operatorname{arg} z)$, where by "$\operatorname{arg} z$" I just mean the unique angle $\theta \in [0, 2\pi)$ that $z$ makes with the $+\operatorname{Re}$ axis. However, we could have instead defined a parametrization  $(0, \infty) \times [2\pi, 4\pi) \to \mathbb C - \{0\}$ or a parametrization $(0, \infty) \times [-\pi, \pi) \to \mathbb C - \{0\}$, or any other conceivable way to parametrize the complex plane with polar coordinates. If $\theta \in [2\pi, 4\pi)$ and $\phi \in [-\pi, \pi)$, then $(r, \theta)$ and $(r, \phi)$ will represent the same complex number if $\theta - \phi = 2\pi n$ for some $n \in \mathbb Z$. In other words, if $\theta - \phi = 2\pi n$, then $re^{i\theta} = re^{i\phi}$.

Here's the punchline. Let $z = re^{i\theta} = re^{i\phi}$. Does $\log z = \log r + i\theta$ or does $\log z = \log r + i\phi$?