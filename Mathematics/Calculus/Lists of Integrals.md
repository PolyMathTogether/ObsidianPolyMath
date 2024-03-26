# Irrational functions
---
1. $\int \sqrt{ a^2 + x^2 } \, dx$
   $$\begin{align*}
\int \sqrt{ a^2 + x^2 } \, dx &= a^2\int \sec^2(t)\sqrt{ 1+\tan^2(t) } \,  dt \\ \\
&= a^2 \int \sec^3(t) \, dt \\ \\
&= a^2 \int \sec(t) \, dt + a^2 \int \tan^2(t) \sec(t) \, dx \\ \\
&= a^2 \ln\left|\tan(t) + \sec(t)\right| + a^2 \tan(t)\sec(t) - a^2\int \sec^3(t) \, dt \\ \\
\int \sqrt{ a^2 + x^2 } \, dx &= \frac{a^2}{2}\left(\ln\left|\tan(t) + \sec(t)\right| + \tan(t)\sec(t)\right) + C \\ \\
&= \frac{a^2}{2} \left( \ln\left| \frac{x}{a} + \sqrt{ \left( \frac{x}{a} \right)^2 +1 }\right| + \frac{x}{a}\sqrt{ \left( \frac{x}{a} \right)^2+1 } \right) + C
\end{align*}$$ 