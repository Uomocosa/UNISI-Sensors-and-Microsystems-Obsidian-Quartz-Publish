##### List of things to memorize:
![[SaM - Temperature Sensors]]

---
###### [[SaM - Different Types of Temperature Sensors]]
- ***Table***:<br>(_Both [[SaM - RTD Sensor|RTDs]] and [[SaM - Thermocouples|thermocouples]] can operate at **very high temperatures**_)<br>(_Thermocouples have a **really simple structure** and the **best accuracy** and **high repeatability**, however they need [[SaM - Cold Junction for Thermocouples|cold junction compensation]] to be used as absolute sensors, and they have a **low voltage output**_)<br>(_[[SaM - Thermistor]] have the **lowest cost**_)<br>![[Pasted image 20230719115302.png]]

----
###### Study these:
- [[SaM - MEMORIZE (Thermocouple)]]
- [[SaM - MEMORIZE (RTD Sensor)]]
- [[SaM - MEMORIZE (Thermistor)]]

---
###### [[SaM - Sensors Based on Silicon Junctions (BJT and Integrated Circuits)]]
- ***Characterisitcs***:
	- Absolute temperature sensors.
	- We can find integrated circuits which behave **linearly**, and have **very good performances**.
	- Limited temperature range, like most **IC** $\approx 150°\text{C}$.
- ***BjT used as a constant current generator***:<br>(_There is a short-circuit between the base and the collector, therefore this device operates in the **active region**_)<br>![[Pasted image 20230719123638 1.png|250]]
- ***BjT active region formula***:$$V_{out} = V_{BE} = \frac{kT}{q}\ln\left({I_C \over I_S}\right) $$
- ***Real World Measures***:
	- For $T = T_A$ (ambience temperature), so $300\ \text{°K}$.
	- $V_{BE} = V_{out} = 600 \ \text{mV}$.
	- Ideally its [[SaM - Sensitivity|sensitivity]] would be $2 {\text{mV} \over \text{°K}}$.
	- Around $300°K$ if $I_S$ is not compensated, we have $\alpha = -4 {\text{mV} \over \text{°K}}$. #NOT_SURE_ABOUT_THIS (It is a huge difference)
- ***Terminology***:
	- **C** is the **collector**, **E** the **emitter**, and **B** the **base**.

---
###### [[SaM - Classical Band Gap Based Temperature Sensor (3 Pins)]]
- ***$N$ parallel BjTs***:<br>![[Pasted image 20240116121217.png|250]]
- ***Formula***:$$I_C = N \cdot  I_{C_2}$$Or:$$I_C = NI_{S_2} \kern2px e^{\frac{q V_G}{KT}}$$
- ***Classical band gap based temperature sensor structure***:<br>![[Pasted image 20230719123740 1.png|500]]
	- ***Output formula***:<br>(_It has a **linear dependance on temperature**_)$$V_{out} = {R_T \over R_1} \cdot {k \kern2px T \over q } \cdot \ln (N)$$
	- ***Real World Measures***:
		- Usual values for the [[SaM - Sensitivity|sensitivity]] for this kind of devices are in the range: $\alpha \in \left[2 \ {\text{mV}\over°\text{C}}\div 10 \ {\text{mV}\over°\text{C}}\right]$

---
###### [[SaM - Classical Band Gap Based Temperature Sensor (2 Pins)]]
- ***Circuit***:<br>![[Pasted image 20230923170203 1.png]]
- ***Equivalent circuit***:<br>(_The user has to select the resistance $R$_)<br>![[Pasted image 20230923170203 2.png|333]]
- _There are also integrated circuits that behave not as current generators but has **voltage generators**_:<br>![[Pasted image 20230719123853.png|333]]
