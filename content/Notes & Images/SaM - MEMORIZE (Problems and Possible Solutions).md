##### List of things to memorize:
![[SaM - Problems and Possible Solutions]]

---
![[SaM - MEMORIZE (Resistive Bridge • Wheatstone)#SaM - Definition of a Resistive Bridge • Balanced Bridge]]
###### 
![[SaM - MEMORIZE (Resistive Bridge • Wheatstone)#SaM - Design of a Resistive Bridge]]
###### 
![[SaM - MEMORIZE (Resistive Bridge • Wheatstone)#SaM ~ Resistive Bridge Example • Strain Gauge]]
###### 
![[SaM - MEMORIZE (Resistive Bridge • Wheatstone)#SaM ~ Half Bridge Example • Two Strain Gauges]]
######
![[SaM - MEMORIZE (Resistive Bridge • Wheatstone)#SaM - Half Bridge • Calculation for the Maximum Sensitivity of a Resistive Bridge]]
######
###### [[SaM - Types of Resistive Bridge Recap]]
- $1 \over 4$ bridge: ${\large{V_{TH} \over V}} = {\large{G\varepsilon \over 4}}$
- $1 \over 2$ bridge: ${\large{V_{TH} \over V}} = {\large{G\varepsilon \over 2}}$
- $1 \over 4$ bridge: ${\large{V_{TH} \over V}} = {{G\varepsilon}}$
- **ALL BRIGES reject the common mode disturbances** (DC errors).
- The half-brige has **improved relative sensitivity**, it is linear for $(1+K) \gg x$.
- The full-brige has **even more relative improved sensitivity**, it is always linear.

---
![[SaM - MEMORIZE (Resistive Bridge • Wheatstone)#SaM - Full Bridge]]
######
![[SaM - MEMORIZE (Resistive Bridge • Wheatstone)#SaM - Wire Resistance in a Resistive Bridge (2 and 3 Wires Layout)]]
######
###### [[SaM ~ Complete Sensor • Load Cell with a Resistive Bridge]]
- ***Structure***:<br>![[Pasted image 20240112173342.png|333]]
- ***Electrical model***:<br>![[Pasted image 20240112173532.png|222]]
- ***Formulas***:$$\begin{array}{l} \varepsilon_l={\large{\sigma_1 \over E}} \\[3px] \varepsilon_t= - \nu \varepsilon_l \\[3px] \sigma_1 = {\large{F_1 \over A}} \end{array}$$
- ***[[SaM - Metal Strain Gauge • Passive Strain Sensor|Strain gauge]] general formula***:$$R = R_0 \kern2px (1 + G\varepsilon )$$
- ***Specific formula for the four strain gauges***:$$\begin{array}{l} R_1 = R_0 \kern2px (1 + G\varepsilon_l ) \\ R_2 = R_0 \kern2px (1 + G\varepsilon_t ) \\ R_3 = R_0 \kern2px (1 - G\varepsilon_l ) \\ R_4 = R_0 \kern2px (1 - G\varepsilon_t ) \\ \end{array}$$
- ***Resisitive bridge formula***:$$V_{out} = V \left({R_1\over R_1 + R_4}-{R_2\over R_2 + R_3}\right)$$
- ***Final formula***:$$V_{out} = V \kern2px {G \kern2px (1+\nu) \kern2px  \over 2} \kern2px \varepsilon_l$$Or:$$V_{out} = V \kern2px {G \kern2px (1+\nu) \kern2px  \over 2} \kern2px {E \over A} \kern2px F_1$$
- ***Real World Measures***:
	- usually $\nu \simeq 0.35$.

---
![[SaM - MEMORIZE (Resistive Bridge • Wheatstone)#SaM ~ Complete Sensor • Accelerometer with a Resistive Bridge]]
######
###### [[SaM - 2 Wires Measurement with Wire Resisitances]]
- ***Structure***:<br>![[Lecture 9_230926_222449_4 2.jpg|500]]
- ***Total resistance formula***:$$R_{\small{\text{MEASURED}}} = R(T) + R_{{\small W1}} + R_{{\small W2}}$$

---
###### [[SaM - 4 Wires Measurement with Wire Resisitances]]
- ***Structure and formula***:<br>![[Lecture 9_230926_222449_5 2.jpg|500]]

![[SaM - MEMORIZE (RTD Sensor)#SaM - Remove the Offset in the Measurement System]]
######
![[SaM - MEMORIZE (Amplifiers)#SaM - Non-Ideal Operational Amplifier • OZE (Out of Zero Error)]]
######
###### [[SaM - Self-Heating]]
- ***[[SaM - Lumped Parameter Systems|Simple lumped thermal parameter system]]***:<br>![[Pasted image 20231123193338.png]]
- ***Meaured temperature at regime***:$$T_{S\infty}= T_X + R_{XS}\dot{Q}_S$$
- ***Measurement error***:$$\Delta T = R_{XS}\dot{Q}_S$$

---
###### [[SaM - Reduce the Effect of Self-Heating]]
- ***Using a "train of pulses"***:<br>![[Pasted image 20231124113031.png|500]]
- ***Calculations***:
	1. the self-heating depends directly on the average power $(\overline P)$:$$\overline P = {1 \over T} \int_{0}^{T_{on}} I^2(t) \cdot R \kern7px dt$$
	2. If we perform the calculation:$$\begin{array}{l} \overline P &=& {\huge{T_{on} \cdot I_0^2 \cdot R \over T}} \\[3px] &=& \delta \cdot I_0^2 \cdot R       \end{array}$$
	3. While respect to the **DC** approach:$$\overline{P}_{DC} = I_0^2 \cdot R$$It is reduced by a factor decided by the duty cycle $\delta$.

- ***Logaritmic voltage-current-power graph***:<br>![[Pasted image 20230601171409.png|400]]
- ***Formulas***:$$\log V = \log R + \log I$$And:$$\log V = \log P - \log I$$
- ***Visualize the effect of selh-heating on the measured resitance***:<br>![[Pasted image 20230601171543.png|500]]

---
###### [[SaM - Coupling with the Environment (and Solution)]]
- ***[[SaM - Lumped Parameter Systems|Simple lumped thermal parameter system]]***:<br>![[Pasted image 20240116192926.png|333]]
- ***Measured temperature at regime***:$$T_S(t) = T_S{_{\kern-1px \infty}}\left(1 - e^{-\large{t \over \tau}}\right)  + T_S\left(0^-\right) \kern2px e^{-\large{t \over \tau}} $$Where:$$\begin{array}{l} T_S{_{\kern-1px \infty}} = {\huge{T_A \kern2px R_{XS} \over R_{XS} + R_{SA}}} + {\huge{T_S \kern2px R_{SA} \over R_{XS} + R_{SA}}} \\[7px] \tau = C_S  {\huge{R_{XS} \kern2px R_{SA} \over R_{XS} + R_{SA}}} \end{array}$$
- ==***Solution***==: If $R_{SA} \gg R_{XS}$, then: $T_S{_{\kern-1px \infty}} \approx T_A$.
- ***Graph***:<br>![[Pasted image 20240116194241.png|500]]


| **thermal conductivity** ($K$)                                          | _Still Air_ | _Glass_ | _Gold_   | _Diamond_ |
| ----------------------------------------------------------------------- | ----------- | ------- | -------- | --------- |
| $K \left(\left[{\text{W} \over \text{°K} \cdot \text{m}}\right]\right)$ | $10^{-2}$   | $1$     | $10^{2}$ | $10^{3}$  |
- **_Still Air_ means**: "_A porous material filled with Air_", so we are talking about **only [[SaM - Heat Convection • Thermal Resistance|convection]]**, no [[SaM - Heat Conduction • Thermal Resistance|conduction]].
- A bigger coefficient means a **lower thermal resistance**, so a better coupling, and a **faster heat transfer**.<br>So "***still air***" is an **thermal insulator**.

---
###### [[SaM - Electrical Noise]]
- ***Example***:<br>![[Pasted image 20230718200937 1.png|500]]
- ***Formula***:$$V_R \kern2px {j\omega R_{in}C_{\text{COUP}} \over 1 +j \omega R_{in} (C_{\text{COUP}} + C_{TH} + C_P')}$$
- ***Bode Plot***:<br>![[Pasted image 20230718201005 1.png|500]]
- ***At low frequency, meaning: $f \ll f_p$, we can approximate as***:$$\frac{V_i}{V_d} \simeq j \omega R_{in} C_{COUP}$$
- ***Real World Measures***:
	- Especially in this case, if the resistance $R_{in}$ is small, the sensitivity of the circuit to electrical noise becomes smaller (a good thing).<br>⇒ ==It is better, if possible, to use a front end amplifier with **low resistance**==.<br>⇒ Meaning, that it's better to use [[SaM - Current Amplifier|current]], or [[SaM - Charge Amplifier|charge amplifiers]], so that we have the $R_{in}$ [[SaM - Current Amplifier|resistance very low]], resulting in a cutoff frequency $f_p$ very high.<br>**HOWEVER**: we cannot choose a too-small input resistance, since if I put the $R_{in}$ resistance at $0$, **I don't read anything** $\left(\frac{V_i}{V_d} = 0\right)$.
	- It would be better to have the $f_p$ cutoff frequency much larger than $50 \kern2px \text{Hz}$.<br>Since **the most important source of electrical noise is the power ==line wiring==**, that we have everywhere, and the power lines generate noise at $50 \kern2px \text{Hz}$. ("***White Noise***")
- ***Terminology***:
	- $V_R$ : reference voltage.
	- $C_R$: reference capacitance.<br>In other cases you can have no reference capacitance, for instance if you measure **humidity**.
	- $C_S$: sensor.
	- $C_{CABLE}$: in case of a long cable, i need to consider it.
	- $C_{COUP}$: parasitic capacitance with external electric potential $V_d$.<br>This $V_d$ could be for instance another appliance, or a person which moves.
	- $R_{in}$: input resistance to front-end electroncis.
	- $C_{P}$: parasitic capacitance (from the front-end electronics).
	- We can consider:
		- $C_P' = C_{\text{CABLE}} \parallel C_P$
		- $C_{\text{TH}} = C_R \parallel C_S$

---
###### [[SaM - Shields]]
- ***Simple shield structure***:<br>![[Pasted image 20230718201053.png|500]]
- _Inside the closed metallic surface ("shield"), the electrical field is zero, **due to the high mobility of charges**_.
- _Shields are especially useful when I can't use a [[SaM - Current Amplifier|current amplifier]]_.
- _The new $C_{\text{COUP}}'$ is much smaller then the un-shielded $C_{\text{COUP}}$_.
- **HOWEVER**: _the output still depends on $C_G$_. #NOT_SURE_ABOUT_THIS 

---
###### [[SaM - Coaxial Cable]]
- ***Structure***:<br>![[Pasted image 20230718201110 1.png|333]]
	1. ****Inner Conductor** or **Wire**.
	2. **1st Insulation**.
	3. **Outer Conductor** or **Elettromagnetic Shield**.
	4. **2nd Insulation.**
	5. **Outer Jacket** or **Durable Shield** (in particular this shield provides mechanical protection and shields the cable from environmental factors like moisture and physical damage).
- ***Electrical model***:<br>![[Pasted image 20230718201110 2 1.png|500]]
- ***Formula***:$$V_{in} = {C_R \over C_S + C_G + C_P + C_R}$$
- ***Real World Measures***:
	- For a coaxial cable, we can imagine to have a value of capacitance $C_G$, which is $100 \frac{\text{pF}}{m}$ multiplied by the length $l$ of the cable.<br>So if the the cable is long and $C_G$ is really big, it will "mask" the relativily small value of our sensor ($C_S$).<br>⇒ We will lose a lot of sensitivity.
	- A coaxial cable is not good if the **$C_S$ sensor's capacitance is small** and if the **cable is long** ⇒ so if $C_G \gg C_S$.
	- _~Ex.:_ $10$ meters of cable means $C_G \simeq 1 \text{nF}$, we have said that our $C_S$ in in the order of $0.1 \kern2px pF$, so ($10^{-13}$).<br>⇒ $C_G$ is **$10'000$ times larger than the capacitance of the sensor** $C_S$.
- ***Terminology***:
	- $C_G$ : **guard gapacitance**, which in this case is the cable capacitance.
	- $C_R$ : **reference capacitance**.
	- $C_S$ : sensor.
	- $R_{in}$: input resistance to front-end electroncis.
	- $C_P$ : parasitic capacitance (from the front-end electronics).

---
###### [[SaM - Driven Shields or Tri-Axial Cable]]
- ***Structure***:<br>![[Pasted image 20230718201119.png|500]]
	1. An **internal shield** called **guard** that surrounds the wire.
	2. An **external shield** which is usually **grounded**.
	3. In this types of cables the **guard** is kept at the same voltage as the wire.
- ***Electrical model***:<br>![[Pasted image 20230718201134.png|500]]
- ***Impedance seen by the sensor $(Z_i = C_{eq})$***:$$C_{eq} = {C_G \over A + 1}$$
- ***Equivalent electrical circuit***:<br>![[Pasted image 20230718201200.png|500]]
- ***Real World Measures***:
	- I will need an amplifier which has a **large gain**, to reduce the impedace $C_{eq}$, and a **wide band**, since we are operating at AC, so it has to use **large frequency** because of the small value of the capacitance of the sensor ($C_S$).<br>Usually the operating range (depending on the value of the sensor) is $100 \kern2px \text{kHz} \div 2 \kern2px \text{MHz}$.<br>⇒ So we need this **open loop gain** to be $\sim 100$ or $1000$, at around $1 \kern2px \text{MHz}$.
	- The last thing we need, since we have a variable signal, is a filter to remove the drifts at low frequency
- ***Terminology***:
	- $C_G$ : **Guard capacitance** between wire and **internal shield**.<br>Tho since wire and **internal shields** are at the same voltage, this capacitance is empty of charge, so the special property of **tri-axial cables** is that:$$C_G = 0\kern2px F$$
	- $C_2$ : **Second shield capacitance**, this has charge, so its value is different from $0$.

---
###### [[SaM - Tri-axial Cable + Tri-axial Sensor]]
- ***Normal [[SaM - Capacitive Proximity Sensors|capacitive proximity sensor]] and a tri-axial sensor***:<br>![[Pasted image 20230718201222.png]]
- _The field in the normal sensor, is bend at the edges, instead for a tri-axial sensor that is not the case, we consider the field as "almost ideal"_.
- _In the tri-axial sensor, the "**guard system**", prevents the distortion of the field due to something outside the sensing area_.
