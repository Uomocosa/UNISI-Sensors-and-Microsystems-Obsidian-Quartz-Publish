- _This [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|RTD sensor]] is made of **platinum**, it is a standard material **very stable**, **reproducible** and **resist to oxidation**_
- If we describe this sensor using the [[SaM - Calendar Van Dusen Equation|Calendar Van Dusen Equation]], we usually have this values for the coefficients:
	- $A = 3.9 \times 10^{-3} \, \text{°C}^{-1}$
	- $B = -5.8 \times 10^{-7} \, \text{°C}^{-2}$
	- $C = -4.2 \times 10^{-12} \, \text{°C}^{-4}$
	- **NOTE**: We can also see the coefficent temperature $A$ as its [[SaM - Sensitivity|sensitivity]], but if we want a more accurate sensitivity (for example if we want a more precise accuracy at higher temperature $\overline{T}$) we might want to use the following formula:$$\alpha(\overline{T}) = \left.\frac{R_0A + 2R_0BT}{R_0}\right|_{T=\overline{T}}$$ 
- It is called **PT100** since it is made of platinum and the its resistance value assumed at $0 °\text{C}$ is $100 \ohm$.<br>While "**PT**" stands for *Platinum*.
	- *This sensor is made of **platinum**, it is a standard material, it is **very stable**, **reproducible** and it **resist to oxidation***
	- The value assumed by the PT100 at $0 °\text{C}$ is called $R_0$ or ***nominal resistance***.<br>And as mention above the PT100 has a nominal resistance $R_0=100 \ohm$.
	- The measured value can also change if the power it's high enough, so due to [[SaM - Self-Heating|self-heating]], of about $\simeq 0.5 {\text{°C} \over \text{mW}}$.
	- The usual [[SaM - Working Range & Safe Range|temperature range]] of these sensors is: $[-200°\text{C} \div 850 °\text{C}]$.
	- So if we consider $A = 3.9 \times 10^{-3} \, \text{°C}^{-1}$ as its sensitivity, we have that its resistance value has range: $[22\ohm \div 431 \ohm]$.

---
###### Memory Card
![[Samsung_SaM_Notes_15_240515_183959_2.jpg]]

---
![[Pasted image 20230713164154.png]]
