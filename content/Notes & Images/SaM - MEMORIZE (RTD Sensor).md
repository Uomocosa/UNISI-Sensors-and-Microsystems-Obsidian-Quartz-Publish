##### List of things to memorize:
![[SaM - RTD Sensor]]

---
###### [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)]]
- ***RTD (Resistance Temperature Detectors)***
- ***TCR (Temperature Coefficient of Resistance) formula***:$$\alpha_R = \frac{dR}{dT}\frac{1}{R}$$
	- ***PTC***: *Positive Temperature Coefficent* ($\alpha_R \gt 0$).
	- ***NTC***: *Negative Temperature Coefficent*  ($\alpha_R \lt 0$).
- ***TCR Definition for RTDs***:$$\text{TCR}= {R_{100}-R_0\over100°C \cdot R_0}$$
- ***Real World Measure***:
	- The usual [[SaM - Sensitivity|sensitivity]] of these sensors is: $\alpha \simeq +10^{-3} \ °\text{C}^{-1}$
	- *We have seen two tyes of RTDs*:
		- *Thin Films*:<br>![[Pasted image 20231121200250.png|200]]
		- *Wirewound*:<br>![[Pasted image 20231121200229.png|200]]
- ***Terminology***:
	- $R_{100}$ is the resistance the sensor assumes at $100°\text{C}$.
	- $R_{0}$ is the resistance the sensor assumes at $0°\text{C}$.

---
###### [[SaM - Calendar Van Dusen Equation]]
- ***Formula***:$$R(T) = R_0 \cdot \left[1 + A  T + B  T^2 + CT^3 \cdot \kern2px (T - 100°) \right]$$
- ***Simplified formula***:$$R(T) = R_0 \cdot \left[1 + A T + B T^2 \right]$$
- ***More accurate sensitivity***:$$\alpha(\overline{T}) = \left.\frac{R_0A + 2R_0BT}{R_0}\right|_{T=\overline{T}}$$
- ***Find the [[SaM - Accuracy or Maximum Error|maximum error]] for using the Calendar Van Dusen Equation***:
	1. Define the formula $f$: $R = f(T)$:$$R(T) = R_0 \cdot \left[1 + A  T + B  T^2\right]$$
	2. Find the inverse formula $T= f^{-1}(R)$.
	3. Find the **maximum error** in the **Worst Case (WC) possible**:$$\Delta T_{WC} = \frac{dT}{dA}\Delta A +  \frac{dT}{dB}\Delta B +  \frac{dT}{dR_0}\Delta R_0 +  \frac{dT}{dR}\Delta R$$Where:
		- $\frac{dT}{dR}\Delta R$ is the **maximum measurement error** and depends on the circuit used, not just on the sensor, ==so we forget about it==.
		- $\Delta A,\ \ldots ,\ \Delta R$ are the maxium possible variations, since we took the worst case possible.
- ***Real World Measure***:
	- For the [[SaM ~ Real World Example • Standard RTD Sensor • PT100 Sensor|PT100 sensor]]:
		- $A = 3.9 \times 10^{-3} \, \text{°C}^{-1}$
		- $B = -5.8 \times 10^{-7} \, \text{°C}^{-2}$
		- $C = -4.2 \times 10^{-12} \, \text{°C}^{-4}$
		- ${\Delta R_0 \over R_0} = 6\cdot 10^{-4}$, or: $R_0 = 100\ohm \pm 0.06 \ohm$.
	- For "**Class A Devices**" the **maximum error** is $0.15 °\text{C}+0.002T$.

---
###### [[SaM ~ Real World Example • Standard RTD Sensor • PT100 Sensor]]
- _This [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|RTD sensor]] is made of **platinum**, it is a standard material **very stable**, **reproducible** and **resist to oxidation**_
- _It is called **PT100** since_:
	- _It is made of platinum, "**PT**" stands for **Platinum**_. 
	- _Its nominal resistance $(R_0)$ value assumed at $0 °\text{C}$ is $100 \ohm$_.
- ***[[SaM - Calendar Van Dusen Equation|Calendar Van Dusen coefficients]]***:
	- $A = 3.9 \times 10^{-3} \, \text{°C}^{-1}$
	- $B = -5.8 \times 10^{-7} \, \text{°C}^{-2}$
	- $C = -4.2 \times 10^{-12} \, \text{°C}^{-4}$
- ***[[SaM - Self-Heating|Self-heating effect]]***: $\simeq 0.5 {\text{°C} \over \text{mW}}$.
- ***Usual [[SaM - Working Range & Safe Range|temperature range]] of these sensors***: $[-200°\text{C} \div 850 °\text{C}]$.<br>⇒ ***Usual resistance value range***: $[22\ohm \div 431 \ohm]$.

---
###### [[SaM - Accuracy of the Complete Measurement System]]
- ***Complete Measurement system***:<br>![[Pasted image 20231120190224.png|500]]
- ***Simple example using the [[SaM ~ Real World Example • Standard RTD Sensor • PT100 Sensor|PT100 sensor]]***:<br>![[Pasted image 20231120191120.png|500]]
- ***Accuracy of the complete system***:$$\alpha \triangleq \frac{dV_A}{dT} = I_{DC} \cdot A_0 \cdot A \cdot R_0$$Where:
	- $R_0$ : nominal resistance of the **PT100 sensor**.
	- $A$ : [[SaM - Calendar Van Dusen Equation|Calendar Van Dusen coefficient]].
	- $A_0$ : [[SaM - Operational Amplifier|open loop gain of the operational amplifier]].
	- $I_{DC}$ : current source.<br>A higher current improves the **SNR** (Signal to Noise Ratio), however it can create a [[SaM - Self-Heating|self-heating problem]].

---
###### [[SaM - Remove the Offset in the Measurement System]]
- ***Linear sensor (~Ex.: [[SaM - RTD Sensor|RTD]]) equation, taken within $T \in \left[T_{MIN} \div T_{MAX}\right]$***:<br>![[Pasted image 20240116182444.png|500]]
- ***Simplest read-out electronics***:<br>![[Pasted image 20240116182412.png|333]]
- ***Output formula***:$$V_0 = V_{DC} {R_{REF} \over R(T) + R_{REF}}$$
- ***Output graph***:<br>![[Pasted image 20240116183300.png|333]]
- ***Formulas***:$$\begin{array}{l} V_{0_{MIN}} = V_{DC} {\large{R_{REF} \over R_{MAX} + R_{REF}}} \\[5px] V_{0_{MAX}} = V_{DC} {\large{R_{REF} \over R_{MIN} + R_{REF}}} \\[5px] V_{\small {REF}} = V_{DC} {\large{R_{REF} \over R(T_{REF}) + R_{REF}}} \end{array} $$Where: 
	- $T_{REF}$ is taken as $T_{MAX} - T_{MIN} \over 2$.
	- $V_{\small {REF}}$ can be seen as the **offset** of the system.
	- While $\left[V_{0_{MIN}} ,\ V_{0_{MAX}}\right]$ is its **dynamic range**.
	- The information given by the sensor lies all in this small range that we will call $\Delta V$.
- ***Problem***: _we don't fully utlize the range given by the **acquisition system** (**A/D**)_.<br>***Solution***: *compensate the offset, so bring the output signal to have a $V_{\small{REF}} = 0$*:<br>![[Pasted image 20240116183919.png|500]]
- ***Using a [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|balanced bridge]]***:<br>![[Pasted image 20240116184017.png|500]]
- ***Problem***: _we might need to consider the [[SaM - 2 Wires Measurement with Wire Resisitances|wires resistances]]_.
- ***Problem***: _we have corrected the offset, but we cannot correct the **drift**, which is usually taken as_:$$V_{\text{drift}} = {1 \over 10} V_{\text{offset}} \kern25px (@\ 50°\text{C})$$

---
###### [[SaM - RTD Example • Linearized Uncertainty]]
- ***Circuit***:<br>![[Pasted image 20231124180519.png|500]]
- ***Output formula***:$$V_{RTD} = A_0\left[\left(V_{REF}-V_{io} - {V_{out}\over G_0}\right){R(T) \over R_{REF}}- V_{id}\right]$$
- ***The complete formula for this RTD circuit depends on***:
	1. $V_{REF}$
	2. $V_{io}$
	3. $V_{id}$
	4. $V_{out}$
	5. $V_{RTD}$
	6. $R_0$
	7. $A$
- ***Uncertanty formula***:$$u(T) = \left|{\partial T \over \partial V_{REF}}\right|u(V_{REF}) + \left|{\partial T \over \partial V_{io}}\right|u(V_{io}) + \ldots + \left|{\partial T \over \partial A}\right|u(A)$$
- ***Uncertanty simplified***:$$u(T) \le {R_{REF}\over R_0 \kern2px A_0 \kern2px A \kern3px V_{REF}}\cdot 10 \ \mu\text{V}$$
- ***Terminology***:
	- $A_0$ : open loop gain of the [[SaM - Differential Amplifier|differential amplifier]].
	- $V_{io}$ : [[SaM - Non-Ideal Operational Amplifier • OZE (Out of Zero Error) • Special Kinds of Operational Amplifiers • Precision Amplifier  • Low Noise • Low Input Bias Current • Zero Drift • Low Noise Operational Amplifier|voltage input offset]].
	- $V_{out}$ : output of the [[SaM - Operational Amplifier|operational amplifier]] $(G_0)$.
	- $G_0$ : open loop gain of the [[SaM - Operational Amplifier|operational amplifier]].
	- $R(T)$ : [[SaM - RTD Sensor|RTD sensor]].
	- $u(V_{REF})$ : "*drift of the reference voltage*".
	- $u(V_{io})$ : "*drift offset*" for the [[SaM ~ Real World Example • Standard RTD Sensor • PT100 Sensor|PT100]] it is about $\simeq 10\mu\text{V}$. #IMPORTANTE 
	- $u(V_{id})$ : "*drift offset*".
	- $u(V_{RTD})$ or $V_{LSB}$ : "*Voltage at the Least Significant Bit*".

---
###### [[SaM ~ Solution Based on a Resistive Bridge and an RTD]] 
(*Skipped*)
