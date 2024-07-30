##### List of things to memorize:
![[SaM - Magnetism]]

---
###### [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field]]
$$\begin{array}{l} \text{In a vacum} &  \vec B = \mu_0 \vec H \\ \text{In a material} &   \vec B = \mu \vec H     \end{array}$$Where:$$\mu = \mu_0 \mu_r$$And: $$\mu_r = 1 + \mathcal{X}_M$$
- ***Terminology***:
	- $\mu$ : magnetic permeability $\left(\mu = \mu_0 \mu_r\right)$
		- $\mu_0$ : magnetic permeability in the void $\left(\mu_0 = 4\pi \cdot 10^{-7} \  {\text{T}\cdot \text{m}\over \text{A}} \right)$
		- $\mu_r$ : relative magnetic permeability
	- $\mathcal{X}_M$ : magnetic susceptibility $\left(\mu_r = 1 + \mathcal{X}_M \right)$
	- $B$ : magnetic field density $\left(B = \mu H\right)$, and $\left[B\right] = T \ \left(\text{Tesla}\right)$
	- $H$ : magnetic field intensity $\left[H\right] = {\text{A}\over\text{m}}$
	- $M$ : magnetization $\left(M = \mu_0 \mathcal{X} H\right)$

---
###### [[SaM - Types of Magnetic Materials (Diamagnetic, Paramagnetic and Ferromagnetic Material)]]
==Both diamagnetic and paramagnetic materials have $\mu_r \simeq 1$==, more specifically: 
	- **Diamagnetic material**: $\mu_r \lt 1$ & $\mathcal{X}_M \simeq - 10^{-4}$
	- **Paramagnetic material**: $\mu_r \gt 1$ & $\mathcal{X}_M \in \left[+10^{-3} \div +10^{-5}\right]$
	- While **ferromagnetic material** shows "***hysteresis***", so $\mu_r$ is **not** constant:<br>![[Pasted image 20231120174743.png]]
- ***Terminology***:
	- $\mu_r$ : relative magnetic permeability
	- $\mathcal{X}_M$ : magnetic susceptibility $\left(\mu_r = 1 + \mathcal{X}_M \right)$
	- $H$ : magnetic field intensity $\left[H\right] = {\text{A}\over\text{m}}$
	- $M$ : magnetization $\left(M = \mu_0 \mathcal{X} H\right)$

---
###### [[SaM - Geometrical Magneto Resistance]]
- ***[[SaM - Drift Current • Current Density Equation|Current density equation]]***:$$\vec J = nq\vec v = \sigma \vec E$$Can be rewritten as:$$\vec v = \mu \vec E$$Where:$$\mu = {\sigma \over n q}$$
- ***Geometrical magneto resistance formula***:$$\vec v = \mu \vec E + \mu \kern2px (\vec v \times \vec B) $$
- ***Terminology***:
	- $\vec J$ : current density vector, $\left[J\right] = {\text{A} \over \text{m}^2}$
	- $n$ : [[SaM - Instrinsic Semiconductor • Density of Carriers • Energy Gap and Carriers Dependance on Temperature|density of carriers]].
	- $q$ : charge of an electron $\left(-1.6 \cdot 10^{-19} \ \text{C}\right)$ or of a [[SaM - Hole|hole]] $\left(+1.6 \cdot 10^{-19} \ \text{C}\right)$
	- $\vec v$ : velocity of carriers.
	- $\sigma$ : [[SaM - Conductivity and Mobility of Intrisinc Silicon|conductivity]] of the material.
	- $\vec E$ : [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|electric field vector]].
	- $\mu$ : [[SaM - Conductivity and Mobility of Intrisinc Silicon|mobility of carriers]].
	- $\vec B$ : [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetic field density]].

---
###### [[SaM - Drift Current • Current Density Equation]]
***Transport Current Equation in one dimension***:$$ J_n = \sigma_n E $$***Velocity of an electron***:
$$\vec v = \frac{q \tau}{m_e^*}\vec E$$***Relation between the avereage time between collisions ($\tau$) and the average free path ($\lambda$)***:$$\tau = \frac{\lambda}{V_{TH}}$$Where $v_{TH}$ is called the "***mean thermal velocity***", and it is defined as:$$V_{TH} = 4 \sqrt{\frac{kT}{2\pi m_e^*}}$$_The **transport current**, with a symmetrical distribution of carriers_:$$\vec J_n = n q \mu_n E$$
- ***Terminology***:
	- $m_e^*$ : effective mass

---
###### [[SaM - Types of Magneto Resistances]]
Given a certain [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetic field intensity]] $(H)$ a [[SaM - Magneto Resitances|magneto-resistive material]] will change its resisitivity.
- An **OMR** (*Ordany Mangeto Resitive*) material can change its reisitivity up to a $5\%$.
- There are also other types of mangeto resistances, these are all due to "*quantistic effects*":
	- **GMR** (*Giant Magneto Resitance*)
	- **CMR** (*Colossal Magneto Resitance*)
	- **TMR** (*Tunnel effect Magneto Resitance*)
---
###### [[SaM - Anisotropic Magneto Resistance (AMR) • Easy Axis • Barber Pole • Honeywell]]
- Materials that present AMR, like: _Ni_, _Fe_ and _Permalloy_ (_Fe_ +  _Ni_).
- ***AMR Formula***:$$\rho(\theta) = \rho_{\parallel} - \Delta{\rho} \cdot \sin^2\theta $$
- **Easy axis** $(x)$, an axis taken in the same direction of $\vec M_r$ 
- If we have that $\vec H_{\text{ext}} \ll H_S$ than we can approximate:$$\sin \theta \approx {H_y \over H_S}$$
- ***AMR Formula using the approximation***:$$\rho \simeq \rho_{\parallel} - \Delta \rho \left({H_y \over H_S}\right)^2$$
- ***Total resisitance value***:$$R \simeq R_0 \left(1- \frac{\Delta R}{R_0}\left(\frac{H_y}{H_S}\right)^2\right)$$Where:$$\begin{array}{l} \Delta R = \Delta \rho \cdot {l \over S} \\[3px] \Delta \rho = \rho_{\parallel} - \rho_{\perp} \\[3px] R_0 = \rho_{\parallel} \cdot {l \over S}    \end{array}$$
- ***Graph of $\rho(\theta)$ given $\theta$***:<br>![[Pasted image 20230718200022.png|500]]
- _At $\theta \approx 45°$ the sensor behaves linearly_.
- ***Rotate the current $45°$ with a barber pole***:<br>![[Pasted image 20230718200035 - Copia 1.png|500]]
- ***Simplified resistance formula for a barber pole***:$$R(H) \approx R_0 \mp \Delta R \kern2px {H_y\over H_S}$$
- ***Honeywell*** or ***resistive bridge***:<br>![[Pasted image 20230718200128 1.png|300]]
- ***Formula of the Honeywell***:$$V_{\text{TH}} = \alpha_r \cdot V$$We can also calculate the relative sensitivity $(\alpha_r)$ as: $${V_{\text{TH}} \over V} = {\Delta R \over R_0}\kern2px {H_y \over H_S}$$Remember that:$\Delta R = \left(\rho_{\parallel} - \rho_{\perp}\right) \cdot {l \over S}$
- ***Magnetic angle sensors formula***:$$\tan \left(2 \kern1px \theta \right) = {V_{\text{THA}} \over V_{\text{THB}}}$$Where:
	- $A$ or $V_{\text{THA}}$, refers to a honeywell bridge sensing along the $x$ axis.
	- $B$ or $V_{\text{THB}}$ refers to the honeywell bridge sensing along the $y$ axis.
- ***Terminology***
	- $\Delta \rho = \rho_{\parallel} -\rho_{\perp}$
		- $\rho_{\parallel}$ is the resisitivity when $\theta = 0°$.
		- $\rho_{\perp}$ is the resisitivity when $\theta = 90°$.
	- $\theta$ is the angle formed by $\vec J$ and $\vec M$, where:
		- $\vec J$ : current density vector, $\left[J\right] = {\text{A} \over \text{m}^2}$
		- $\vec M$ is the [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|total magnetization vector]], accounting for the external magnetic filed $\vec H_{\text{ext}}$, and for the [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetization of the material]] $\vec M_r$, $\left(\vec M_r = \mu_0 \mathcal{X} \vec H_{\text{ext}}\right)$
		- $\vec H_{ext} = \kern2px <H_x,\ H_y>$
	- $H_S$ is the **saturation field**, it is a property of the material.
	- $\rho$ : [[SaM - Recap of Basic Components • Resistance, Capacitance, Inductance • Resistivity, Permittivity, Permeability|resisitvity]].
	- $V_{\text{TH}} = V_+ - V_-$ is the output. 
	- $\alpha_r$ is the [[SaM - Sensitivity|relative sensitivity]], and for this structures it is usually $10^{-3}$.
	- $V$ is the input voltage.
	- $\vec B = \mu_0 \kern2px \vec H_{\text{ext}}$ is the [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|external magnetic field density]].

---
###### See Also
- [[SaM - MEMORIZE (Inductive Sensors)]]

---
