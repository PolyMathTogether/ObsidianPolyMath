$\quad$Let us consider a light clock: an object that keeps track of events by shooting a beam of light from one end and detect it at the other. If the clock is stationary, obviously the time measured between the emission and the detection will be $t = \frac{L}{c}$, where $L$ is the length of the light clock.

![[Fig 02.01 Light Clock|center]]

$\quad$Behold a beautifully-drawn spaceship fitted with a vertical light clock moving at constant velocity $v$, and earth. We shall call the coordinates in the earth's frame of reference the unprimed coordinates: $(t, x, y, z)$, and the spaceship's frame will have the primed coordinates: $(t', x', y', z')$. In this section of time dilation, only the time coordinate needs to be considered.

![[Fig 02.02 Rocket and Earth|25%|center]]
$\quad$Event A is the emission of light in the light clock, and is the moment the origin of both frames of reference line up. We will let the time in both frames of reference be $0$ at this instant. Event B shall be the detection of the light beam, and the time of Event B on earth's frame of reference and the rocket's frame of reference shall be $t$ and $t'$ respectively. This means, the interval between Event A and Event B is $t$ in earth's frame and $t'$ in the rocket's frame.
$\quad$First, we shall find $t'$. Because the rocket houses the light clock, it is stationary in this frame of reference. This means the interval between the emission and detection of light is $t' = \frac{L}{c}$, as previously stated.

![[Fig 02.03 Rocket's Frame|center]]

$\quad$Then, let us find $t$. In the earth's frame of reference, the light beam moves upwards and alongside the rocket, i.e. its trajectory is diagonal in this frame of reference, as opposed to solely vertical.

![[Fig 02.04 Earth's Frame|200%|center]]

$\quad$You can notice the time between Event A and Event B in this frame of reference is longer, as the path the light has traveled is longer while the speed of light remained the same. We can find how much longer it is by using the Pythagorean theorem to find the path length.

![[Fig 02.05 Pythagorean|center]]
$\quad$The path length is $ct$, as $t$ is the time between the events. We can therefore make the following equation to find $t$.
$$
(ct)^2 = (vt)^2 + L^2
$$
$\quad$By solving the equation:
$$
\begin{align*}
c^2t^2 - v^2t^2 &= L^2\\
t^2(c^2-v^2) &= L^2\\
t\sqrt{c^2-v^2} &= L\\
t &= \frac{L}{\sqrt{c^2-v^2}}\\
t &= \frac{L}{c}\frac{1}{\sqrt{1-\frac{v^2}{c^2}}}
\end{align*}
$$
$\quad$We now know the interval between A and B in the earth's frame of reference. The interval between those same events in the rocket's frame of reference is $t'$, which is equal to $\frac{L}{c}$. We can therefore find the relation between the intervals in each frame:
$$
t = t'\frac{1}{\sqrt{1-\frac{v^2}{c^2}}}
$$
$\quad$The factor multiplying $t'$ is a factor we will get to see often in the upcoming sections, and this factor is called the Lorentz Factor. To keep the equation brief, define $\gamma$ to be the Lorentz factor:
$$
\gamma = \frac{1}{\sqrt{1-\frac{v^2}{c^2}}}
$$
$\quad$And so the final relation between the time passed in one frame of reference and the other is
$$
t = \gamma t'
$$
$\quad$In conclusion, when a frame of reference is moving at a speed close to the speed of light relative to us, more time will pass in our frame than in the moving frame. So, the other frame will appear to have "slowed down". However, do note that the moving frame of reference will also see us moving, hence both frames of reference will see the other frame is in slow-motion. This does not cause any paradox because the time will sync up if the two frames change directions to meet each other again.
$\quad$Let's have an example which will solidify our understanding.
$\quad$A particle starts traveling from earth at the constant velocity of $0.5c$ towards a planet $10$ lightyears away from earth. How long does the particle take to travel to the planet in $a)$ The earth's frame of reference and $b)$ The particle's frame of reference?

![[Fig 02.06 Example|center]]

$\quad$The answer for the earth's frame of reference is trivial; it takes light 10 years to reach the other planet, so it would take the particle 20 years to reach it. For the particle, we shall first find its Lorentz Factor $\gamma$:
$$
\begin{aligned}
\gamma &= \frac{1}{\sqrt{1-\frac{v}{c}^2}}\\
&= \frac{1}{\sqrt{1-(\frac{1}{2})^2}}\\
&= \frac{2}{\sqrt{3}}
\end{aligned}
$$
$\quad$With the relationship between the time elapsed in earth's frame $t$ and in the particle's frame $t'$ being
$$
\begin{aligned}
t &= \gamma t'\\
t' &= \frac{t}{\gamma}\\
&= \frac{(20)}{(\frac{2}{\sqrt{3}})} \approx 17.32..
\end{aligned}
$$
$\quad$Thus, approximately $17.32$ years will have passed for the particle upon its arrival on the planet. As the velocity approaches the speed of light, the difference in time grows more extreme. For example, if the particle was traveling at $0.99c$ instead, the time passed will be approximately $2.82$ years.
