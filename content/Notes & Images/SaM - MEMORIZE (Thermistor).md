##### List of things to memorize:
![[SaM - Thermistor]]

---
###### [[SaM - Definition of Thermistor]]
- _Thermistor are made of a **thick layer of ceramic** (**semiconductor**)_.
- _They are very common, and **cost less than [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|RTDs]]**_.
- ***Structure***:<br>![[Pasted image 20230713164346 1.png|333]]
- ***Principle of operation***: _we exploit the semi-conductive behavior of the ceramic material which gives us a **[[SaM - Thermal Activated Conductivity • Dependence of Conductivity on Temperature|thermally activated conductivity]]**_.
- ***Thermisotr have a [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|negative TCR (Temperature Coefficient of Resisitance)]] or NTC (Negative Temperature Coefficient)***:$$\text{TCR} = {dR \over dT}\cdot{1 \over R}\lt0$$
- ***Formula of the thermistor's resistance ***:$$R(T) = R_A \cdot e^{\large \kern2px \beta\left({1\over T} - {1 \over T_A}\right)}$$
- ***Real World Measures***:
	- $R_A$ : $R(T = T_A)$
		- $T_A$ : ambience temperature $\left(T_A = 300 °\text{K}\right)$
	- $\beta \in \left[3000 °\text{K} \div 5000 °\text{K} \right]$
	- Thermistor are of about $100 \ \mu\text{m}$ in lenght.
	- **Temperature range**: $T \in \left[-50 °\text{C} \div 150 °\text{C} \right]$. ([[SaM - MEMORIZE (Temperature Sensors)|here]] instead is defined differently)
	- Common values for the thermistor's resistance: $R \in \left[1.8 \ \text{k}\ohm \div 10 \ \text{k}\ohm \right]$.

---
###### [[SaM - Thermal Activated Conductivity • Dependence of Conductivity on Temperature]]
- _The [[SaM - Conductivity and Mobility of Intrisinc Silicon|conductivity]] of [[SaM - Instrinsic Semiconductor • Density of Carriers • Energy Gap and Carriers Dependance on Temperature|semiconductors]] also depends on **temperature**_.
- ***Graph of the conductivity for [[SaM - Doping of Silicon|n-type doped silicon]]***:<br>![[Lecture 6_230911_165051_8 1.jpg|500]]
- ***Graph of the conductivity for metals***:![[Lecture 6_230911_165051_8 2.jpg|500]]
- ***Terminology***:
	- $N_D^{+}$ : density of "ionazied" donors.<br>**NOTE**: The ionazied term means the dopants that contribuite to conduction, so the "active" dopants.<br>*~Ex.: in case of donors the electron that from the "donors extrinsix band" ($E_D$) has gone to the condution band*.

---
###### [[SaM - Steinhart-Hart Relashionship and Different Standard of Thermistor]]
- ***Equation***:$${1 \over T} = a + b \ln (R) + c \ln^3 (R)$$Where:
	- $a ={\large{1 \over T_A}} - {\large{\ln (R_A) \over \beta}}$
	- $b = {1 \over \beta}$
	- $c \approx 0$
	- $\beta \in \left[3000 °\text{K} \div 5000 °\text{K} \right]$
- ***Types of thermistor***:
	1. ***Standard precision***: $\text{accuracy} \in [0.1 °\text{C} \div 0.2 °\text{C}]$ with $T_{\text{RANGE}} \in [0 °\text{C} \div 70 °\text{C}]$.
	2. ***Extra precision***: $\text{accuracy} = 0.1 °\text{C}$ and large $T_{\text{RANGE}}$.
	3. ***Ultra precision***: $\text{accuracy} = 0.05 °\text{C}$ with $T_{\text{RANGE}} \in [0 °\text{C} \div 50 °\text{C}]$.
