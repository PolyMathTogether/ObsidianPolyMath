Just like the [[Derivative]] is used to analyze the **behavior** and **properties** of **functions of single variable**, it can also be applied to [[Multivariate Function]] to achieve the same purpose.

# Definition
---
Let $U$ be an [[Open Set]] and a **subset** of $\mathbb{R}^{n}$ and a **multivariate function** $f\,\colon \, U \mapsto \mathbb{R}$. Then the **partial derivative** of $f$ at the point $\mathbf{a} = (a_{1}, a_{2}, \dots, a_{n})$ with respect to the $i$-th variable $x_i$ is defined as
$$
\frac{\partial}{\partial x_{i}} f(\mathbf{a}) = \lim_{ h \to 0 } \frac{f(\mathbf{a}+h \hat{\mathbf{e}}_{i}) - f(\mathbf{a})}{h}
$$
when the limit exists. Where $\hat{\mathbf{e}}_{i}$ is the **unit vector** of $i$-th variable $x_{i}$.

# Notation
---
**Partital derivative** with respect to $x$ can be denoted as $\frac{\partial f}{\partial x}$ or $f_{x}'$ or $\partial_{x}f$.