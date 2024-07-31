##### List of things to memorize:
![[SaM - Primary Sensors]]

---
###### [[SaM - Definition of Primary Sensor]]
*Sensor = Primary Sensor + Real Sensor*
The typical structure of a device is: ***Sensor*** ⇒ ***Front-End Electronics*** ⇒ ***A/D Converter***

- ==_A primary sensor transform a non-electrical quantity into another (more "convinent") non-electrical quantity_==.
- ==_A sensor (or in this case called "real sensor") instead, transforms a non-electrical quantity into an **electrical quantity**_==.
---
###### [[SaM - Different Definitions for Preassure]]
- **differential pressure** (so the difference between two pressures)
- **absolute pressure**, so it's like taking $p_1$ as $0$ pascal
- **gauge pressure**, which is a differential pressure where **$p_1$ is $1$ atmosphere**

- There are many different applications and solutions for primary sensors for pressure, and they depend essentially on the **range** (preassure ranges) can be very different

- The unit for pressure that should be used is **Pascal**.
- Actually also **atmosphere** is used: **one atmosphere is a little more than 100 kilopascal**.
- It is also used **bar**, a **bar is exactly 100 kilopascal**.
- **PSI** which is **pound per square inch**, which corresponds to $6.89 \cdot 10^3 Pa$. 

---
###### [[SaM - Liquid Columns]]
![[Pasted image 20230927113444.png|500]]

---
###### [[SaM - Deformable Structures]]
![[Pasted image 20230927113516.png|500]]
- ***Formula***:$$p = \frac{k \cdot \Delta x}{A}$$
---
###### [[SaM - Burdón Tubes]]
![[Pasted image 20230710121807.png|500]]

---
###### [[SaM - MEMS Membranes]]
![[Pasted image 20230927113817 1.png|500]]
- ***Formula***:$$\overline D_z = \alpha \cdot \Delta p$$Where: (*NOT IMPORTANT, too complicated*)$$\alpha = {(3-\nu^2) \kern2px R^4 \over 16 \kern2px E \kern2px t^2},\kern25px \overline D_z = {1 \over 3} D_z(0),\kern25px \Delta p = p_{\text{above}}-p_{\text{under}}$$
---
###### [[SaM - Orifices]]
![[Lecture 3_230907_175256_4 1 1.jpg|500]]
- "*Orifices*" in italian: "*Orifizi*".
- ***Bernoulli equation***:$${1 \over 2}\rho v^2 + p + \rho g h = \text{const.} $$
- ***Orifices equation***:$$v_2 = \sqrt{p_2-p_1 \over \rho\left({A_2^2 \over A_1^2 - 1}\right)}$$
---
###### [[SaM - Pitot Tube]]
- ***Structure***:<br>(_One tube has static preassure, used as reference, the other is open and its preassure varies due to the velocity of the fluid_)<br>![[Pasted image 20240307111342.png|500]]
- ***Using the bernoulli equation, if we measure the difference in height***:$${1 \over 2} \rho v_1^2 + p_{\text{atm}} + \rho g h_1 =   p_{\text{atm}} + \rho g h_2$$***Or if we measure the difference in preassures***:$${1 \over 2} \rho v_1^2 + p_1 + \rho g h_{\text{static}} =   p_2 + \rho g h_{\text{static}}$$Where:
	- $p_{\text{atm}} = p_1$.
	- $h_1 = h_2 = h_{\text{static}}$.
So:$$v = \sqrt{2(p_2-p_1)\over \rho}$$

---
###### [[SaM - Anemometry or Hot Wire]]
![[Lecture 3_230907_175256_6 1.jpg|500]]<br>![[Pasted image 20230710122140.png]]
- ==We heat something and then we sense the temperature of other devices close to this heater, to understand which is the convection factor, the convection behavior of the fluids surrounding this heat source==

---
###### [[SaM - Doppler Effect for Primary Sensors]]
$$f_0' = f_0 \left(1 - f_D\right)$$Where:$$f_D = {2 v \cos \theta \over c}$$
![[Lecture 3_230907_175256_7 1.jpg|500]]

---
###### [[SaM - Time of Flight Principle for Primary Sensors]]
- ***Formulas***:$$c_w = {L \over 2}{T_{UP} + T_{DOWN}  \over T_{UP} \cdot T_{DOWN}}$$And:$$v = {L \over 2}{T_{UP} - T_{DOWN}  \over T_{UP} \cdot T_{DOWN}}$$
- ***Structure***:<br>(_There is an error in the following formulas_)<br>![[Lecture 3_230907_175256_8 1.jpg|500]]

---
###### [[SaM - MEMS Cantilever]]
![[Pasted image 20231119195139.png|500]]
- ***Formula***:$$\text{new\_quantity} = \alpha \cdot F$$More specifically:
	- $\varepsilon = \alpha_{\text{stress}} \cdot F$
	- $D_z(x) = \Delta z = \alpha_{\text{deflection}} \cdot F$
- It is a **differential primary sensor**:<br>![[Pasted image 20231127120608.png|500]]

---
###### [[SaM - Load Cells or Pillar]]
![[Pasted image 20231126192033.png]]
- ***Formula***:$$\varepsilon_l = \frac{F}{E\cdot A}$$
- It is a **differential sensor**:<br>![[Pasted image 20231127115825.png|500]]

---
###### [[SaM - Gyroscope]]
![[Lecture 4_230908_153707_1 1.jpg|500]]
- ***Coriolis aceleration formula***:$$\vec a = -2\vec \Omega \times \vec v$$
- ***Simplest case (angular velocity perpendicular of the velocity)***:$$a_y = -2\kern2px \Omega_z \kern1px  v_x$$
---
###### [[SaM - Accelerometer]]
![[Lecture 4_230908_153707_2 1.jpg|500]]
- ***Calculations***:
	1. ***Find the [[SaM - Lumped Parameter Systems|lumped parameter model]]***:<br>![[Lecture 4_230908_153707_2 2.jpg|500]]
	2. ***Find the [[SaM - Thevenim and Norton Equivalent|Thevenim Equivalent]]***:<br>![[Lecture 4_230908_153707_4 1.jpg|500]]<br>Simplifying the **Thevenim resistance**, since $m_B \gg m_S$, so we exclude it from the load, since a parallel between $m_S \parallel m_B \simeq m_S$.
	3. ***Calculate***:$$H(s) = \frac{m_{\tiny{S}}}{m_{\tiny{S}}\kern2px s + \lambda + \large{\frac{k}{s}}}$$
	4. ***Transform into [[Bode Plot|Bode form]]***:$$\frac{R(s)}{A(s)} = \frac{m_{\tiny{S}}}{k} \frac{1}{{m_{\tiny{S}} \over k}s^2 + {\lambda \over k}s + 1}$$
- ***Mounted and Unmounted accelerometer***:<br>![[Lecture 4_230908_153707_6 1.jpg|500]]
- **Mounted Behaviour** if $m_B \gg m_S$.

---
###### [[SaM - Non-Idealities of an Accelerometer]]
- ***Gravity***:
	- If the sensor does NOT rotate ⇒ ***offset (can be corrected)***.
	- If the sensor rotates ⇒ ***variable offset (cannot be corrected)***.
- ***Not mounted in a "solid" way***:<br>![[Pasted image 20230710172353 2.png|500]]<br>![[Pasted image 20230710172353 1.png|500]]

---
###### [[SaM - Transfer Funtion of a Mounted Accelerometer]]
$${R(s) \over a(s)} = H(s) {{m_s \over K} \over {m_s \over K}s^2+{\lambda \over K}s+ 1}$$

---
###### [[SaM - Primary Sensor for Temperature]] 
(*Skipped*)