##### List of things to memorize:
![[SaM - Thermocouples]]

---
###### [[SaM - Defintion of Thermocouples • Law of Thermocouples • Types of Thermocouples • Extension Wires]]
- ***Thermocuple***: _two **conductive metal wires**, of **different materials**, in a "**[[Nabla Operand • Gradient • Divergence • Curl • Laplacian|gradient]] of temperature**"_.
- ***Electrical field formed in a single conductive metal immerged in a "[[Nabla Operand • Gradient • Divergence • Curl • Laplacian|gradient]] of temperature"***:$$\vec E = \sigma(T) \cdot \nabla T$$
- ***Basic example***:<br>![[Pasted image 20230719115316.png|500]]
- ***Simplest termocouple***:<br>![[Pasted image 20230719115341 1.png|500]]
- ***Formula***:$$\Delta V = \sigma_{\kern-4px AB} \cdot \Delta T$$Where: $\sigma_{\kern-4px AB} = \sigma_{\kern-4pxA} - \sigma_{\kern-2pxB}$.
- ***6 laws of thermocouples***:
	1. "_Law of homogeneus metals_":<br>![[Pasted image 20230923000457.png|333]]
	2. I only care about the two temperature **at the junctions**:<br>![[Pasted image 20230719115357.png|333]]
	3. Any piece of material that at his junctions has the same temperature does not change the voltage drop:<br>![[Pasted image 20230719115415.png|333]]
	4. Similar to the previous:<br>![[Pasted image 20230719115428.png|333]]
	5. "_Law of intermediate metals_":<br>![[Pasted image 20230923000415.png|333]]
	6. "_Law of intermediate temperatures_":<br>![[Pasted image 20230923000440.png|333]]
- ***[[SaM - Defintion of Thermocouples • Law of Thermocouples • Types of Thermocouples • Extension Wires|Extension wires]]***:<br>![[Pasted image 20230719115554.png|500]]<br>![[Pasted image 20230719115603 1.png|500]]
- ***Real World Masures***:
	- There are are $8$ types of thermocouples: **K**, **J**, **T**, **N**, (**B**, **R**, **S**), **I**:
		- **T** is the most accurate ($68\frac{\mu V}{°\text{C}}$)
		- (**B**, **R**, **S**) have the largest range (up to $1800°\text{C}$).
		- If you take a standard **class 1** - **J type** thermocouples, then you have an accuracy of about $\pm 1.5°\text{C}$ at $350°\text{C}$.
- ***Terminology***:
	- $\nabla T$ : **[[Nabla Operand • Gradient • Divergence • Curl • Laplacian|gradient]] of temperature**.
	- $\sigma$ or $\sigma(T)$ : "***seebeck coefficient***", it's a function of temperature.

---
###### [[SaM - Cold Junction for Thermocouples]]
- ***Cold junction***: _we keep one of the junctions of a [[SaM - Defintion of Thermocouples • Law of Thermocouples • Types of Thermocouples • Extension Wires|thermocouple]] at a controlled temperature_.
- ***Structure***:<br>![[Pasted image 20230719115640 1.png|500]]
	- _In this example, we know the temperature $T_C$.
- ***Cold junction compensation***: _we know **at priori** the temperature of the "cold junction", and we can compensate it from the output_.
- ***Automatic cold junction compensation***: _we measure the temperature of the "cold junction"_:<br>![[Pasted image 20230719115647.png|500]]
- _Another example for an automatic cold junction compensation, making the thermocouple an **absolute sensor**_:<br>![[Pasted image 20230719123624.png|500]]

---
###### [[SaM - Thermal Representation of a Thermocouple]]
- ***The [[SaM - Lumped Parameter Systems|lumped parameter system]], specifically the [[SaM - Thermal Lumped Parameter System|thermal lumped parameter system]] of a thermocouple***:<br>![[Pasted image 20230719123615.png|500]]
	- $T_X$ is my the temperature of the target body.
	- $T_2-T_1$ is what I sense.
	- ==The thermocouple is characterized by a very small capacitance ($C_1$), since it is a conductive metal==.
	- $T_A$ : ambience temperature.

---
###### [[SaM - Thermocouples (Class I & II)]]
- ***Reduced Range of [[SaM - Defintion of Thermocouples • Law of Thermocouples • Types of Thermocouples • Extension Wires|thermocouples]]***: _The **reduced range** is a range of temperatures more than the actual measurement range of the devices, in this range the error is "fixed"_.
- ***Extended Range of thermocouples***: _While **outside the reduced range**, you have also to account for **an additional error**, which scales with temperature, so the more you are outsude the range, the more the total error will be_.
- ***Class I thermocouples***: 
	- **Reduced range**: $[-40°\text{C} \div 375°\text{C}]$, **reduced range error**: $\pm 1°\text{C}$.
	- **Extended range error**: $0.004 °\text{C}^{-1}$
- ***Class II thermocouples***: 
	- **Reduced range**: $[0°\text{C} \div 333°\text{C}]$, **reduced range error**: $\pm 2.5°\text{C}$.
	- **Extended range error**: $0.0075 °\text{C}^{-1}$
- ***Equivalent electrical circuit of a thermocouple***:<br>![[Pasted image 20230719123559 1.png|333]]
	- $R_S$ is the resistance given by the thermocouple.
	- $\sim 40 {\mu \text{V} \over °\text{C}}$ represent a common [[SaM - Sensitivity|sensitivity]] for a thermocouple.

---
###### [[SaM - Thermopiles]]
- ***Structure***:<br>![[Pasted image 20230719123606.png|500]]
- ***Accuracy of a thermopile composed of $N$ identical thermcouples***:$$\alpha_{\text{thermopiles}} = N \cdot \alpha_{\text{thermocouple}}$$

---
###### [[SaM ~ Real World Example of a Classical Band Gap Based Temperature Sensor]]
- You have to add your own thermocouple.<br>⇒ The sensor is linear if your thermocouple is linear.
- **TMP35** sensor's sensitivity (pre-amplified): $\alpha = 41 {\mu\text{V} \over \text{°C}}$.
- **TMP35** sensor's sensitivity (post-amplified): $\alpha = 10 {\text{mV} \over \text{°C}}$.
