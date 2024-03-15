# Open Cover
---
- $T \subset \mathcal{R}$
- $A$ is a set, $U_{\alpha}$ is [[Open Set]] for every $\alpha \in A$
$$T \subset \bigcup_{\alpha \in A} U_{\alpha} $$
- Then $\{ U_{\alpha}: \alpha \in A\}$ is known as _open cover_ of $T$.

## Example
---
- $T = (0,1)$
- $A = \{3,4,5, \, \cdots \}$
- $U_n = \left( \frac{1}{n}, \frac{n-1}{n} \right)$
  
$$
T \subset \bigcup_{n \in A} U_{n}
$$
$$
\leftrightarrow T \subset \left( \frac{1}{3}, \frac{2}{3} \right) \cup \left( \frac{1}{4}, \frac{3}{4} \right) \cup \left( \frac{1}{5}, \frac{4}{5} \right) \cup \, \cdots
$$
- Then $\{U_{n}: n \in A\}$ is _open cover_ of $(0,1)$.

# Subcover
---
- $\{U_{\alpha}: \alpha \in A\}$ is _open cover_ of $T \subset \mathcal{R}$
- $B \subset A$
$$T \subset \bigcup_{\beta \in B} U_{\beta} $$
- Then $\{U_{\beta}: \beta \in B\}$ is _subcover_ of $\{ U_{\alpha}: \alpha \in A\}$

## Finite Subcover
---
- If $B$ is _finite_[^1] then $\{U_{\beta}: \beta \in B\}$ is _finite subcover_ of $\{ U_{\alpha}: \alpha \in A\}$

> Proof: the open cover of $(0,1)$ from above example does not have a finite subcover.
#### <u>Solution</u>

> [!success] Proof
> $B = \{a, a + 1, \cdots, b\} \subset A$
$\to V_{a,b} = \bigcup\limits_{n\in B} U_{n} \subset \bigcup_{n \in A} U_{n} = (0,1)$
> As a result, $T \not\subset V_{a,b}$ then $\{U_{n}: n \in B\}$ is not subcover of $\{ U_{\alpha}: \alpha \in A\}$

# Compact Set
---
We say a set $K \subset \mathcal{R}$ is _compact_ if every _open cover_ of $K$ has a _finite sub cover_.

[^1]: Finite set has a finite number of members. i.e. $\{1,2,3\}$