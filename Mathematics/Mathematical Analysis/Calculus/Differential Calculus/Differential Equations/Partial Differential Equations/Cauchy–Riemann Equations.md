---
tags:
  - "#PDE"
  - "#Differential-Equations"
  - "#Differential-Calculus"
  - "#Calculus"
---


Cauchy-Riemann equations are *necessary and sufficient condition* for a function $f(z)$ to be *complex differentiable*:
$$\frac{\partial u}{\partial x} = \frac{\partial v}{\partial y}$$
and
$$\frac{\partial v}{\partial x} = - \frac{\partial u}{\partial y}$$
where $f(z) = u(x,y) + iv(x,y)$ with $u: \mathcal{R}^2 \to \mathcal{R}$ and $v: \mathcal{R}^2 \to \mathcal{R}$.

---
## <u>Proof</u>:
If $f(z)$ is differentiable at $z_0$ then
$$
f'(z_0) = \lim_{z \to z_0} \frac{f(z) - f(z_0)}{z-z_0}
$$
must exist. By replacing $f(z) = u(x,y) + iv(x,y)$ we have:

$$
\frac{f(z) - f(z_0)}{z-z_0}
$$
$$= \frac{u(x, y) - u(x_0, y_0)}{z-z_{0}} + i \frac{v(x, y) - v(x_0, y_0)}{z-z_{0}}$$
case 1: $z-z_0 \in \mathcal{R}$
$$f'(z) = \frac{\partial u(x,y) } { \partial x} + i \frac{\partial v(x,y) } { \partial x} \hspace{3em}(1)$$
case 2: $z-z_0 \in \mathcal{I}$
$$f'(z) = -i \frac{\partial u(x,y) } { \partial y} + \frac{\partial v(x,y) } {\partial y} \hspace{3em}(2)$$
From $(1)$ and $(2)$:
$$\begin{align}
\frac{\partial u(x,y) } { \partial x} + i \frac{\partial v(x,y) } { \partial x} &= -i \frac{\partial u(x,y) } { \partial y} + \frac{\partial v(x,y) } {\partial y} \hspace{3em} (*) \\ 
\leftrightarrow \frac{1}{2}\left( \frac{\partial}{\partial x} + i \frac{\partial}{\partial y} \right) &= 0 \\
\leftrightarrow \frac{\partial}{\partial \overline{z}} &= 0
\end{align}
$$
If $f'(z)$ exists then equation $(*)$ must be true so:
$$\begin{split}
\frac{\partial u}{\partial x} &= \frac{\partial v}{\partial y} \\
\frac{\partial v}{\partial x} &= - \frac{\partial u}{\partial y}
\end{split}$$