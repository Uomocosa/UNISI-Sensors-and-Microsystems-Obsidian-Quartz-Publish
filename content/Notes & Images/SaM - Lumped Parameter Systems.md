![[Lecture 2_230905_175804_1.jpg]]

---
For **Thermal Domain**, the Lumped parameter System is given by these three factors:
1. [[SaM - Heat Convection • Thermal Resistance|Heat convection]] (_placed as a Thermal **Resistance**_)
2. [[SaM - Heat Conduction • Thermal Resistance|Heat conduction]] (_placed as a Thermal **Resistance**_)
3. [[SaM - Heat Stored in a Body • Thermal Capacitance|Heat stored in a body]] (_placed as a Thermal **Capacitance**_)
- Both **heat convection** and **heat conduction** represent the **thermal resistance** between two bodies, which one of the two formulas we use to define the thermal reistance, depends on the way the two bodies exchange heat:
	- Via "***motion of matter***" (such as air or water): we are talking about **heat convection**.
	- Otherwise we are talking about **heat conduction**.
- Here is an [[SaM - Thermal Lumped Parameter System|example for thermal lumped parameter systems]].
- To better understand what the **heat flux** or **flow quantity** $\dot Q_S$ means, we have seen in a [[SaM - Reduce the Effect of Self-Heating|lecture]] that it is refered to the **power** $P(t)$ of the system.
- The **effort quantity** instead is intutitive since it is a temperature difference ($\Delta T$).

---
For **Mechanical Domain**:
- The lumed parameter equivalent is simply a **mass-spring-dumper system**:<br>![[Pasted image 20231124101933.png]]
	1. A **Spring** is placed in the system as a **Capacitance**.
	2. A **Damper** as a **Resistance**.
	3. A **Mass** as an **Inductance**.
- Also we have seen [[SaM - Mechanical Lumped Parameter System|this example]].

---
For the **[[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|Magnetic Domain]]**:
- We always consider the magnetic circuit formed by a **core** of ferromagnetic material, with a **gap**.<br>Optionally there could also be a **permanent magnet** built in the core:<br>![[Pasted image 20230719112102.png|500]]
- For this domain we represent:
	- **Effort quantity**: $\text{MMF}$ (*Magneto Motive Force*) $\left[\text{A}\cdot\text{turn}\right]$ (**ampere** $\cdot$ **turns**, since it is found multipling the current per the number of turns of a inductance).<br>Usually we find a **coil** with $N$ turns, and powered by a current $I$ used to create the [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetic field]] in the **core**.
	- **Flow quantity**: $\phi(B)$ *(Flux of the Magnetic Field)* $\left[V \cdot s\right]$ (**volt** $\cdot$ **seconds**).
- A permanent magnet (**PM**) is represented in the **lumped parameter equivalent system** as a series of an effor quantity and a generated impedance (voltage generator + resistance).

---
- Also for good measure we need to mention that we will also study an [[SaM - Acustic Impedance • Ultrasonic Lumped Parameter System|ultrasonic system]], but its [[SaM - Coarse Approximation of the Lumped Parameter Model of an Ultrasonic Transducer|lumped parameter system]] is only a coarse approximation.

---
![[Samsung_SaM_Notes_04_240515_111320_1.jpg]]
![[Samsung_SaM_Notes_04_240515_111320_2.jpg]]
