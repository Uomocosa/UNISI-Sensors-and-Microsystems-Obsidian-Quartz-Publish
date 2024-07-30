##### List of things to memorize:
![[SaM - Piezoresistivity]]

---
###### [[SaM - Piezoresistivity Effect]]
- ***Formula for metals***:$${d\rho \over \rho} = c {dV \over V}$$
- ***Formula for anisotropic materials (like doped Silicon)***:$${d\vec\rho \over \rho_0} = \overline{\overline{\Pi}}\cdot\overline{\overline{c}}\cdot\overline{\overline{\varepsilon}}$$
- ***Terminology***:
	- $\large {d\rho \over \rho}$ : infinitesimal change in resisitivity.
	- $\large {dV \over V}$ : infinitesimal change in volume.
	- $\overline{\overline{\Pi}}$ is the [[SaM - Piezoresistivity Effect in Details|piezoresistive coefficent tensor]].
	- $\overline{\overline{c}} \cdot \overline{\overline{\varepsilon}} =\overline{\overline{\sigma}}$ is the [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|Hooke's law]].
		- $\overline{\overline{c}}$ : stifness tensor (we have seen the [[SaM - Collapsed Stiffness Tensor for Isotropic Materials|stiffness tensor for isotropic materials]]).
		- $\overline{\overline{\varepsilon}}$ : [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|strain]] matrix (or displament matrix).
		- $\overline{\overline{\sigma}}$ : [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|stress]] matrix.
---
###### [[SaM - Recap of Basic Components • Resistance, Capacitance, Inductance • Resistivity, Permittivity, Permeability]]
- **Resistance** : $R =  \rho {\large\frac{l}{S}}$
- ***Condutance*** : $G = {\large{1 \over R}}$.
- **Capacitance** : $C = \varepsilon {\large\frac{A}{d}}$
- **Inductance** : $L = n^2\mu \kern2px{\large\frac{A}{l}} = n^2{\large\frac{1}{\mathcal{R}}}$
- ***Terminology***:
	- $\rho$ : resisitivity.
	- $\varepsilon$ : [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|eletric permittivity]].
	- $n$ : number of turns of a coil.
	- $\mu$ : [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetic permeability]].
	- $l$ : length.
	- $S$ : surface.
	- $A$ : area.
	- $d$ : distance
	- $\mathcal{R}$ : reluctance.

---
![[SaM - MEMORIZE (Stress and Strain • Strain and Stress)#SaM - Definition of Stress and Strain]]
![[SaM - MEMORIZE (Stress and Strain • Strain and Stress)#SaM - Young and Poisson Modulus]]
###### [[SaM - Piezoresistivity Effect in Details]]
- ***Electric field***:$$\begin{array}{l}  \text{Isotropic:} & \vec{E} = \rho_0  \cdot \vec{J}  \\  \text{Anisotropic:} & \vec{E} = \overline{\overline{\rho}}  \cdot \vec{J}   \end{array}$$
- ***Electric field in a deformed isotropic material***: $$\begin{array}{l}  \text{Isotropic (UNdeformed):} & \vec{E} = \rho_0  \cdot \vec{J}  \\  \text{Isotropic (DEFORMED):} & \vec{E} = \rho_0 \cdot \left(\overline{\overline{I}}+{\Delta \overline{\overline{\rho}} \over \rho_0}\right)  \cdot \vec{J}   \end{array}$$Where:$${\Delta \overline{\overline{\rho}} \over \rho_0} = \overline{\overline{\Pi}} \cdot  \overline{\overline{\sigma}}$$
- ***Terminology***:
	- $\vec E$ : [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|electric field]].
	- $\rho$ : resisitvity.
	- $\vec J$ : current density vector, $\left[J\right] = {\text{A} \over \text{m}^2}$
	- $\overline{\overline{I}}$ : identity matrix.
	- $\large {d\rho \over \rho}$ : infinitesimal change in resisitivity.
	- $\overline{\overline{\Pi}}$ is the [[SaM - Piezoresistivity Effect in Details|piezoresistive coefficent tensor]].<br> #TODO #NOT_SURE_ABOUT_THIS We probably defined it wrong, we made an example for *Silicon*, and it is the same as the [[SaM - Collapsed Stiffness Tensor for Isotropic Materials|collapsed stifness tensor]], but that is defined as $\overline{\overline{c}}$ in the [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|Hooke's law]].<br> #NOT_SURE_ABOUT_THIS This is probably also called the **piezoresistive factor**.
	- $\overline{\overline{\sigma}} = \overline{\overline{c}} \cdot \overline{\overline{\varepsilon}}$ is the [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|Hooke's law]].

---
![[SaM - MEMORIZE (Base Knwoledge on Sensors)#SaM - Definition of Isotropic and Anisotropic Materials]]
###### [[SaM - Crystallographic Axis]]
- $\left[h \kern2px k \kern2px l\right]$ defines a vector.
- $\left(h \kern2px k \kern2px l\right)$ defines a plane $\perp \left[h \kern2px k \kern2px l\right]$.
- $\left<h \kern2px k \kern2px l\right>$ defines a direction $\parallel \left[h \kern2px k \kern2px l\right]$.
- Typical cell for Silicon:<br>![[Pasted image 20230610190527.png|222]]
- ***Real World Measure***:
	- Typical surfaces: $\left(1 \kern2px 0 \kern2px 0\right)$, $\left(1 \kern2px 1 \kern2px 1\right)$, $\left(1 \kern2px 1 \kern2px 0\right)$, used in micromachining technology
	- For Silicon: $a = 543 \ \text{pm}$ (**Remember** : $p = 10^{-12}$)
- ***Terminology***
	- $a$ : length of the unit cell.
###### 
- - -
![[SaM - MEMORIZE (Stress and Strain • Strain and Stress)#SaM - Collapsed Stiffness Tensor for Isotropic Materials]]

---
###### [[SaM - Dependency of the Piezoresistance Factor on the Concentration of Dopants]]
- _The following fenomena happen for weakely doped silicon, meaning_: $N_D \ \text{or}\  N_A \lt 10^{19} \ \text{cm}^3$
- ***Change in the [[SaM - Piezoresistivity Effect|piezoresisitivity factor]] ($c$ or $\Pi$) due to the doping concentration***:<br>![[Pasted image 20230610194059.png|333]]
- ***Change in the TCR (Temperature Coefficient of Resisitance) due to the doping concentration***:<br>![[Pasted image 20230610194643.png]]
- ***Change in the temperature coefficient of sensitivity due to the doping concentration***:<br>![[Pasted image 20230610194744.png]]
- ***Terminology***:
	- $N_A$ or $N_D$ : [[SaM - Doping of Silicon|density of dopants]], acceptors and donors.
	- *Boron* $(\text{III group})$, is an acceptor.

---
###### [[SaM - Piezoresistance of Doped Silicon • Doped Silicon as a Strain Gauge]]
- [[SaM - MOSFET|How does a MOSFET work]].
- ***Setup***:
	1. Take a thin film of $n$-type doped silicon and place metal lines at both ends:<br>![[Pasted image 20230610200459 1.png|333]]
	2. We feed it a current:$$\vec J =  \left<J_1,\ 0,\ 0\right>$$
	3. We apply an [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|extensive stress]]:$$\vec \sigma = \left< \sigma_1,\ \sigma_2,\ 0,\ 0 ,\ 0 ,\ 0  \right>$$
	4. Eletric field: current + [[SaM - Piezoresistivity Effect|piezoresistive effect]]:$$\vec E = \rho \kern0px\cdot\kern-1px \left( \overline{\overline{I}} + \overline{\overline{\pi}}\cdot\overline{\overline{\sigma}} \right) \cdot \vec J$$
- ***If necessary you can rotate the $\overline{\overline{\pi}}$ tensor***:$$\pi' = N^{-1} \kern2px \pi \kern2px N$$
- ***For an uniaxial stress*** $\left(\vec \sigma = \left< \sigma_1,\ 0,\ 0,\ 0 ,\ 0 ,\ 0  \right>\right)$:$$E_1 = \rho_e \kern2px (1+G \varepsilon_1) \kern2px J_1 $$Where: $G = \pi_{11}' \cdot E$
- ***Voltage***:$$V = R_0 \kern2px (1+G \varepsilon_l) \kern2px I$$
- ***We can change the [[SaM - Crystallographic Axis|crystallographic axis]] and the voltage/current reading***:<br>*This will change the values of the $\overline{\overline{\pi}}$ matrix*:<br>![[Pasted image 20230611121245.png|333]]
- ***Terminology***:
	- $\vec J$ : current density vector, $\left[J\right] = {\text{A} \over \text{m}^2}$
	- $\vec \sigma$ : [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|stress]].
	- $\vec E$ : [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|electric field]].
	- $\overline{\overline{I}}$ : identity matrix.
	- $\varepsilon_1$ or $\varepsilon_l$ : [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|longitudinal strain]].
	- $G$ : [[SaM - Metal Strain Gauge • Passive Strain Sensor|gauge factor]].
	- $V$, $R$, $I$ : voltage, resistance, current.
---
