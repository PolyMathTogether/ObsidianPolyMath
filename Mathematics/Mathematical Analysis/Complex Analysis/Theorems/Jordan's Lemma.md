---
tags:
  - Complex-Analysis
  - Theorems
  - Mathematical-Analysis
---

Suppose have a continuous function defined on _semicircular contour_. If the function has the form:
$$f(z) = e^{iaz}g(z)$$
Then the _lemma_ states that:
$$\left|\oint_{C_{R}}f(z)dz_{0}\right| \leq \frac{\pi}{a}M_{R} \hspace{1em} \text{where} \hspace{1em} M_{R} := \max_{\theta \in [0, \pi]} \left|g(Re^{i\theta})\right| $$

For the case $a=0$ see [[Estimation Lemma]].
![[semicicular.png]]
## Aplications
---
By _Jordan's Lemma_
$$\lim_{ R \to \infty } \left|\oint_{C_{R}}f(z)dz_{0}\right| \leq \lim_{ R \to \infty } \frac{\pi}{a}M_{R} = 0$$
Equivalently
$$\lim_{ R \to \infty }  \oint_{C_{R}}f(z)dz_{0} = 0$$