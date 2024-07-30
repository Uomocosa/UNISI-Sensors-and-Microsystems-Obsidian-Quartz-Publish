##### List of things to memorize:
- General Lumped Parameter System
- Thermal Domain
- Mechanical Domain
- Magnetic Domain
- Acustic Domain

---
###### General Lumped Parameter System

|                           | General [[SaM - Lumped Parameter Systems\|lumped parameter system]] | Electrical System |
| ------------------------- | ------------------------------------------------------------------- | ----------------- |
| ***Effort Quantity***     | $Y(s)$                                                              | Voltage: $V(s)$   |
| ***Flow Quantity***       | $X(s)$                                                              | Current: $I(s)$   |
| ***Generated Impedance*** | $Z(s) = {Y(s) \over X(s)}$                                          | Resistance: $R$   |

| System | *Effort Quantity* | *Flow Quantity* | *Impedances* |
| ---- | ---- | ---- | ---- |
| ***Thermal Domain*** | *Temperature Difference*:$$\Delta T(s)$$ | *Heat Flux*:$$\dot Q(s)$$ | *[[SaM - Heat Convection • Thermal Resistance\|Thermal Resisitance due to Convection]]*:$$R_{\text{TH}} = {1 \over hA}$$*[[SaM - Heat Conduction • Thermal Resistance\|Thermal Resisitance due to Condution]]*:$$R_{\text{TH}} = {t \over kA}$$*[[SaM - Heat Stored in a Body • Thermal Capacitance\|Thermal Capacitance]]*:$$C_{\text{TH}} = c \cdot V$$ |
| ***Mechanical Domain*** | *Force*:$$F = ma$$ | *Speed*:$$\dot x$$ | *A Spring is modelled as a Capacitance*:$$C= {1 \over k}$$<br>*A Damper is modelled as a Resistance*:$$R = \lambda$$*A mass is modelled as an Inductance*:$$L = m$$ |
| ***[[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|Magnetic Domain]]*** | *Magneto Motive Force*:$$\text{MMF} = N \cdot I$$ | *Flux of the Magnetic Field*:$$\phi(B) = \mu H S$$ | _Reluctances are modelled as a resistance_:$$\mathcal{R} = {l \over \mu S}$$_**Permanent Magnets** are modelled as a Voltage genrator and a relactance, so_:$$\begin{array}{l}  \mathcal{R}_M = \large{l_M \over \mu_M S_M}  \\[3px]  \text{MMF} = \mathcal{R}_M \cdot \phi(B_r)  \\[3px]  \phi(B_r) = S_M \cdot B_r = \mu_0 \cdot S_M \cdot M_r  \end{array}$$ |
| ***[[SaM - Acustic Impedance • Ultrasonic Lumped Parameter System\|Acustic Domain]]*** | *How fast the wave changes form*:$$\dot u$$ | *Stress (for Solids)*:$$\overline{\overline{T}}$$*Preassure (for Liquids)*:$$p$$ | _**Acustic Impedance**_:$$\begin{array}{l} \text{fluids:} & Z = {\huge{p \over \dot u_1}} \\[5px] \text{solids:} & Z = {\huge{T_{11}\over \dot u_1}}   \end{array}$$_Or_:$$Z = \rho \cdot v_l$$ |

---
###### Thermal Domain
- [[SaM - Heat Convection • Thermal Resistance|Heat Convection]]:$$\begin{array}{l} R_{TH}={\large \frac{1}{h\cdot A}} \\[3px] [h] = {\large{\text{W} \over \text{°K}}} \end{array}$$
- [[SaM - Heat Conduction • Thermal Resistance|Heat conduction]]:$$\begin{array}{l}  R_{TH}={\large\frac{t}{k\cdot A}} \\[3px]  \left[k\right] = {\large{\text{W} \over \text{°K}\cdot \text{m}}}    \end{array}$$
- [[SaM - Heat Stored in a Body • Thermal Capacitance|Heat Stored in a Body]]:$$\begin{array}{l} C_{TH}=c\cdot V  \\      \end{array}$$
- [[SaM - Thermal Lumped Parameter System|Examples for thermal lumped parameter systems]]:
	- ***Target + Ambient***:<br>![[Lecture 2_230905_175804_3 1.jpg|500]]
	- ***Sensor + Target***:<br>![[Lecture 2_230905_175804_4 1.jpg|500]]
	- ***Sensor + Target + Ambient***:<br>![[Lecture 2_230905_175804_4 2.jpg|500]]
- ***Terminology***:
	- $R$ : thermal resistance.
	- $h$ : convective heat transfer coefficient.
	- $k$ : thermal conductivity.
	- $C$ : thermal capacitance.
	- $c$ : specific heat.
	- $V$ : volume.
	- $T$ : temperature.
	- $\dot Q$ : heat flux.

---
###### Mechanical Domain
- **Generated Impendaces**:<br>![[Pasted image 20231124101933.png|333]]
- ***Example***:<br>![[Lecture 2_230905_175804_2 1.jpg|500]]
- ***Terminology***:
	- $k$ : elastic constant.
	- $\lambda$ : damping coefficient.
	- $m$ : mass.
	- $F$ : force $(F = ma)$.
	- $\ddot x = a$ : acceleration.
	- $\dot x$ : velocity.
	- $x$ : displacement.

---
######  [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|Magnetic Domain]]
- ***Magnetic Circuit with a Permanent Magnet (PM) (no Coil)***:<br>![[Pasted image 20230719112102.png|500]]
- ***Model with a Coil (no Permanent Magnet)***:<br>![[Pasted image 20230719112153 1.png|500]]
	- ***Formulas***:$$\begin{array}{l}  \mathcal{R}_g = \large{l_g \over \mu_0 S_g}  \\[3px]  \mathcal{R}_c = \large{l \over \mu_{\small{C}} S_C}  \\[5px]  \phi(B) = B \cdot S, \kern25px B = \mu H  \\[7px]  \phi(B) = \normalsize{\mu_0 \kern2px H_g S_g} = \normalsize{\mu_{\small{C}} \kern2px H_C S_C}  \end{array}$$
- ***Magnetic Circuit with Coil and Permanent Magnet (PM)***:<br>![[Pasted image 20230719112222 1.png|333]]
- ***Permament Magnet Model***:<br>![[Pasted image 20230719112222 2.png]]
	- ***Formulas***:$$\begin{array}{l}  \mathcal{R}_M = \large{l_M \over \mu_M S_M}  \\[3px]  \text{MMF} = \mathcal{R}_M \cdot \phi(B_r)  \\[3px]  \phi(B_r) = S_M \cdot B_r = \mu_0 \cdot S_M \cdot M_r  \end{array}$$
- ***Complete Model***:<br>![[Pasted image 20230719112237 1.png|500]]
	- ***Formula***:$$\begin{array}{l} v = -N{\large{d\phi(B) \over dt}} = \\ = -{\large\frac{N^2}{\mathcal{R}_{TOT}}\frac{dI}{dt}} + \left({\large\frac{N^2}{\mathcal{R}_{TOT}^2}} I+ {\large\frac{N}{\mathcal{R}_{TOT}^2}}\text{MMF}_{eq}\right){\large\frac{d\mathcal{R}_{TOT}}{dt}}      \end{array}$$
- ***Terminology***:
	- $\mu_r$ : [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|realtive magnetic permeability]].
	- $\mu_0$ : [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|vacum magnetic permeability]] $(\mu_0 = 4\pi \times 10^{-7} \, {\text{T}\cdot \text{m}\over \text{A}})$.
	- $l$ : lenght.
	- $S$ : surface.
	- $\mathcal{R}$ : [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|reluctance]].
	- $\text{MMF}$ : [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|magneto motive force]].
	- $\phi(B)$ : [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|flux of the magnetic field]].
	- $N$ : number of turns of the coil.
	- $I$ : current flowing in the coil.
	- $B$ : [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetic field density]].
	- $H$ : [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetic field intensity]] $(B = \mu H)$.
	- $M$ : [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetization]] $\left(M = H\cdot (1 + \mu_r),\kern25px B = \mu_0 (H + M)\right)$.
	- $v$ : [[SaM - Magnetic Lumped Parameter System • Electro-Motive Force • Variable Reluctance|elettro motive force]] $(v = -V), \kern15px V$ : voltage.

---
###### [[SaM - Acustic Impedance • Ultrasonic Lumped Parameter System|Acustic Domain]]
- ***Generated Impedance***:$$\begin{array}{l} \text{fluids:} & Z = {\huge{p \over \dot u_1}} \\[5px] \text{solids:} & Z = {\huge{T_{11}\over \dot u_1}}\\[9px] \text{general:} & Z = {\rho \cdot v_l }    \end{array}$$
- ***Measure Unit***:$$\left[Z\right] = \text{Rayl} = {\text{kg} \over \text{m}^2 \kern2px \text{s}}$$
- $v_l = \sqrt{c_{11} \over \rho}$
- ***Relation between $\dot u_1$ and $v_l$***:$$\dot u_1 = -{T_{11} \over \rho}{1 \over v_l}$$
- ***Terminology***:
	- $Z$ : [[SaM - Acustic Impedance • Ultrasonic Lumped Parameter System|acustic impedance]].
	- $p$ : preassure.
	- $T_{11}$ : [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|stress]].
	- $\dot u$ : _how fast the [[SaM - Ultrasonic Waves|wave]] changes form_.
	- $v_l$ : [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|longitudinal propagation velocity of the wave]].
	- $\rho$ : [[SaM - Recap of Basic Components • Resistance, Capacitance, Inductance • Resistivity, Permittivity, Permeability|resisitivity]].
	- $c_{11}$ : elastic constant, specifically this is from the [[SaM - Collapsed Stiffness Tensor for Isotropic Materials|collapsed stiffness tensor]].
