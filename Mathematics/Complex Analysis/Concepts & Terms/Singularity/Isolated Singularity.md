# Definition
---
If complex function $f(z)$ with [[Singularity]] $c$ is [[Holomorphic]] on $\mathcal{U} \setminus \{c\}$, then $c$ is known as *isolated singularity* of $f$. Where $\mathcal{U} \in \mathcal{C}$ is an [[Open Set]].

# Examples
---
- $0$ is isolated singularity/simple pole of function $\frac{1}{z}$
- Every $z = k \in Z$ is an isolated singularity of function $\frac{1}{\sin (\pi z)}$

# Residue Calculation
---
## Simple pole
If $c$ is a simple [[Pole]] (pole with order of $1$) of $f(z) = \frac{g(z)}{h(z)}$ then:
$$
Res(f, c) = \lim_{ z \to c } \,(z-c) \, f(z) \\
=\frac{g(z)}{h'(z)}
$$
## Higher order pole
If $c$ is a pole with order of $n$ then:
$$Res(f, c) = \lim_{ z \to c } \frac{d^{n-1}}{dz^{n-1} }[(z-c)^{n}f(z)]$$