###### Memory Card
![[Samsung_SaM_Notes_23_240516_111131_1.jpg]]

---
We have seen how [[SaM - Inductive Proximity Sensor|inductive proximity sensors]] works.
Now we can go instead to the other possibility: I take into account the fact that there is **no excitation**.

Here's a **VRS** (**variable reluctance sensors**):
![[Pasted image 20230719112428 1.png|333]]
- When speaking about this usually we think to a structure where there is no external excitation.<br>⇒ So an **[[SaM - Types of Active Sensors|active sensor]]**.
- For semplicity (and also because it's a good approximation) I consider $I=0$.7

In this case we have to forget the part which depends on the current, so we will get an output voltage equal to:$$v = -N{d \over dt}\left({\text{MMF}_{eq} \over \mathcal{R}_{TOT}}\right) = N {\text{MMF}_{eq} \over \mathcal{R}^2_{TOT}}{d \mathcal{R}_{TOT} \over d t}$$Where:
- $v$ is the [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|electro-motive force]] (==this is actual voltage measured in Volts, but has sign inverted with rispect to the actual voltage drop==).
- $\text{MMF}_{eq}$ : [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|equivalent magneto motive force]].
- $\mathcal{R}_{TOT}$ : [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|total reluctance]]

And if I use a very large resistance $R_L \to \infty$, for example tanks to an amplifier, then actually I will have a very small current, and the assumption $I = 0$, is true in general.
So not only because I don't force a current, but also there is no current induced in the circuit due to the very large impedance at the sensing coil.

---
#IMPORTANTE 
So in this case to generate a voltage I need a varying reluctance, so the drawing doesn't show it but ==I need the gap length to change==.

![[Pasted image 20240115184858.png]]

---
We have also seen a variable reluctance sensor used to measure speed, or anglular speed:<br>![[Pasted image 20240215181018.png|333]]

This is its [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|lumped parameter model]]:<br>![[Pasted image 20240215181103.png|500]]

So while the *thoothed wheel* rotates this will be the plot of $v={dx \over dt}$:<br>![[Pasted image 20240215181138.png|500]]
- The **period** $T$ is given by the angular rotation between two theeth, the more theet the wheel has, the lower will be the period:$$T = {1\over \omega \cdot \#{\text{theeths}}}$$Where:
	  - $\omega$ (previously called $\omega_M$) is the **angular velocity**.
	  - $\#{\text{theeths}}$ : number of theets.
  - We need to mention that also the amplitude of the graph will scale with $\omega$, not just the period.<br>This can be a problem, because we will have a good **signal to noise ratio** (**SNR**) when the machine is rotating fast, and a lower one when it rotates slow.<br>==If the machine is still the only thing I will measure will be the noise==.
