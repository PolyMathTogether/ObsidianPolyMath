
# Trigno functions
---
1. $\int \sec^nx \, dx$
   $$\begin{align*}
I(n) &= \int \sec^n(x) \, dx \\ \\
&= \int \sec^2 x \sec^{n-2}x \, dx \\ \\
&= I(n-2) + \int \tan^2 x \sec^{n-2} x \, dx \\ \\
&= I(n-2) + \frac{\tan x \sec^{n-2} x}{n-2} - \frac{1}{n-2} \int \sec^{n-2} \, d\tan x \\ \\ 
I(n) &= \frac{\tan x \sec^{n-2} x}{n-1} + \frac{n-2}{n-1}I(n-2)
\end{align*}$$
2. $\int \frac{1}{1+\sec x} \, dx$
   $$\begin{align*}
\int \frac{1}{1+\sec x} \, dx &= \int \frac{2\cos^2t-1}{\cos^2t} \, dt \\ \\
&= \int (2- \sec^2t) \, dt \\ \\
&= 2t - \tan(t) + C \\ \\
&= x - \tan \frac{x}{2} + C
\end{align*}$$
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
2. $\int \left(\sqrt{ a^2 + x^2 }\right)^n \, dx$
   $$\begin{align*}
\int \left(\sqrt{ a^2 + x^2 }\right)^n \, dx  = a^{n+2}\int \sec^{n+2}(t) \, dt 
\end{align*}$$
3. $\int x^2\sqrt{ a^2+x^2 } \, dx$