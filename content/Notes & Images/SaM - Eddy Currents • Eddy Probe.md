##### ***Remeber***:

> - Suppose you have a **non-ferromagnetic** target, so the target's permeability is approximately $\mu_T \simeq \mu_0$, actually if it's exactly $\mu_0$ the reluctance will not change at all.<br>⇒ So theoretically from [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|the modeling that we have done untill now]], there is no way of sensing the proximity of this non-ferromagnetic target because the overall reluctance (insiede and outside the target) is constant.
> - But if this non-ferromagnetic target is **conductive**, what happens is that the variation of the flow inside (due to the **AC exitation**), **generates currents**.<br>Obviously, this happens if the variation are large enough, and so this current becomes important.
> - These current which is an **induced current**, let's call it $i_e$, is called **Eddy Current**, and  are due to the voltage which generates in the target ($v_T$) : <br>![[Pasted image 20230719112556.png|500]]
> - This Eddy current, forms a magnetic field which **opposes to the variation of the flux**.<br>Therefore ==the best way to model everything is to consider the **mutual induction**==.

> - However to have a measearable effect, I need that the thickness of the target ($t$) to be larger than the "**skin depth**" or "**penetration depth of the magnetic field**" ($\delta$), so:$$t \gt \delta = \frac{1}{\sqrt{\pi \sigma f \mu_T}}$$Where:
> 	- $\sigma$ :  the **conductivity** of the target.
> 	- $f$ : frequency of the excitation.
> 	- $\mu_T$ : permittivity of the target.
> - Here's the **skin depth**, measured in $\mu m \ (=10^{-6}\ m)$, per $f = 1 \ \text{MHz}$ #IMPORTANTE 
> 	- *Alluminum*: $\delta = 84 \ \mu m$
> 	- *Permalloy*: $\delta = 2 \ \mu m$
> 	- *Steel*: $\delta \in [ 12 \ \mu m \div 400 \ \mu m ]$
> 	- **NOTE**: ==In order to have this eddy current effect to be "usable", usually we use **very high frequency**==.

> We model the Eddy Currents like this:<br>![[Pasted image 20230719112630.png]]
> - And the resulting impedance $Z \triangleq {v \over i_1}$ will be equal to: $$Z = \underbrace{R_1 + {\omega^2 M(x) R_2 \over R^2 + \omega^2L_2^2}}_{\huge R_e} + j\omega \kern0px \underbrace{\left(L_1 - {\omega^2 M(x) L_2 \over R_2^2 + \omega^2L_2^2}\right)}_{\huge L_e}$$And since the final formula is too complex just remember that the resulting impedance: $$Z \triangleq {v \over i_1} = R_e + j\omega L_e $$And that both $R_e$ and $L_e$ depend linearly from $M(x)$.

> - So Eddy currents probe can be used, but ==they need to be calibrated depending on the material==.<br>Which is especially important if the material is also **ferromagnetic**.
> - Let's see how the equivalent percentance inductance $L_e(x) \over L_0$, changes with respect of the distance to the target and the material:<br>![[Pasted image 20230719112730.png|500]]
> - **NOTE**: #IMPORTANTE <br>Some materials increases their inductance $L_e(x)$, like *Stell*.<br>While other decreases their inductance, like for example *Alluminum*.<br>Also the percentange change of $L_e(x) \over L_0$ can assume values of around $[\sim 80\% \div 120\%]$.

> - ==We have previously disregarded of the effect of Eddy Currents, because we have considered the **reluctance** the most relevant variation, and also we have considered **low frequencies**==, so the induced current played a **minor role**.

> - A typical front end for this kind of objects, which has to operate at very high frequency is for instance: **an FM modulated system**: #IMPORTANTE <br>(*However the strucutre is NOT IMPORTANT):*<br>![[Pasted image 20230719112745 1.png|500]]
> - The frequency which are used with this kind of probes is let's say also in the order of $\sim 2 \text{MHz}$.

---
###### Memory Card
![[Samsung_SaM_Notes_23_240516_111131_2.jpg]]

---
# Index
- [[#Eddy Currents]]
- [[#Maximum Thickness]]
- [[#Lumped Parameter Circuit]]
- [[#Target Characteristics]]
- [[#Target Characteristics]]
- [[#Eddy Probe]]
- [[#Small Recap on VRS and Eddy Current]]

---
##### Eddy Currents
There is also another effect that we have not considered up to now.
![[Pasted image 20230719112556.png]]
- We suppose to have a non-ferro magnetic target so $\mu_r \simeq 1$, so the target's permeability is approximately $\mu \simeq \mu_0$, actually if it's exactly $\mu_0$ the reluctance will not change at all.<br>⇒ So theoretically from the modeling that we have done, there is no way of sensing the proximity of this non-ferromagnetic target because the overall reluctance (insiede and outside the target) is constant.
- But if this non-ferromagnetic target is **conductive**, what happens is that the variation of the flow inside (due to the **AC exitation**), **generates currents**.<br>Obviously, this happens if the variation are large enough, and so this current becomes important.
- These current which is an **induced current**, let's call it $i_e$, is called **Eddy Current**, and  are due to the voltage which generates in the target ($v_T$).

---
##### Maximum Thickness

This Eddy current, forms a magnetic field which **opposes to the variation of the flux**.<br>Therefore the better way to model everything is to consider the **mutual induction**:
![[Pasted image 20230719112606.png]]
- The effect that the coil has on the target is like the primary of a **transformer**.<br>Instead the Eddy current flowing is like the current induced in the secondary of a transformer.
- We can model everything using mutual induction, but before going on, I will also show you that if $t$ is the **thickness of the target**, then I need that the thickness of the target has to be larger than the "**skin depth**" or "**penetration depth of the magnetic field**" ($\delta$), so:$$t \gt \delta = \frac{1}{\sqrt{\pi \sigma f \mu_T}}$$Where:
	- $\sigma$ :  the **conductivity** of the target.
	- $f$ : frequency of the excitation.
	- $\mu_T$ : permittivity of the target.
- I need this $t$ to be larger than $\delta$ in order to get actually a real and appreciable effect.
- To have an idea, I can put here the minimum thickness for different material, and for different frequencies:<br>**NOTE**: $\delta$ measured in **$\mu$m** (**$=10^{-6}$ m**):
- ==In order to have this eddy current effect to be "usable", usually we use **very high frequency**==.


---
##### Lumped Parameter Circuit

So this is the situation:
![[Pasted image 20230719112630.png]]
- We model the Eddy Current effect with a transformer defined by the **mutual inductance** $M(x)$.
- $R_1$, $L_1$, is the electrical circuit which models the input (core + coil).
- $M(x)$, $R_2$, $L_2$, is the electrical circuit which models the target.
- The mutual inductance here depends on $x$ (the **gap**), so the distance between the target and the probe, because the field is more intense if you are closer to the tip of the probe.
- If the target is non-ferromagnetic ⇒ $L_1$ is constant, or approximately.

> ***Formula used for transformers***:
> A transformer with mutual inductance $M$ and two currents $i_1$ and $i_2$ flowing trough its two "branches", then we will have the two voltage drops equal to (in the frequency domain):$$\begin{align}&V_1 = j\kern2px \omega \kern1px M \kern1px i_2\\&V_2 = j\kern2px \omega \kern1px M \kern1px i_1\end{align}$$

So we can write:
![[Pasted image 20230719112641.png]]
$v$ : "voltage" formed inside the target, the formula it is a bit messy I will rewrite it:$$v = \left(R_1 + j\omega L_1\right)i_1 + j\omega M(x) i_2$$
Then we can calculate:
![[Pasted image 20230719112654.png]]
- $Z$ the impedance seen by my generator defined as $\frac{v}{i_1}$.
- $R_e$ : equivalent resistance.
- $L_e$ : equivalent inductance.


---
##### Target Characteristics
*What happens if instead the target is also ferromagnetic (not only conductive)?*
⇒ **Then we will have an equivalent reluctance $L_e$ which varies with $x$.**
![[Pasted image 20230719112713.png]]
- So Eddy currents probe can be used, but ==they need to be calibrated depending on the material==.<br>Which is especially important if the material is also **ferromagnetic**.

So we have an impedance and also an inductance that depend on:
![[Pasted image 20230719112730.png]]
- Here you can see the ratio between the equivalent inductance ($L_e(x)$), as a function of $x$ and the reference value $L_0$ (which is the no-target reference, so vacuum in front of the tip).
- The scale is in percentage.<br>To understand we take the example of the **iron alloy**: *when it is very close to the target will have a $20\%$ increased value with respect to the "no-target reference"*.
- So the total impedance will depend on:
	- Gap distance ($x$).
	- Conductivity $\sigma$ or instead we can say resistivity $\rho$.
	- Then also on the temperature $T$, because temperature is affecting the behavior of the conductivity of the material.
	- The permeability of the target $\mu_T$.
	- The thickness $t$ of the target.<br>Because obviously in case we have a small thickness, we will confine the currents in a smaller range, and so we have a reduced effect of the parasitic current.<br>(So in case we do not respect the $t \gt \delta$ rule)

---
##### Eddy Probe

![[Pasted image 20230719112745.png]]
- ==We have previously disregarded of the effect of Eddy Currents, because we have considered the **reluctance** the most relevant variation, and also we have considered **low frequencies**==, so the induced current played a **minor role**.
- A typical front end for this kind of objects, which has to operate at very high frequency is for instance: **an FM modulated system**.
- And this is a front end structure, I don't want you to remember it, it's here only to understand which kind of solution I usually adopted for this kind of probes.
- And in this case obviously the oscillating frequency depends on the value of this inductance $L(x)$ and resistance $R(x)$, but there are also many other types of circuit, obviously.<br>And the frequency which are used with this kind of probes is let's say also in the order of $2 \kern2px MHz$.

---
##### Small Recap on VRS and Eddy Current

We can recap for a moment which kind of sensor we have studied in detail.<br>So we have essentially divided sensors into:
- Where we had **Inductive VRS** (**variable reluctance**).
- Where we had **Eddy Current**.

Inductive VRS are based on **variation of the reluctance of the magnetic circuit**.

Instead Eddy Current ones are different, the principle of measurement relies on **mutual inductance** (we have modelled it as a **transformer**).
Where the secondary circuit is the target, and it depends on the primary which is the probe, which also depends on the secondary.
⇒ So there is a **mutual coupling** and **mutual inductance** which varies due to the different position of the target and of the inducing circuit (the primary circuit).

On this kind of principle many other measurement devices, so sensors, can be found in industry.

So there are many devices which can measure speed or position, especially angle or position, based on transformer structure where primary and secondary circuits can move with respect to the other.
![[Pasted image 20230719112757.png]]
So we have studied the eddy current probe but there are many other like a tachymetric circuit, and so on.

---

