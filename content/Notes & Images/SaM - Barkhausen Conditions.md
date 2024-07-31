##### ***Remeber***:

> - We have seen that for an [[SaM - Introduction to Oscillators|oscillator]] to function as such, we need to have an **divergent input-output transfer function**, even better if it is **marginally stable**, given this:$${V_o\over V_S} = {A \over 1 + \beta A}$$We need to find a solution to this equation:$$1 + \beta(j\omega)A(j\omega) = 0$$And we will have an **oscillating output**.
> - To find a solution we need to fullfill the ***Barkenhausen Conditions***, which are:$$\begin{array}{l} |\beta A | \ge 1 \\ \angle{\beta A} = 180° \end{array}$$If $|\beta A|$ is exactly $1$, we will have a **marginally stable** output, otherwise it will diverge and it will become a **square wave** form (usually, we have not seen other cases).
> - *~Ex.: Suppose you want an oscillator with oscillating frequency $\omega_0$, than you need to have the gains $\beta$ and $A$ to satisfy this condition:*<br>==*When the phase $\angle \left[\beta(j\omega_0) \cdot A(j\omega_0) \right] = 180°$ you need to have their module $|\beta(j\omega_0) \cdot A(j\omega_0)| = 1$*==.

> - The most important condition for an oscillator, is the **frequency stability**.
> - ==*That means that the two parameters: $\beta$ and $A$, which are the gain of the amplifier and the gain of the feedback network, **have to be stable in time, not changing***==.<br>==Otherwise, you will have a sine wave with the frequency which changes in time==, and this is something which, for sure, isn't good for an oscillator.
> - If $\angle\beta A$ changes (for some errors), the phase of the oscillating wave will change, **which is not good**.
> - ==So to allivieate this problem we can "take a big slope" when crossing the $-180°$ degrees line, so around $\omega_0$ (where I need to oscillate).<br>This way if the phase $\angle\beta A$ chanes, the oscillating frequency $\omega_0$ will only change a little==:<br>![[Pasted image 20230719114850 1.png|500]]

---
###### Memory Card
![[Samsung_SaM_Notes_24_240516_113108_1.jpg]]

---
![[Pasted image 20230719114757.png]]
![[Pasted image 20230921231752.png]]
- In case we have a sine wave oscillator that means that we have real part of the pole equal to zero.
- That means that there exists the solution of the equation: ...
- So you find a value $\omega_0$, which gives you the two poles.<br>⇒ Therefore, when you design a sine wave oscillator, you will start by setting a solution of this equation in the $\omega$ domain.

So we have to grant that there exists a frequency which gives you this equality here.
![[Pasted image 20230719114821.png]]
- And in order to do so, we use the so-called "***Barkhausen condition***", which are the same.
- I have, that even it is not perfectly equal to $1$, it should be a little bit larger, **not smaller**.<br>Because having this product here smaller than one, when the phase takes this value here, means having a **stable system**.<br>For an oscillator we absolutely don't want a **stable system** (otherwise the output of the system will fade)
- So this is the design condition:<br>==We need to ensure that at the frequency where the phase is equal to $180$ degrees, the module is almost $1$, or at least larger than one==.<br>If this condition is fulfilled ⇒ **the circuit will oscillate**.


Obviously, the most important condition, the most important specification for an oscillator, is the **frequency stability**.
So, quality of the oscillator comes from this parameter, which is frequency stability.
The second Barkhausen condition to be met is **stability in time**:
==*That means that, for instance, this two parameters ($\beta$ and $A$), which are the gain of the amplifier and the gain of the feedback network, **has to be stable in time, not changing***==.
Otherwise, you will have a sine wave with the frequency, which changes in time, and this is something which, for sure, isn't good for an oscillator.
So, the most important thing we have to grant is a **stability**.

![[Pasted image 20230719114850.png]]
- In normal cirucits (non-oscillators) we usually select the amplifier, so it has a constant phase in the operational range of the circuit, so that if we increase the frequency by a little the phase is still the same.
- In oscillators, we do differently, we have said that if $\angle\beta A$ changes (for some errors), the phase of the oscillating wave will change, **which is not good**.<br>==To allivieate this problem we can "take a big slope" where crossing this $-180°$ degrees line, so around $\omega_0$ (where I need to oscillate).<br>This way if the phase $\angle\beta A$ chanes, the oscillating frequency $\omega_0$ will only change a little==.

![[Pasted image 20230719114902.png]]
- Therefore a good solution will be:<br>Choose $\beta$ networks, to be **resonant circuit**, with resonance approximately on the frequency of the oscillating circuit itself ($\omega_0$). #NOT_SURE_ABOUT_THIS (What does it mean?)

---