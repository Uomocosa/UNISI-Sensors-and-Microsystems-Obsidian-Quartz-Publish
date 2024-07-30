> Differently from the [[SaM - Transmission Mode for Ultrasonic Beams • C-Mode Image|transmission mode]], in "***echo mode***" measurements, ==we have a **single transducer**== which acts as a transmitter (**TX**) and also as a receiver (**RX**).
> ==This device can't act at the same time as an actuator or as a sensor, so we need to define the phase when it acts like a transmitter, and when as a receiver==.

> Let's take as example a situation like this:<br>![[Pasted image 20230720163055 1.png|500]]
> Where have three different mediums with the [[SaM - Acustic Impedance • Ultrasonic Lumped Parameter System|acustic impedance]] $Z_1$, then $Z_2$ and $Z_3$, that means that you have different velocity and/or different density.

> Here's how the echo mode works: 
> At first we have the **actuation phase** where it is used as an **actuator**/**transmitter** and we imagine to have a situation like this:<br>![[Pasted image 20230720163055 2.png|500]]<br>==Sometimes if you are lucky you have the same sound speed and different density, this is very good and we'll see how==.<br>For the graph, we place $v$ which is the propagation velocity of the wave, and as for the $x$-axis I place a timeline.
> The first excitation, ==the vibration at the beginning is strong==:<br>![[Pasted image 20230720163105 1.png|500]]<br>So what happens the wave starts, arrives here ($l_1$), some is reflected back, this echo will be then sensed by the same device that will act as a reciver (RX).
> ==The fraction which is reflected or transmitted depends on the mismatch between this impedances $Z_1$ and $Z_2$==.

> So here is the modelling of just the sensor (we ignore the TX part):<br>![[Pasted image 20230925232629.png|500]]
> - $F_{ext}$ will be very small.
> - $T_{11}$ : stress along $x_1$ applied over the surface $A_s$.
> - $A_s$ : sensor's surface.

> So after the first excitation, a time $t_1$ will pass and I will recive a new signal, the echo of the first one, and ofter another bit of time ($t_2$) I will sense a second echo, the one "returning" from the second material.<br>![[Pasted image 20230720163114.png|500]]
> The **amplitude** of the first echo depends on the difference and values of $Z_1$ and $Z_2$, the distance it needed to travel $l_1$ (due to attenuation), and the geometry or shape of the beam, simialr for the secon echo, but since it need to travel two materials, and is furter away, the amplitude and signal recived will be straight up worse.
> We can calculate $t_1$, also called **time of flight** (**TOF**), and $t_2$ using these formulas:$$\begin{array}{l}  t_1 = {2 l_1 \over v_{l_1}}  \\[3px]  t_2 = {2 l_2 \over v_{l_1}} + {2 (l_2-l_1) \over v_{l_2}}  \end{array}$$So the distances $l_1$ and $l_3$ can be evaluated if $v_1$ and $v_2$ are known.

> There is also another problem to tackle, what if the three surfaces are close:<br>![[Pasted image 20230720163131.png|500]]
> - ==The recived signal is the superpose of the two==.
> - $T_p$ pulse duration (duration of each echo), we must impose that $T_p \ll \Delta t$.
> - $\Delta t$: "time-of-flight-difference" between the second and third material.<br>You can also see it as: how far away the two echos are from each other.
> - So we have to assure that the pulse duration $T_p$ much smaller than the time-of-flight-difference between the second and third material ($\Delta t$):$$\Delta T = {2 \Delta l \over v_{l_2}}$$So, if we perform [[SaM - Echo Mode • Calculation of the Dead Zone|some calculations]] we ombtain that the $\Delta l$ must be:$$ \Delta l \gg {N \over 2} \lambda_w$$Where:
> 	- $N \in \mathbb{N}$ from $T_p = N\cdot T$, meaning:<br>"The **duration of the pulse** $(T_p)$ is a **multiple** $(N)$ of the **wave period** $(T)$"
> 	- $\lambda_w = {v_l \over f_0}$ : [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|wavelength]].
> 		- $v_l$ : [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|longitudinal propagation velocity of th wave]].
> 		- $f_0$ : [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|wave frequency]].
> 		- $f_0 = {1 \over T}$.
> - Remeber that the pulse duration must be a multiple of the period, and it cannot be shorter than one period (I send a wave $U$, it will return scaled of intensity but still similar in shape as the wave $U$), so we can write:$$T_p = N T$$Where $T = {1 \over f_0}$ is the period, and $f_0$ is the natural frequency.
> - We must have the two materials at least much more distant then ${K \over 2}\lambda_w$
> - The larger the wavelength ⇒ the larger should be $\Delta l$, so that we get **two recognizible echos**

> Also $k$ coincides with the $Q$-factor of the oscillator:$$ \Delta l \gg {Q \over 2} \lambda w $$ So the higher is the $Q$-factor, the longer will be the signal duration.
> ==So low $Q$ and short wavelength give us best performances, possible **in terms of resolution**==.
> But actually if the path is short (the signal duration), then we have a smaller energy traveling, so maybe we will have a smaller penetration depth.

> We saw that in echo mode we can arrive to measure the time of flight ($t_1$, $t_2$, $t_3$), gieven by:$$t_{TOF} = \frac{2\kern2px l}{v}$$Where: 
> - $l$ is the size of the matrial.
> - $v$ the propagation velocity of the wave.
> 
> I we know $v_l$, which depends on the material $c_{11}$ and $\rho$, or $l$ we can find the other values:<br>![[Pasted image 20230720165403.png|500]]

> Finally **US** (Ultrasonic) devices can be used for:<br>![[Pasted image 20230926120859.png]]
> - The last example is: "***Parking assistance systems***, *when you are in an automotive, to understand the distance of an obstacle to be alerted by an alarm*"

---
###### Memory Card
![[Samsung_SaM_Notes_19_240515_191312_1.jpg]]

---