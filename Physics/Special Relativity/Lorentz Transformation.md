$\quad$The combination of the three phenomena is going to be used to formulate the general coordinate transformation between two inertial frames of reference.
$\quad$We shall consider two frames of reference, $S$ and $S'$. The origin of $S'$ is in motion at a constant velocity of $v$ in the $S$ frame of reference, in the $+x$ direction. Let's say there exists an arbitrary event $E$. We are going to find that, for a given time and location in one frame of reference, when and where does event $E$ occur in the other frame.
$\quad$To formalize Lorentz Transformation, we will define an event $E_{0}$ which will serve as our reference point. Event $E_0$ occurs at the origin when both frames of reference overlap, meaning $x = 0$ and $x' = 0$ both refer to the same point. We shall let the moment $E_0$ occurs be $t = t' = 0$. We can write $E_0$'s coordinate as $E_0(0,0,0,0)$ in both frames.

![[Fig 05.01 E0 Coordinates|center]]
$\quad$In a similar fashion, we shall write the coordinates of event $E$ as $E(ct,x,y,z)$ and $E(ct',x',y',z')$ for the $S$ and $S'$ frame of reference, respectively. Note the usage of $ct$ instead of $t$, this is for the sake of unit consistency.

![[Fig 05.02 E Coordinates|center]]

$\quad$Firstly, acknowledge that time dilation is used to find the time delay between two events which occur at a different time, but at the same position in the primed frame of reference. On the contrary, simultaneity is used to find the time delay between two events which occur at the same point in time but at a different position in the primed frame of reference. So by introducing an intermediate event, we can find the time delay in the lab frame between two events which occur at different time and positions.
$\quad$Let $E_{1}$ be the intermediate event. It occurs at the origin of $S'$, and at the same time as $E$ in the $S'$ frame. This means the coordinate of $E_1$ in $S'$ is $(ct',0,0,0)$. The coordinate of $E_1$ in $S$ shall be $(ct_1,x_1,y_1,t_1)$. 

![[Fig 05.03 E1 Coordinates 1|center]]
$\quad$We can immediately evaluate the value of $t_1$ using time dilation on the interval between event $E_0$ to $E_1$:
$$
t_1 = \gamma t'
$$
$\quad$Because $E_1$ occurs at the origin of $S'$ frame, and $S'$ is moving at $v$ in the $+x$ direction, we easily find that:
$$
\begin{aligned}
x_1 &= vt_1\\
x_1 &= v(\gamma t')\\
\end{aligned}
$$
$\quad$So the event's coordinate in $S$ is $(c\gamma t', v \gamma t', 0 ,0)$.

![[Fig 05.04 E1 Coordinates 2|center]]
$\quad$In $S'$, $E_1$ and $E$ occurs simultaneously with the spatial difference on the $x$ axis of $x'$. From simultaneity, two events which occur simultaneously with spatial difference in $S'$ will have a time delay between them in $S$.
$\quad$In $S$, the time delay between $E_1$ and $E$ due to simultaneity is 
$$
c\Delta t = x'\beta \gamma
$$
$\quad$Where $\beta = \frac{v}{c}$. Therefore, the time at which $E$ occurs in $S$ is
$$
\begin{aligned}
ct &= c\gamma t' + c\Delta t\\
&= c\gamma t' + x' \beta \gamma\\
&= \gamma \left(ct' + \beta x'\right)
\end{aligned}
$$
$\quad$As for the position at which $E$ occurs, it is the sum of the distance $S'$ has moved, plus the distance $x'$ under length contraction. This means:
$$
\begin{aligned}
x &= (vt_1 + v\Delta t) + \frac{x'}{\gamma}\\
&=(v\gamma t' +\frac{v}{c}c\Delta t)+ \frac{x'}{\gamma}\\
&=(v\gamma t' +\frac{v}{c}x'\beta\gamma)+ \frac{x'}{\gamma}\\
&=v\gamma t' +\frac{\gamma^2 x'\beta^2 + x'}{\gamma}\\
&=\gamma\beta ct' + \frac{x'(\gamma^2\beta^2 + 1)}{\gamma}
\end{aligned}
$$
$\quad$Let's evaluate $\gamma^2\beta^2 + 1$:
$$
\begin{aligned}
\gamma^2\beta^2+1 &= \frac{1}{1-\frac{v}{c}^2}\left(\frac{v}{c}\right)^2 + 1\\
&= \frac{\frac{v}{c}^2}{1-\frac{v}{c}^2} + \frac{1-\frac{v}{c}^2}{1-\frac{v}{c}^2}\\
&= \frac{1}{1-\frac{v}{c}^2} = \gamma^2\\
\gamma^2\beta^2 +1&= \gamma^2
\end{aligned}
$$
$\quad$Back to $x$:
$$
\begin{aligned}
x &=\gamma\beta ct' + \frac{x'(\gamma^2\beta^2 + 1)}{\gamma}\\
&=\gamma\beta ct' + \frac{x'\gamma^2}{\gamma}\\
&= \gamma (\beta c t' + x')
\end{aligned}
$$

![[Fig 05.05 E Coordinates|center]]

$\quad$As for $y$ and $z$, since there is no length contraction nor motion in those axis, it is simply
$$
\begin{aligned}
y &= y'\\
z &= z'
\end{aligned}
$$
$\quad$So ultimately, for a given event $E$ which occurs at the coordinate $(ct',x',y',z')$ in the $S'$ frame, it occurs at $(\gamma (ct' + \beta x'), \gamma (x' + \beta ct') ,y', z')$ in the $S$ frame of reference.
$$
\begin{aligned}
ct &= \gamma(ct' + \beta x')\\
x &= \gamma(x' + \beta ct')\\
y &= y'\\
z &= z'
\end{aligned}
$$
$\quad$Note the symmetrical relationship between time and displacement in the Lorentz transformation equations.