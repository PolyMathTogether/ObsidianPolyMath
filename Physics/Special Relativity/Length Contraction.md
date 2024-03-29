$\quad$The second phenomenon covered is Length Contraction. In a frame of reference in which an object is stationary, its length is longer than its length in a frame of reference in which it is in motion.
$\quad$Similar to Time Dilation, we will be using a light clock. However, the light clock will be horizontal this time, and the detector will be on the same side of the emitter, thus requiring the light to reflect off from the other end back into the detector.
$\quad$I am not going to bother drawing a rocket.

![[Fig 03.01 Horizontal Light Clock|25%|center]]

$\quad$Again, the coordinate in the light clock's frame will be the primed coordinate $(t',x',y',z')$. The length of the light clock in its own frame will therefore be $L'$. We'll call the event when the light hits the other end and bounces back Event A, and when it returns Event B. The interval between the start and Event A is $t'_A$, and between Event A and B is $t'_B$.

![[Fig 03.02 Light Clock's Frame|50%|center]]

$\quad$Clearly in this frame of reference, $t'_A = t'_B = \frac{L'}{c}$ and the total time is $t' = \frac{2L'}{c}$. Onto the earth's frame of reference, which is slightly less trivial.
$\quad$In the earth's frame of reference, the interval between the start and Event A is going to be longer than $\frac{L}{c}$, as the end of the light clock is also moving away at the speed $v$.

![[Fig 03.03 Earth's Frame A|200%|center]]

$\quad$Once the light has reached the end of the light clock, it has traveled a total distance of $L + vt_A$; $L$ being from the length of the light clock itself, and $vt_A$ from the light clock's edge moving away. So, $t_A$ can be found from the equation:
$$
\begin{aligned}
ct_A &= L + vt_A\\
t_A(c-v)&=L\\
t_A &= \frac{L}{c-v}
\end{aligned}
$$
$\quad$For $t_B$, the interval will instead be shorter, as the end of the light clock is now traveling towards the light beam, making the distance needed to be traveled by the light shorter.

![[Fig 03.04 Earth's Frame B|200%|center]]

$\quad$Once it hits the end of the light clock, the beam's return trip will have the distance of $L - vt_B$. Of course, we will now find $t_B$ from the equation:
$$
\begin{aligned}
ct_B &= L - vt_B\\
t_B &= \frac{L}{c+v}
\end{aligned}
$$
$\quad$This makes the total time elapsed be
$$
\begin{aligned}
t &= t_A + t_B\\
&= \frac{L}{c-v}+\frac{L}{c+v}\\
&= L\left(\frac{1}{c-v} + \frac{1}{c+v}\right)\\
&= L\left(\frac{(c+v)+(c-v)}{(c-v)(c+v)}\right)\\
&=L\left(\frac{2c}{c^2-v^2}\right)\\
&=\frac{2L}{c}\left(\frac{1}{1-(\frac{v}{c})^2}\right)\\
&=\frac{2L}{c}\gamma^2
\end{aligned}
$$
$\quad$And from the previous chapter, the relation between time elapsed in each frames is $t = \gamma t'$, thus we end up with the equation:
$$
\begin{aligned}
t &= \gamma t'\\
\left(\frac{2L}{c} \gamma ^2\right) &= \gamma \left(\frac{2L'}{c}\right)\\
L \gamma &= L'\\
L &= \frac{L'}{\gamma}
\end{aligned}
$$
$\quad$Which is the relation between the lengths in the two frames of reference.
$\quad$So, an object whose length while stationary is $L'$ will be contracted as its velocity approaches that of the speed of light. Note that this "object" does not necessarily be an actual object; the distance between two points is also contracted in a frame of reference of high velocity.