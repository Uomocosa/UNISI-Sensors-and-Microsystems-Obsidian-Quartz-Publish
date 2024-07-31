##### List of things to memorize:
![[SaM - Resistive Sensors]]

---
[[SaM - Potentiometer]]:$$R(x) = \rho \frac{x}{S}$$
- ***Terminology***:
	- $R$ : resistance.
	- $x$ : displacement.
	- $\rho$ : [[SaM - Recap of Basic Components • Resistance, Capacitance, Inductance • Resistivity, Permittivity, Permeability|resistivity]].
	- $S$ : surface.

---
[[SaM - Metal Strain Gauge • Passive Strain Sensor]]:
- ***Principle of operation*** & ***Strucutre***:<br>![[Pasted image 20231127191427 1.png|333]]<br>![[Pasted image 20231128114747 1.png|333]]
- ***Formula***:$$R=R_0(1+G\varepsilon_x)$$
- ***G (Gauge) Factor***:$$G=1+2\nu + c \kern3px (1-2\nu)$$
- ***Considering the Transverse Sensitivity***:$$R=R_0\left(1+G \kern2px \varepsilon_l + G_T \kern3px \varepsilon_T \right)$$
- ***Considering the Temperature Effect***:$$R=R_0(1 + \alpha T + G \varepsilon_x + G \varepsilon_{TH} + G_T \varepsilon_{TH})$$Where:$$\varepsilon_{TH} = (\lambda_S - \lambda_{TO})\cdot \Delta T $$
- ***Real World Quantities***:
	- $G\varepsilon_x \sim 0.1$ ⇒ variation of resisitance $\left(\Delta R \over R\right)$ is really small (*bad*).
	- $G \in [2  \div 4]$.
	- $R_0 \in [50 \ \ohm \div 700 \ \ohm]$.
	- $\alpha_{\text{TCR}} \in [10^{-5}°\text{C}^{-1} \div 10^{-6}°\text{C}^{-1}]$ ⇒ low [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|TCR]] (*good*).
- ***Terminology***:
	- $G$ : gauge factor.
	- $c$ : [[SaM - Piezoresistivity Effect|coefficient of piezoresisitivity]].
	- $\nu$ : [[SaM - Young and Poisson Modulus|Poisson modulus]].
	- $\varepsilon_x$ or $\varepsilon_l$ : parallel [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|strain]].
	- $\varepsilon_T$ : perpendicular [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|strain]].
	- $G_T$ : transverse gauge factor.
	- $\alpha$ or $\alpha_{\text{TCR}}$ : the [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|TCR]].
	- $\varepsilon_{TH}$ : thermal exampansion.
	- $\lambda_S$ : thermal exampsion coefficients of the **substrate**.
	- $\lambda_{TO}$ : thermal exampsion coefficients of the **metal grid**.
	- $T$ : temperature.
	- $\Delta T$ : temperature variation.

---
###### See Also
- [[SaM - MEMORIZE (RTD Sensor)]]
- [[SaM - MEMORIZE (Thermistor)]]
- [[SaM - MEMORIZE (Thermocouple)]]

---
###### [[SaM - Photoresistance]]
- ***Workings of a Photoresistance***:
	1. To use the "***photoelectric effect***", we need a **semiconductor** with [[SaM - Field Band of Silicon • Energy Gap, Valence Band, Conduction Band|energy gap]] $(E_g)$ less then the energy of a **photon** $(E)$.
	2. When a photon hits the material, it is able to free one electron from the [[SaM - Field Band of Silicon • Energy Gap, Valence Band, Conduction Band|valence band]] $(E_V)$ and promote it into the [[SaM - Field Band of Silicon • Energy Gap, Valence Band, Conduction Band|conduction band]] $(E_C)$. 
	3. So given a certain wavelength $(\lambda)$ we will obatin a response in the form of more [[SaM - Instrinsic Semiconductor • Density of Carriers • Energy Gap and Carriers Dependance on Temperature|free carriers]], so more conduction, ==⇒ **less resistance**==
- ***Energy of the photon***:$$E = \hbar \cdot \nu$$
- ***Minimum frequency***:$$\nu_{\min} = {E_g \over \hbar}$$
- ***Maximum wavelenght***:$$\lambda_{\max} = {c \cdot \hbar \over E_g}$$
- ***Conductance of a semiconductor***:$$G = (q \kern1px n \mu_n + q \kern1px p \mu_p) \cdot \frac{A}{l}$$
- ***Total resistance of a photoresistance***:$$R = A_x E_{\nu}^{-\alpha}$$
- _This is more like a **detector** then a real sensor_.
- ***Real World Measures***:
	- Visible light has a wavelength: $\lambda \in [0.4 \mu\text{m} \div 0.7 \mu\text{m}]$<br>And a corresponding energy: $E \in [1.78 \ \text{eV} \div 2.8 \ \text{eV}]$
	- Cadmium sulfide $(CdS)$ semiconductor has an $E_g = 1.8 \ \text{eV}$
	- $PbS$ : lead sulfide, $E_g = 0.4 \ \text{eV}$ (used in **Infra-Red Cameras**).
	- $PbSe$ : lead selenide, $E_g = 1.5 \ \text{eV}$ (used in **Infra-Red Cameras**).
	- ***$\alpha$*** : exponent for the photoresistance formula, is in the range $\alpha \in [0.7 ,\ 0.9]$
	- For a photoresistance we have usually this ratio: ${\large{R_{\text{ILLUMINATED}} \over R_{\text{DARK}}}} = 10^{-4}$
	- Photoresistances are slow devices: $\tau_{63\%} \approx 10 \ \text{ms}$
- ***Terminology***
	- $E_g$ : [[SaM - Field Band of Silicon • Energy Gap, Valence Band, Conduction Band|energy gap]].
	- $\lambda$ : wavelength.
	- $\nu$ : frequency.
	- $c \simeq 3 \cdot 10^{8} \frac{m}{s}$ : speed of light.
	- $\hbar = 6.626 \times 10^{-34} \kern2px J\cdot s$ : Planck's constant.
	- $G = {1 \over R}$ : [[SaM - Recap of Basic Components • Resistance, Capacitance, Inductance • Resistivity, Permittivity, Permeability|conductance]].
	- $q = -1.602 \times 10^{-19} \ \text{C}$ charge of the electron.
	- $A_x$ : ???
	- $E_{\nu}$ : **illuminance** is measured in ***lux*** (measure unit) $\left[\text{lux} = {\large{\text{cd} \cdot \text{sr}\over\text{m}^2}} \right]$
		- ***cd*** : candela (measure unit).
		- ***sr*** : steradian (measure unit).
	- $\tau$ :  [[SaM - Rise Time|rise time]].

---
![[SaM - MEMORIZE (Magnetism)#SaM - Geometrical Magneto Resistance]]

![[SaM - MEMORIZE (Magnetism)#SaM - Types of Magneto Resistances]]

![[SaM - MEMORIZE (Magnetism)#SaM - Anisotropic Magneto Resistance (AMR) • Easy Axis • Barber Pole • Honeywell]]

###### [[SaM - Chemical Resistive Sensor]]
- ***Structure***:
	1. Thick film ceramic resistances (==an inert material==).
	2. Two metal electrodes.
	3. An active layer (==a pourus material==, *~ex.: like a mox film*).
	4. Thick film metal resisitance on the backside (==a heater==).
- ***Topside view***:<br>![[Pasted image 20230718200234 - Copia 1.png|333]]
- ***Backside view***:<br>![[Pasted image 20230718200255 1.png|333]]
- ***Principle of Operation***:
	1. This sensor is based on **absorption**.<br>Meaning the **active layer** is a granular material that trap or absorb, different compounds.
	2. After being absorbed on the active layer, there is a transfer of charge from it (from the metal oxide - mox film) to the gas, and vice versa.<br>_~Ex.: ==oxygen tends to take an electron from the metal oxide, and it traps this electron, this negative charge, on the surface==_.
	3. We have a plus charge region under the surface, like in a **diode**.
	4. When many of these "diode-granes" are put togheter they resist the flow of current, so we have ==increased the reisitance of the sensor==.
- ***Sensitivity***:$$\alpha = {dR \over d [C]}$$
- ***Sensitivity to a different compound***:$$\alpha_x = {dR \over d [x]} \neq 0$$⇒ ==Chemical Resistive Sensor are **non-selective** devices==.
- ***Power used to opertate this device***:$$P_W = R_H \cdot I^2 = G \left(T_S - T_A\right)$$
- ***Conductivity of the device***:$$G = G_0 e^{-\huge\frac{q^2 N_S^2}{2\varepsilon K T_S N_D}}$$
- ***Other things to memorize***:
	- Chemical Resistive Sensor are **non-selective** devices.
	- This is more like a **detector** than a real sensor.
	- [[SaM - Chemical Resistive Sensor|Why we need a heater]].
	- [[SaM - Chemical Resistive Sensor|Why the temperature of the sensor should be kept constant]].
	- These sensors are **not so reproducible**.
	- The **humidity** (water vapor), always present in the environment, can influence the resitance value.
- ***Real World Measures***:
	- Thick film : $t \sim 100 \ \mu \text{m}$ ($t$ : thickness).
	- Thin film : $t \lt 10 \ \mu \text{m}$ ($t$ : thickness).
	- $T_S \in [150°\text{C},\ 450°\text{C}]$.
- ***Terminology***:
	- **inert** : meaning it doesn't interact with chemical compounds.
	- $[C]$ : specific compund the sensor is designed for.
	- $[x]$ : non-spefic compund the sensor is NOT designed for $([x] \neq [C])$.
	- $P_W$ : power of the overall device.
	- $G = {1 \over R}$ : [[SaM - Recap of Basic Components • Resistance, Capacitance, Inductance • Resistivity, Permittivity, Permeability|conductance]].
	- $q V_S$ : height of the potential barrier between each grain of the substrate.
	- $N_S$ : density of the absorbed and charged chemical compound.
	- $T_S$ : temperature of the sensor.
	- $N_D$ : [[SaM - Instrinsic Semiconductor • Density of Carriers • Energy Gap and Carriers Dependance on Temperature|density of donors]].
	- $k = 1.38\cdot 10^{-23} \ {\large{\text{J}\over\text{°K}}}$ : Boltzmann's constant.
	- $\varepsilon$ : [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|electric permittivity]] $(\varepsilon = \varepsilon_0 \varepsilon_r)$
		- $\varepsilon_0$ : electric permittivity of the void $\left(\varepsilon_0 = 8.85 \cdot 10^{-12} \ {\text{C}^2 \text{m}^2 \over \text{N}}\right)$
		- $\varepsilon_r$ : relative electric permittivity
