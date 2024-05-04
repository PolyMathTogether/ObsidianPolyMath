$\quad$The next phenomenon resulting from the postulates is known as Simultaneity. Consider the following paradox:
![[Fig 04.01 Barn-Pole Paradox|50%|center]]
$\quad$A pole moves at a constant velocity into a barn, whose width is $L$. The pole's rest length is $L'$, such that its length is contracted to $L$ in the barn's frame of reference. In the barn's frame of reference, when the front end of the pole reaches the exit of the barn to the right, the back end of the pole is exactly at the entrance on the left. This means the pole fits perfectly in the barn in this frame of reference. However, in the pole's frame of reference, its length is longer than the barn's width, meaning it cannot fit into the barn. How is this possible?
$\quad$The solution to the paradox is simultaneity. In the barn's frame of reference, the event where the front end of the pole is at the exit and the event where the back end is at the entrance occurs simultaneously, making the pole fit into the barn. On the other hand, in the pole's frame of reference, these two events have a brief time interval between them, meaning the front end of the pole would have already exited the barn by the time the back end is at the entrance.

![[Fig 04.02 Barn-Pole Paradox Solution|center|200%]]

$\quad$In order to express this phenomenon mathematically, let's consider another scenario: a light clock with a detector in the middle. This light clock can emit two beams of light, both from the left edge and the right edge. The detector in the middle will only be activated if it detects the light beam from both sides at the same time.

![[Fig 04.03 Simultaneous Light Clock|50%|center]]

$\quad$Once again we will consider the two frames of reference: the frame in which the light clock is in motion with the velocity $v$ (we will call this the lab frame), and the frame in which the light clock is stationary. In the stationary frame, the light clock's length is $L'$, while in the lab frame, its length is $L$. From [[Length Contraction]], we know the relation between the lengths is $L = \frac{L'}{\gamma}$. We shall begin the thought experiment.
$\quad$In the light clock's frame, both ends of the detector are activated simultaneously. The time the light beam from each sides reach the midpoint is $t'_{A} = t'_{B} = \frac{L'}{2c}$. 
![[Fig 04.04 Light Clock Frame|50%|center]]

$\quad$In the lab frame, the light clock is in motion. The midpoint is moving towards the B emitter, meaning the distance light beam B has to travel to reach the midpoint is less than that of light beam A. This means emitter A must activate sooner than emitter B.
![[Fig 04.05 Lab Frame|center|200%]]

$\quad$The time lag between A emitter's activation and B emitter's activation shall be denoted $\Delta t$. The time light beam A and B took to hit the midpoint shall be denoted $t_{A}$ and $t_{B}$, respectively. Obviously, $t_{A} = t_{B} + \Delta t$.
$\quad$The distance A and B travelled is $L_{A}$ and $L_{B}$ respectively. The distance beam A travelled is half the length of the light clock, plus the distance the midpoint has travelled away.
$$L_{A} = \frac{L}{2} + vt_{A}$$
$\quad$And similarly, the distance beam B travelled is half the length of the light clock, subtracted by the distance the midpoint travelled towards it.
$$L_{B} = \frac{L}{2} - vt_{B}$$
$\quad$Additionally, by definition,
$$\begin{aligned}
L_{A} = ct_{A}\\
L_{B}=ct_{B}
\end{aligned}
$$
$\quad$Hence,
$$\begin{aligned}
ct_{A} &= \frac{L}{2} + vt_{A}\\
t_{A} &= \frac{L}{2(c-v)}\\
ct_{B} &= \frac{L}{2} - vt_{B}\\
t_{B} &= \frac{L}{2(c+v)}
\end{aligned}
$$
$\quad$And so, we can find the value of time lag as a result of simultaneity $\Delta t$:
$$
\begin{aligned}
\Delta t &= t_{A} - t_{B}\\
&= \frac{L}{2(c-v)} - \frac{L}{2(c+v)}\\
&= \frac{L}{2} \left( \frac{1}{c-v} - \frac{1}{c+v} \right)\\
&= \frac{L}{2} \left( \frac{(c+v)-(c-v)}{(c-v)(c+v)}\right)\\
&= \frac{L}{2} \left( \frac{2v}{(c-v)(c+v)}\right)\\
&= L \left( \frac{v}{c^2-v^2}\right)\\
&= \frac{Lv}{c^2} \left( \frac{1}{(1-\frac{v}{c}^2)}\right)\\
c\Delta t &= \beta L \gamma^2\space;\space\beta = \frac{v}{c}\\
c\Delta t &= \gamma\beta L'
\end{aligned}
$$
$\quad$To conclude, an event which occurs simultaneously in one frame of reference, but has the spatial difference of $x'$, will have the temporal difference of
$$c\Delta t = \gamma \beta x'$$
$\quad$With all three of these phenomena, we can form the ultimate transformation between two frames of reference.