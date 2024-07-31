##### ***Remeber***:

> For [[SaM - Ultrasonic Waves|ultrasonic waves]] and [[SaM - Ultrasonic Transducers (Piezoelectric Device)|ultrasonic sensors or actuators]] we have not defined a [[SaM - Lumped Parameter Systems|lumped parameter system]], we have just defined the two quanitites for flow and effort and the generated impedance that binds the two.
> So for **ultrasonic systems** we have:
> - **Flow quantity**: $\dot u_1$
> - **Effort quantity**: $T_{11}$ ([[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|stress]]) for solids, $p$ (**preassure**) for liquids.
> - ==**Acustic Impendance**== $\left(\textbf{effort quantity}\over \textbf{flow quantity} \right)$: #IMPORTANTE $$\begin{array}{l} \text{fluids:} & Z = {\huge{p \over \dot u_1}} \\[5px] \text{solids:} & Z = {\huge{T_{11}\over \dot u_1}}   \end{array}$$==We can also define the **acustic impedance** in another, more useful way==: #IMPORTANTE $$Z = \rho \cdot v_l $$==This formula is valid for both **solids** and **liquids**==.<br>Here we have: 
> 	- $\rho$ : **density of the material**, measured in $\left[\frac{\text{Kg}}{\text{m}^3}\right]$.
> 	- $v_l$ : [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|longitudinal velocity of a wave inside a certain material]] $\left(v_l = \sqrt{c_{11} \over \rho}\right)$.
> 	- Remeber also that $u_1$ and $v_l$ are **reciprocal**:$$\dot u_1 = -{T_{11} \over \rho}{1 \over v_l}$$Where:
> 		- $\dot u_1$ represents "==*how fast the wave changes form*==".
> 		- $v_l$ is the longitudinal propagation velocity.
> 		- Both are velocities, and as such are expressed in $\left[\frac{\text{m}}{\text{s}}\right]$.
> - **Power**: (**effort quantity** $\cdot$ **flow quantity**): $$\begin{array}{l} \text{fluids:} & P = p \cdot \dot u \\ \text{solids:} & P = T_{11}\cdot \dot u_1   \end{array}$$

> #IMPORTANTE 
> Here's the value of the acustic impedance for the **PZT**:$$Z_{{\text{PZT}}} = 32.5 \ \text{Rayl}$$The unit of measure for the acustic impedance is $\left[\text{Rayl} = {\text{kg} \over \text{m}^2 \kern2px \text{s}}\right]$

%%> - $Z_{{\text{???}}} = 430 \ {\text{Rayl}}$%%

> Formulas that we need to arrive at this conclusion:
> 1. From the [[SaM - Elastic Waves and Acustic Waves • Calculation of the Wave Equation|"Elastic Waves and Acustic Waves" lecture]]:$$\lim_{\Delta V \to 0} \rho \kern2px \ddot{u_1} = {\partial T_{11} \over \partial x_1} + {\partial T_{12} \over \partial x_2} + {\partial T_{13} \over \partial x_3}$$And from the same lecture we have the [[SaM - Elastic Waves and Acustic Waves • Calculation of the Wave Equation|wave equation]]:$$\rho \ddot{u}_j = c_{ijkl}{\partial u_k \over \partial x_j \partial x_l}$$ 
> 2. We can simplifiy it if we consider it for [[SaM - Planar Waves or Plane Waves|planar waves]] in [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic material]]:$$\rho \ddot{u}_1 = c_{11}{\partial u_1 \over \partial^2 x_1}$$Since for **planar waves** we have that: $${\partial T_{12} \over \partial x_2} = {\partial T_{13} \over \partial x_3} = 0$$
> 3. From the [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|"Generic Ultrasonic Wave Function" lecture]], we use a a simple **longitudinal wave function**: $$U_1(t,\, x_1) = U_{1F}\left(t - \frac{x_1}{v_l}\right)$$
> 4. From the [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|"Generic Ultrasonic Wave Function" lecture]]:$$v_l = \sqrt{c_{11} \over \rho}$$

> Here are the passages: (**NOTE**: These are my calcuation, they can be wrong #NOT_SURE_ABOUT_THIS )
> 1. From the [[SaM - Elastic Waves and Acustic Waves • Calculation of the Wave Equation|"Elastic Waves and Acustic Waves" lecture]]:$$\lim_{\Delta V \to 0} \rho \kern2px \ddot{u_1} = {\partial T_{11} \over \partial x_1} + {\partial T_{12} \over \partial x_2} + {\partial T_{13} \over \partial x_3}$$
> 2. We assume a [[SaM - Planar Waves or Plane Waves|planar waves]] that propagates in [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic materials]], so we can use a simplified version of the [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|hooke's law]]: $$\rho \ddot{u}_1 = c_{11}{\partial u_1 \over \partial^2 x_1}$$
> 3. Since we are talking about a **planar wave** we will have that:$${\partial T_{12} \over \partial x_2} = {\partial T_{13} \over \partial x_3} = 0$$So we can rewrite $(1.)$ as: $$c_{11}{\partial^2 u_1 \over \partial^2 x_1} = {\partial T_{11} \over \partial x_1}$$
> 4. We now define as we have done in the [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|"Generic Ultrasonic Wave Function" lecture]] a simple **longitudinal wave function**:$$U_1(t,\, x_1) = U_{1F}\left(t - \frac{x_1}{v_l}\right)$$This time we don't consider the **backward** part of the formula, we assume that this wave only propagates **forward**.
> 5. If we derive $U_1(t,\, x_1)$ over $t$ we obtain: $$\dot U_1(t,\, x_1) = V_{1F}\left(t - \frac{x_1}{v_l}\right)$$Where $V_{1F}  = \dot U_{1F}$.<br>And if we derive it over $x_1$ we obtain:$${\partial U_1(t,\, x_1) \over \partial x_1} = -{1 \over v_l} \cdot V_{1F}\left(t - \frac{x_1}{v_l}\right)$$Since $U_{1F}$ depends on $\left(t - \frac{x_1}{v_l}\right)$.
> 6. So we can say:$${\partial U_1(t,\, x_1) \over \partial x_1} = -{1 \over v_l} \cdot \dot U_1(t,\, x_1)$$
> 7. Similarly using $(3.)$ we can say: $$c_{11}{\partial^2 U_1(t,\, x_1) \over \partial x_1^2} = {\partial T_{11} \over \partial x_1}$$Or, if we integrate from both parts over $x_1$: $$c_{11}{\partial U_1(t,\, x_1) \over \partial x_1} = T_{11}$$
> 8. So using $(7.)$: $$T_{11} = c_{11}\cdot \left[ -{1 \over v_l} \cdot \dot U_1(t,\, x_1)\right]$$
> 9. We know form the [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|"Generic Ultrasonic Wave Function" lecture]] that:$$v_l = \sqrt{c_{11} \over \rho}$$And if we calculate:$${c_{11} \over v_l} = {\rho \cdot v_l}$$
> 10. So we can rewrite $(8.)$ as:$$T_{11} = - {\rho \cdot v_l} \cdot \dot U_1(t,\, x_1)$$For simplicity i write $\dot U_1(t,\, x_1)$ as $\dot u_1$, since we have defined the impedance as: $$Z = {T_{11} \over \dot u_1}$$Now we know that it is equal to, and we define it as a **positive value**:$$Z = \rho \cdot v_l$$We have demonstrated it starting from a solid, but the same formula is true also for liquids.

---

![[Pasted image 20230720162047 1.png]]
- So acoustic impedance is like a generalized impedance.
- The ***flow quantity*** (represented as a current) is the speed of the particles, which are vibrating and give the propagation of the wave.
- Whereas the ***effort quantity*** (represented as a voltage) is the **stress** ($T$), or in fluids the **pressure** ($P$).
- So the power ($P$) of the wave would be for us the product of this two quantity.

Let's take for example now a [[SaM - Planar Waves or Plane Waves|simple plane wave]], defined using an [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|ultrasonic wave function]]:
![[Pasted image 20230720162054.png]]
- So you will have uniform speed, preassure and stress.
- **NOTE**: $V_{1F}$ represents "how fast the wave changes form", the propagation speed is still $v_l$.

So we can say, using ***Hooke's law***:
![[Pasted image 20230925184638.png]]
- We change the derivative since integating $T_{11}$ over time or space is similar, except it is scaled.

So the impedance is equal to:
![[Pasted image 20230925184942.png]]
- $\rho$ is the density as usual.
- So the impedance can be written in this two ways.
- $B = c_{11} = \frac{P}{\Delta V \over V}$ : Bulk modulus ($V$ in the formula is volume)
