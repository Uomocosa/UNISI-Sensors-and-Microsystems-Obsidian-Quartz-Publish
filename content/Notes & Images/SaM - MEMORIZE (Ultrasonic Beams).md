##### List of things to memorize:
![[SaM - Ultrasonic Beams]]

---
###### [[SaM - Measurements & Measurement Types for Ultrasonic Beams]]
- ***$3$ Example of measurements***:
	1. **Non-Contact Measurement**.
	2. **Echography** and **[[SaM - Doppler Effect for Primary Sensors|Doppler Effect]]**.
	3. **Non Destructive Testing**.
- ***$2$ Measurement Types***:
1. **[[SaM - Transmission Mode for Ultrasonic Beams • C-Mode Image|Transmission]]**.<br>(*2 devices that alternates between sending an reciving*).
2. **[[SaM - Echo Mode for Ultrasonic Beams|Echo mode]]**. (the most important one)<br>(*1 device for both sensing and reciving*).

---
###### [[SaM - Transmission Mode for Ultrasonic Beams • C-Mode Image]]
- ***Transmission mode***: _using two synced transmitter(**TX**) and reciver (**RX**) we will obtain a **C-mode image**_:<br>![[Pasted image 20230720162945.png|222]]<br>![[Pasted image 20230720163035.png|333]]
- _You can reduce the frequency to see more in depth, or you can increase it to have a more clear image (but at surface level)_.
- _TX and RX must operate at the same frequency_.
- _Sometimes we place the object in water, using water as a coupling medium, but this is not so easy to do_.

---
###### [[SaM - Echo Mode for Ultrasonic Beams]]
- In "**_echo mode_**" measurements, ==we have a **single transducer**== which acts as a transmitter (**TX**) and also as a receiver (**RX**).
- ***Example***:<br>![[Pasted image 20230720163055 1.png|500]]
- ***Actuation phase***:<br>![[Pasted image 20230720163055 2.png|500]]<br>![[Pasted image 20230720163105 1.png|500]]
- ***Modelling of the sensor part, ignoring the TX part***:<br>![[Pasted image 20230925232629.png|500]]
- ***Time of flight of the returning echos***:<br>![[Pasted image 20230720163114.png|500]]
- ***Time of flights***:$$\begin{array}{l}  t_1 = {2 l_1 \over v_{l_1}}  \\[3px]  t_2 = {2 l_2 \over v_{l_1}} + {2 (l_2-l_1) \over v_{l_2}}  \end{array}$$
- ***"Initial dead zone"***: obstical closer than ${T_P \over 2}v_{l_1}$ cannot be seen. #NOT_SURE_ABOUT_THIS (calculation made by myself)
- ***Surfaces too close to each other***:<br>![[Pasted image 20230720163131.png|500]]
- #TODO check tof and dead zones
- ***Time-of-flight-difference between the second and third material***:$$\Delta t = {2 \Delta l \over v_{l_2}}$$
- ***Minimum distance***:$$\Delta l \gg {N \over 2} \lambda_w$$
- ***General time of flight formula***:$$t_{TOF} = \frac{2\kern2px l}{v}$$
- ***Terminology***:
	- $t$ : time.
	- $l$ : size, more specifiaclly length, of the matrial.
	- $v$ : [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|propagation velocity of the wave]].
	- $\lambda_w$ : [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|wavelenght]].
	- $N = {T_P \over T}$
		- $T_P$ : duration of the pulse.
		- $T = {1 \over f_0}$ : period of the wave.
		- "The **duration of the pulse** $(T_p)$ is a **multiple** $(N)$ of the ++wave period** $(T)$"<br>⇒ $N\in \mathbb{N}$

---
###### [[SaM - Acustic Impedance • Ultrasonic Lumped Parameter System]]
- For **ultrasonic systems** we have:
	- **Flow quantity**: $\dot u_1$
	- **Effort quantity**: $T_{11}$ ([[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|stress]]) for solids, $p$ (**preassure**) for liquids.
	- ==**Acustic Impendance**== $\left(\textbf{effort quantity}\over \textbf{flow quantity} \right)$:$$\begin{array}{l} \text{fluids:} & Z = {\huge{p \over \dot u_1}} \\[5px] \text{solids:} & Z = {\huge{T_{11}\over \dot u_1}}   \end{array}$$Or more generarly:$$Z = \rho \cdot v_l $$Where:
		- $\dot u_1$ represents "==*how fast the wave changes form*==".
		- $v_l$ is the longitudinal propagation velocity.
		- Both are velocities, and as such are expressed in $\left[\frac{\text{m}}{\text{s}}\right]$.

---
###### [[SaM - Influence of the Source Geometry on the Ultrasonic Filed Shape-Type]]
- ***Point source ⇒ spherical wave***:<br>![[Pasted image 20230720162529.png|333]]
- *~Ex.: Transducer which is a Plane Piston Circular* (more usual and real case):<br>![[Pasted image 20230720162626.png|500]]
	-  **Inside the cilinder** ("***Frensel Region***" or "**Near Field**"): approximately **planar**.
	- **Outside the cilinder** ("**Far Field Region**"): behaving like a spherical wavefront.
- _For the **Transducer which is a Plane Piston Circular**, if Ii find two obstacles within the "far region field", both are seen by simultaneusly the probe and they appear as to be only one obstical, so **they can't be distinguished** (with a still probe)_:<br>![[Pasted image 20230720162635.png|333]]

---
###### [[SaM ~ Example of Ultrasonic Beams]]
(*Skipped*)

---
###### [[SaM - Focused Transducer for Ultrasonic Beams]]
- ***Focused transducer***:<br>![[Pasted image 20230720162705.png|500]]

---
###### [[SaM - Control of an Ultrasonic Beam]]
- tranducer is formed by **many different and independently excited elements**.<br>![[Pasted image 20230720162719.png|500]]
- If we move the array of tranducers, as shown in the picture, we can emulate the foused beam structure and obtain the same effect.
- However, since [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|the wave depends a linear relationship between time and space]], I don't need to physically move each transducer, because ==the only thing that is needed is to excite these single elements with a **time shift**==.

---
###### [[SaM - Ultrasonic Beam Stearing]]
- ***Example***:<br>![[Pasted image 20230720162730.png|333]]

---
###### [[SaM - Linear Scanning for Ultrasonic Beams]]
- ***Example***:<br>![[Pasted image 20230720162739.png|333]]

---
###### [[SaM ~ Real World Example • Ultrasonic Sensors]]
(*Skipped*)

---
###### [[SaM - Alternative to Piezoelectric Arrays for Ultrasonic Beams]]
- A possible solution, a possible alternative to piezoelectric arrays are the so-called [[SaM - Capacitive Ultrasonic Transducers • CMUT Probes|CMUT probes]].<br>**CMUT** (*Capacitive Ultrasonic Transducer*)
- They use the [[SaM - Traditional Sensors vs. MEMS • MEMS Technology|MEMS technology]], so they are **less expensive**, so you can obtain more complex devices.

---
###### [[SaM - Absorption for Ultrasonic Beams]]
- In real materials you have "**absorption**": _the conversion of ultrasound energy to heat energy_.<br>==This means that the amplitude of the wave decays when traveling in a media==.
