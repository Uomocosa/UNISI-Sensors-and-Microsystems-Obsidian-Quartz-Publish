##### ***Remeber***:

> - Capacitive Sensor are often used in MEMS devices to sense **Pressure**, this is the basic structure, with a fixed plate, and a deformable structure or membrane:<br>![[Pasted image 20230718200720 1.png]]
> - ==In this case we have to suppose both the membrane and the fixed plate to be **conductive** and act as one of the plate of the sensor==.
> - What our Sensor measures is the **average of a differential preassure**, specifically the preassure exerted on the membrane ($p_1$) and the pressure inside our sensor ($p_2$).
> - What we obtain is a **linear passive sensor** with a formula like this:$$C_0(1 + x)$$Where:
> 	- $C_0$ can assume values between $[??? {\text{?}\over\text{?}} \div ??? {\text{?}\over\text{?}}]$. #TODO 
> 	- $x$ is a linear function of the differential preassure: $x = \alpha \kern2px (P_1-P_2)$.<br>It can assume values between $[??? {\text{?}\over\text{?}} \div ??? {\text{?}\over\text{?}}]$. #TODO 

---
###### Memory Card
![[Samsung_SaM_Notes_22_240516_105346_2.jpg]]

---
Capacitive Sensor are often used in MEMS devices to sense **Pressure**:
![[Pasted image 20230718200720.png]]
- As a primary sensor, the pressure can be sensed by means of a **deformable plate** or **membrane**.<br>==In this case we have to suppose the membrane to be **conductive** and act as one of the plate of the sensor==.<br>Under the **deformable conductive memebrane** we have a **conductive fixed plate**.
- ==We measure the **average of a differential preassure**==.

![[Pasted image 20230718200729.png]]
- $\overline D_z$ : average of $D_z(r)$.
- $d_0$ : un-deformed distance between the two plates (constant).
- $\overline d$ : average distance.<br>$\overline d = d_0(1-\frac{\overline{D_z}}{d_0})$
- $R$ : radius of the two circular plates.
- $r$ : our variable.
- $\alpha_D$: sensitivity.
- $\alpha_P = \frac{\alpha_D}{d_0}$: sensitivity.
- ==$x$ is a **linear** function of the pressure==: $$x = \alpha_P (P_1-P_2)$$

Formulas used in the average integration:
1. [[Definition of Average in the Integral Sense|Definition of average]]: $$\overline{f} = \frac{1}{b - a} \int_{a}^{b} f(x) \, dx$$
2. [[Change Variables in an Integral ('Change of Basis')|Change of Basis]]:$$r \to \rho^2$$
3. "Multiplied" the integral by:$$\cdot\kern2px \frac{\pi}{\pi}$$
