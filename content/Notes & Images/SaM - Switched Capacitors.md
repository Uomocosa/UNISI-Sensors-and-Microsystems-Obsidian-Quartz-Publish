##### ***Remeber***:

> A switched capacitor can be used for **increasing the capacitance value**, with respect to the sensor's capacitance, without changing the actual capacitance.<br>==This is like amplifying the capacitors of the sensor==:<br>![[Pasted image 20230719105612 1.png|500]]
> - So the starting phase, $S_3$ : **closed**, so that we start from $0 \kern2px V$.
> - Then there is a sequence of repeated steps, which are this ones:
> 	1. $S_1$: **ON**, $S_2$: **OFF**, $S_3$: **OFF**.<br>So in this phase, we have a charge, which is stored in the capacitance $C_S$, equal to:<br>So we have this charge $Q_1$ stored in $C_S$ at this point. 
> 	2. $S_1$: ***OFF***, $S_2$: ***ON***, $S_3$: ***OFF***.<br>At the beginning of this phase, we had the initial charge in $C_S$.<br>While at the end the total charge reamins the same, it is now shared between $C_S$ and $C_E$, so $C_S$ has given some charge to $C_E$.<br>So the value $V_{out}$ increases.
> 	3. So then we go back to the first phase (***1.***), so: $S_1$: **ON**, $S_2$: **OFF**, $S_3$: **OFF**.

> Most important formula: $$V_{out}^{(n)} = \frac{C_S V_R + C_R V_{out}^{(n-1)}}{C_S + C_R}$$After $n$ steps we have that:$$V_{out}^{(n)} = n \cdot C_S \cdot \Delta Q_n$$Where: $$\Delta Q_n = \frac{V_R}{C_R}$$So to obtain the sensor's capacitance we just use this formula:$$C_S = \frac{V_{out}^{(n)}}{n \kern2px \Delta Q_n}$$

> If I perform all the calculations, I put the steps in a graph, I will have this:<br>![[Pasted image 20230719105635.png]]
> - $V_r \over C_R$ is a constant term, which I call $\Delta Q_n$. 
> - So we have a linear behavior at the beginning, and then saturation, because we can go beyond this value, we will have a saturation at a certain point, the steps will become smaller and smaller until I reach the full charge of the capacitance.<br>==That's why I can perform this "cheat" only untill the voltage $V_R \gg V_{out}$==.<br>⇒ If I limit the measurement ratio to $n_{MAX}$, opprotunaly choosen, I will remain in the linear range of the capacitance, and I have this very simple way of amplifying the signal due to the sensor. 

---
###### Memory Card
![[Samsung_SaM_Notes_22_240516_105346_6.jpg]]

---
![[Pasted image 20230719105612.png]]
![[Pasted image 20230719105622.png]]
- So the starting phase, $S_3$ : **closed**, so that we start from $0 \kern2px V$.
- Then there is a sequence of repeated steps, which are this ones:
  1. $S_1$: **ON**, $S_2$: **OFF**, $S_3$: **OFF**.<br>So in this phase, we have a charge, which is stored in the capacitance $C_S$, equal to:<br>So we have this charge $Q_1$ stored in $C_S$ at this point. 
  2. $S_1$: **OFF**, $S_2$: **ON**, $S_3$: **OFF**.<br>At the beginning of this phase, we had the initial charge in $C_S$, which was:<br>And the charge at the end is the same obviously the same:<br>But the voltage, since these two are put in parallel, at the end of this first phase, will be:<br>So we have a first step of $V_{out}$, the output voltage, which is given by this value here. 
  3. So then we go back to the first phase (***1.***), so: $S_1$: **ON**, $S_2$: **OFF**, $S_3$: **OFF**.

After $n$ repetitions, we will have:
![[Pasted image 20230719105628.png]]


This is like having a **larger capacitance**, with respect to the sensor's capacitance.<br>==This is like amplifying the capacitors of the sensor==, and actually, if I perform all the calculations here, I put the steps, I will have this:
![[Pasted image 20230719105635.png]]
- $V_r \over C_R$ is a constant term, which I call $\Delta Q_n$. 
- So we have a linear behavior at the beginning, and then saturation, because we can go beyond this value, we will have a saturation at a certain point, the steps will become smaller and smaller until I reach the full charge of the capacitance.<br>That's why I can perform this "cheat" only untill the voltage $V_R \gg V_{out}$.
- If I limit the measurement ratio to $n_{MAX}$, opprotunaly choosen, I will remain in the linear range of the capacitance, and I have this very simple way of amplifying the signal due to the sensor. 
- Moreover, the readout circuit, when it reads the voltage output, sees these capacitors that can be very large.<br>⇒ I don't put the wiring in parallel to a small capacitance (less restrictions).
- Obviously, here I didn't take into account the parasitic resistances, and I also considered all the switches ideal, and so this is something which is really simplified, but it any case the principle is this. 
- Thing to remember:
	- Most important formula: $$V_{out}^{(n)} = \frac{C_S V_R + C_R V_{out}^{(n-1)}}{C_S + C_R}$$
	- After $n$ steps we have that:$$V_{out}^{(n)} = n \kern2px C_S \Delta Q_n$$Where: $$\Delta Q_n = \frac{V_R}{C_R}$$
- So to obtain the sensor's capacity we just use this formula:$$C_S = \frac{V_{out}^{(n)}}{n \kern2px \Delta Q_n}$$
