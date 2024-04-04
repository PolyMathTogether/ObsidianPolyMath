
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
\int \sqrt{ a^2 + x^2 } \, dx &= a^2\int \sec^2(t)\sqrt{ 1+\tan^2(t) } \,  dt \hspace{3em} (x=a\tan t)\\ \\
&= a^2 \int \sec^3(t) \, dt \\ \\
&= a^2 \int \sec(t) \, dt + a^2 \int \tan^2(t) \sec(t) \, dx \\ \\
&= a^2 \ln\left|\tan(t) + \sec(t)\right| + a^2 \tan(t)\sec(t) - a^2\int \sec^3(t) \, dt \\ \\
\int \sqrt{ a^2 + x^2 } \, dx &= \frac{a^2}{2}\left(\ln\left|\tan(t) + \sec(t)\right| + \tan(t)\sec(t)\right) + C \\ \\
&= \frac{a^2}{2} \left( \ln\left| \frac{x}{a} + \sqrt{ \left( \frac{x}{a} \right)^2 +1 }\right| + \frac{x}{a}\sqrt{ \left( \frac{x}{a} \right)^2+1 } \right) + C
\end{align*}$$
2. $\int \left(\sqrt{ a^2 + x^2 }\right)^n \, dx$
   $$\begin{align*}
\int \left(\sqrt{ a^2 + x^2 }\right)^n \, dx  = a^{n+1}\int \sec^{n+2}(t) \, dt 
\end{align*}$$
3. $\int x^2\sqrt{ a^2+x^2 } \, dx$
   $$\begin{align*}
\int x^2\sqrt{ a^2+x^2 } \, dx &= a^6 \int \tan^2t\sec^3t \, dt \\ \\
&=a^6\left(\int \sec^3t \, dt -  \int \sec^5t \, dt  \right)
\end{align*}$$
4. $\int \frac{1}{\sqrt{ x^2+a^2 }} \, dx$
   $$\begin{align*}
\int \frac{1}{\sqrt{ x^2+a^2 }} \, dx &= \int \frac{\cosh t}{\cosh t} \, dt \hspace{3em} (x=a\sinh t)\\ \\
&= t + C \\ \\
&= \sinh^{-1} \frac{x}{a} + C
\end{align*}$$
5. $\int \frac{1}{x\sqrt{ x^2+a^2 }} \, dx$
   $$\begin{align*}
\int \frac{1}{x\sqrt{ x^2+a^2 }} \, dx &= \frac{1}{a}\int \frac{a}{x^2\sqrt{ 1+\left( \frac{a}{x} \right)^2 }} \, dx \hspace{3em}  \\ \\
&= -\frac{1}{a}\int \frac{1}{\sqrt{ 1+t^2 }} \, dt \left( t=\frac{a}{x} \right)\\ \\
&= - \frac{1}{a} \sinh^{-1}t + C \\ \\
&= - \frac{1}{a} \sinh^{-1} \frac{a}{x} + C
\end{align*}
   $$
6. $\int \frac{1}{x\sqrt{ x^4 +1}} \, dx$
   $$\begin{align*}
\int \frac{1}{x\sqrt{ x^4 - 1}} \, dx &= \int \frac{1}{t\sqrt{ t^2 -1}} \, dt  \hspace{3em} (t=x^2) \\ \\
&= \int \frac{\tan u \sec u}{\tan u \sec u} \, du \hspace{3em} (t=\sec u) \\ \\
&= u + C \\ \\
&= \sec^{-1}x^2 + C 
\end{align*}$$ 
# Logarithm functions
---
   1. $\int \log x \, dx$
      $$\begin{align*}
\int \log x \, dx = x\log x -x + C
\end{align*}$$
2. $\int x\log x \, dx$
   $$\begin{align*}
\int x\log x \, dx = \frac{1}{4}\int \log t \, dt \hspace{3em} (t=x^2) 
\end{align*}$$
3. $\int x^n\log x \, dx$
   $$\begin{align*}
\int x^n\log x \, dx = \frac{1}{(n+1)^2}\int \log t \, dt \hspace{3em}(t=x^{n+1}) 
\end{align*}$$
4. $\int \log^2 x \, dx$
   $$\begin{align*}
\int \log^2 x \, dx &= \int t^2e^t \, dt \hspace{3em} (t=\log x) \\ \\
&= t^2e^t - 2te^t + 2\int e^t \, dt \\ \\
&= x\log^2 x - 2x\log x+2x + C
\end{align*}$$
5. $\int \log^nx \, dx$
   $$\begin{align*}
I(n) &= \int \log^nx \, dx \\ \\ 
&= \int t^ne^t \, dt \hspace{3em} (t=\log x) \\ \\ 
&= t^ne^t - nI(n-1) \\ \\
&= x\log^nx - nI(n-1)
\end{align*}$$
6. $\int \frac{1}{\log x} \, dx$
   $$\begin{align*}
\int \frac{1}{\log x} \, dx &= \int \frac{e^t}{t} \, dt  \hspace{3em} (t = \log x) \\ \\
&= \int \sum_{n=0}^{\infty} \frac{t^{n-1}}{n!} \, dt \, dx \\ \\
&= \ln t + \sum_{n=1}^{\infty} \frac{1}{n}\frac{t^n}{n!} + C   \hspace{3em} = e^t \sum_{n=1}^{\infty} \frac{(n-1)!}{t^n} + C\\ \\
&= \ln \ln x + \sum_{n=1}^{\infty} \frac{1}{n}\frac{\log^n x}{n!} + C \\ \\
&= x \sum_{n=1}^{\infty} \frac{(n-1)!}{\log^nx} + C
\end{align*}$$
# Trigno function
---
1. $\int e^x \cos x \, dx$
   $$\begin{align*}
\int e^x \cos x \, dx &= Re\int e^x e^{ix} \, dx \\ \\
&= Re \left( \frac{1}{i+1}e^{x(i+1)} \right) + C \\ \\
&=  \frac{e^x}{2} Re((1-i)e^{ix}) + C \\ \\
&= e^x\frac{\cos x+ \sin x}{2} + C
\end{align*}$$
