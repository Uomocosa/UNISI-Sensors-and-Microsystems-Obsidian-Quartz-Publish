##### ***Remeber***:

> - For a Piezoelectric Actuators, we consider to have a slice of piezo-material covered by two slices of conductive material, so that we can apply voltage and an electrical field to these dielectric:<br>![[Pasted image 20230719124208 1.png]]<br>⇒ So ==**it's like capacitance**==.
> - We study the [[SaM - Piezoelectric Effect in Details • Direct and Inverse Piezoelectric Effect|inverse piezoelectric effect]]:$$\overline{\overline{S}} = \overline{\overline{s}} \overline{\overline{T}} + \overline{\overline{d}} \vec{E}$$Also, we suppose to only apply a voltage to the actuator (no external mechanical forces), so we simplify:$$\overline{\overline{S}} = \overline{\overline{d}} \vec{E}$$

> If we take instead a **sensor**, with the same geometry of tha actuators, and apply a force over it:<br>![[Pasted image 20230719124242 1.png]]
> - It still acts as a **capacitance**, due to the strucuture, and we can calculate the charge enclosed in the volume of the sensor:$$Q = d\cdot F$$Where:
> 	- $d$ is the [[SaM - Piezoelectric Effect in Details • Direct and Inverse Piezoelectric Effect|piezoelectric coefficient]]
> 	- $F$ the force can also be seen as the eleastic costant multiplied the displacement, $F = k\cdot x$.

> So the variation of the thickness of the material gives us a charge accumulated over the surface, so ==it's like having **charge** in a **capacitance**==:
> Therefore I can go to this equivalent lumped network, this time I'm in the **electrical domain**:<br>![[Pasted image 20230719124334.png]]
> - This is the symbol for $Q_p$, it indicates a **charge generator**.
> - The capacitace $C_E$ depends on the type of piezoelectric material (form $\varepsilon = \varepsilon_0 \kern2px \varepsilon_r$ the [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|electrical permittivity]]), the surface area ($A$) and height ($h$) of the slice of piezoelectric material.
> - $R_A$, which comes from the non-ideality of the material: so a parasitic reisistance in parallel to the capacitance, which represents the parasitic current path that we have for a non-perfect insulators.<br>$R_A$ is quite large, in the order of $G\ohm$. #IMPORTANTE 

> - If we unite the two (sensor and actuator) we obtain the **complete model for a piezoelectric device**:<br>![[Pasted image 20230924124545.png]]
> - ==So I have the complete description of both the mechanical and the electrical behavior and the coupling between these two==.<br>==And this coupling here is due to the piezoelectric effect==.
> - From an electrical point of view so looking in the electrical port, this device here is an **active device**.<br>⇒ We have the possibility of using this sensor without any external exitation.<br>Remember that the sensed $V$ is really small, we will need an amplifer.
> - From the mechanical port, if you apply a voltage $V$ instead of using it as a sensor you use it as an **actuator**.
> - The output voltage $V$ will be then connected to the electrical circuit.

> Here are some values:<br>![[Pasted image 20240215193429.png]]
> Where $d_{11}$ and the other can be seen defined [[SaM - Compact Piezoelectric Coefficient Matrix for PZT • Dependence of Piezoelectricity on Temperature • Curie Temperature|here]]

| Material                                       | $d \ \left(\text{pC}\cdot \text{N}^{-1}\right)$ | $\varepsilon_r$               | $g \ \left({\text{m}^2\over \text{C}}\right)$ | $E \ \left(10^9{\text{N}\over \text{m}^2}\right)$ | $\lambda \ \left({\text{s}\cdot\text{N}\over \text{m}}\right)$ |
| ---------------------------------------------- | ----------------------------------------------- | ----------------------------- | --------------------------------------------- | ------------------------------------------------- | -------------------------------------------------------------- |
| **Quartz** $(Si O_2)$                          | $d_{11}\in [2 \div 3]$                          | $\in [4 \div 5]$              | $5.8 \cdot 10^{-2}$                           | $80$                                              | $2\cdot 10^{-5}$                                               |
| PZT (_Lead Zirconate Titanate_, _polycrystal_) | $d_{33} = 500$                                  | $\varepsilon_{r_{11}} = 2400$ | $2.4 \cdot 10^{-2}$                           | $80$                                              | $7\cdot 10^{-3}$                                               |
| PVDF (_polymer_)                               | $d_{31} = 23$                                   | $12$                          |                                               | $2$                                               | $5\cdot 10^{-2}$                                               |
#NOT_SURE_ABOUT_THIS unit of measure of $E$ : $E \ \left(10^9{\text{N}\over \text{m}^2}\right)$

---
###### Memory Card
![[Samsung_SaM_Notes_14_240516_113346_1.jpg]]

---
From the inverse effect we can build **actuators**
![[Pasted image 20230719124208.png]]
- We consider no external maehcanical forces, so all the force and strain is given by the piezoelectric effect (by the external voltage source).
- We consider to have a slice of piezo-material covered by two slices of conductive material, so that we can apply voltage and an electrical field to these dielectric.<br>⇒ So ==**it's like capacitance**==.
- We are applying voltage $V$ on this volume with are $A$ and thickness $h$, what happens is that the size (the dimensions) of this object changes when this voltage is applied with respect to the case of the not-excited material.
- I can call $x$, and also this variation along the $x$-axis and $y$ this variation along the $y$-axis
- What I have written here ($F = Kx$) is to convert this elongation ($x$) into an equivalent elastic force ($F$) which gives the same effect.<br>So the same elongation and this therefore is the spring constant of this slice here that depends obviously on the elastic constants of the material and also depends on the geometry, and we can also find this $K$ in this case here.

We have that this slice has height $h$ and surface $A$, and I have to have only a stress applied in this direction ($\vec x$) so I will have:
![[Pasted image 20230719124221.png]]
- $S_{11}$ : strain in the $x$ direction $= \frac{x}{h}$ where in this case $x$ is the displament with respect the undeformed thickness $h$, so it would be more proper to say $= \frac{\Delta x}{h}$, but anyway you get the point.
	- **NOTE**: The strain is a **pure number**.
- $c_{1111}$ is the first element of the $\overline{\overline{c}}$ tensor, which is the **inverse of the compliance tensor $\overline{\overline{s}}$**, it is measured in **pressure**.
- $T_{11}$ is again, a pressure ($F$ : force, $A$ : area)
- So this is our spring constant $K = \frac{c_{1111} A}{h}$ which describes the elastic behavior of this material with this geometry, so both **geometry ($\frac{A}{h}$) and material ($c_{1111}$) are important in this case**.


Now if I want find an equivalent circuit, a lumped linear network describing the overall behavior of this device here, I could obviously take into account all the situation where I have only a force applied in the $\vec x$ direction, and I am accounting for displacements and elongation in the same direction, so I want to be more general.
![[Pasted image 20230719124234.png]]
- $m$ : mass
- $\lambda$ : dumping coefficient
- $K$ : spring coefficient
- So this is not actually describing a perfectly elastic material, some energy is dissipated by the dumping coefficient.
- Then if I have also an external force I can place here another generator ($F_{ext}$)
- The current in this circuit will be equal to $\dot x$ (velocity)
- By placing the $F_p$ force generator, I take into account the **piezoelectric effect** on the mechanical behavior of this slice.

So we can now describe the behavior of a sensor with the same geometry as the actuator:
![[Pasted image 20230719124242.png]]
- Above the surface $A$ we have a very thin layer of conductive material, which has no importance from a mechanical point of view, only from an electrical point of view.
- This time I place here an amperemeter, which measure the current here (I consier it ideal so it's like a shrot circuit).
- $h$ and $x$ same as before.
- And now I take the other equation that describes the **direct effect**, and i consider no external applied field ($\vec E$)
- So the vector $d$ is only due to internal stress, and I place the distributed force all over the surface therefore I will have that I have an internal stress given by this $F$ (it is equally distribuited).

So at this point here I can consider to apply the ***\[Gauss Theorem\]***, using a surface which surrounds the surface here, so it's like having a cube which surrounds the surface here (drawn in red),and for simplicity we take its surface equal to $A$.
Therefore we can write that:
![[Pasted image 20230719124249.png]]
- $Q$ : charge which is in this closed volume, so the charge over this surface here
- $D_1\kern2px  A$ is the flux of $D_1$ on this closed surface which is equal to the charge which is in the surface ($Q$).

So:
![[Pasted image 20230719124319.png]]
- I find that the effect of a variation of the thickness of the material gives us a charge accumulated over the surface, so ==it's like having **charge** in a **capacitance**==.

Therefore I can go to this equivalent lumped network, this time I'm in the **electrical domain**.
![[Pasted image 20230719124334.png]]
- This is the symbol for $Q_p$, it indicates a **charge generator**. #NOT_SURE_ABOUT_THIS 
	%%- **NOTE**: This symbol is missused (it represents a tranformer), we have said that we measure the piezoelectric effect as a charge in a capacitance, so we could model it as the voltage in $V_{C_E}(t_0) = C Q$ #NOT_SURE_ABOUT_THIS %%
- The charge will be due to the piezoelectric effect, plus because it is linear the normal effect that I will have applying a voltage to a structure which is a capacitance.<br>We can model it as a capacitance since it is a structre with two plates in parallel and a dielectric in between, so we have $C_E$ (the electrical capacitance).
- $Q$ : total charge.
- $V$ : output voltage.
- We also need to add another component: $R_A$, which comes from the non-ideality of the material: so a parasitic reisistance in parallel to the capacitance, which represents the parasitic current path that we have for a non-perfect insulators.<br>$R_A$ is quite large, in the order of $G\ohm$.


We can have complete model for a piezoelectric device, which incorporates the **direct and inverse piezoelectric effect**:
![[Pasted image 20230924124545.png]]
- ==So I have the complete description of both the mechanical and the electrical behavior and the coupling between these two. and this coupling here is due to the piezoelectric effect==.
- From an electrical point of view so looking in the electrical port, this device here is an **active device**.<br>⇒ We have the possibility of using this sensor without any external exitation.<br>Remember that the sensed $V$ is really small, we will need an amplifer.
- From the mechanical port, if you apply a voltage $V$ instead of using it as a sensor you use it as an **actuator**.

***Sensor***:
So $A$ and $B$ are the terminal connected to readout electronics, $V$ is usually small, and $F_p$ is usually neglected or negligible, so we have this kind of model here
$F_{\text{ext}}$ is usually larger than this feedback effect $F_p$, so we can neglect the latter, and then we have:
![[Pasted image 20230719124347.png]]


***Actuator***:
But when we want to use it as an actuator then we are in the opposite situation, the power comes from the electrical domain, and it is transferred to the mechanical domain, this time if I go back:
What will be small will be this one because it's a feedback quantity, because the power comes from the electrical domain, and it causes motion, I don't have any  external forces usually, or if there are they are resistance forces and so this is what causes $\dot x$, it will be probably small.
So in this case A and B are connected to a voltage generator.
$Q_p$ can be usually neglected (feedback quantity), so this time we can consider this thing here:
![[Pasted image 20230719124357.png]]
