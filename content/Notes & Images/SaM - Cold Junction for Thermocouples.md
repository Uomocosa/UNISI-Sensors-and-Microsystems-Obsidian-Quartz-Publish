##### ***Remeber***:

> - ***Cold junction***: we keep one of  junctions of a [[SaM - Defintion of Thermocouples • Law of Thermocouples • Types of Thermocouples • Extension Wires|thermocouple]] at a controlled temperature, which we know the value of:<br>![[Pasted image 20230719115640 1.png|500]]
> - This way we have that the voltage measured is equal to:$$V_m = \int^{T_2}_{T_1} \sigma_{\kern-5px\small A} \kern2px dT  + \int^{T_1}_{T_c} \sigma_{\kern-3px\small B} \kern2px dT \int^{T_C}_{T_2} \sigma_{\kern-5px\small A} \kern2px dT  $$And we perform some calculations, we will obtain:$$V_m = V_{\kern-4pxAB}(T_1 ,\ T_c)$$Where: $V_{\kern-4pxAB}$ depends on both $\sigma_{\kern-5px\small A}$ and $\sigma_{\kern-3px\small B}$, and on $T_1$ and $T_C$.
> - ==Also since we know the temperature of $T_c$, or we can fix it at $0°\text{K}$, then we can calculate the **absolute temperature** $T_1$==.

> - We talk about **Cold Junction Compensation**, if we know at priori the temperature of the "cold junction".
> - Instead we talk about **Automatic Cold Junction Compensation**, if we measure the temperature of the "cold junction", like in this example:<br>![[Pasted image 20230719115647.png|400]]
> - We can measure the temperature $T_2$ with a [[SaM ~ Real World Example • Standard RTD Sensor • PT100 Sensor|PT100 absolute temperature sensor]], for example.

> - **NOTE**: Both the **PT100 sensor**, and a **thermocouple** with cold junction compensation, are **absolute temperature sensors**.<br>In many cases, thermocouples are preferred (instead of just a P100 sensor) for certain applications due to their wide temperature range and durability in harsh conditions.

---
###### Memory Card
![[Samsung_SaM_Notes_17_240515_185257_2.jpg]]

---
# Index
- [[#Cold Junction]]
- [[#Automatic Cold Junction Compensation]]

---
##### Cold Junction
We said that a thermocouple measures only the difference in temperature, so if we fix one of the two, with a **cold junction**, I can make a thermocouple into an absolute sensor:
![[Pasted image 20230719115640.png]]
- So I can measure $T_c$ accurately, with an independent **absolute** temperature sensor.
- ***What is the PT100 Device?***
	- The PT100 device, also known as a PT100 sensor or **PT100 resistance thermometer**, is a type of temperature sensor widely used in industrial and scientific applications for precise temperature measurement.<br>It is based on the principle of electrical resistance variation with temperature.
	- The "PT" in PT100 stands for "**Platinum Temperature**," indicating that the sensor is made of platinum, which is the primary material used in PT100 devices.<br>The "$100$" represents the **nominal resistance value of the sensor at $0$ degrees Celsius** (32 degrees Fahrenheit). 


---
##### Automatic Cold Junction Compensation
There is a more convenient way to solve this problem, and make the thermocouple into an absolute temperature sensor, which is all electric and automatic and this is called "**reference junction**".
And we speak about methods which are called "**automatic cold junction compensation**".
![[Pasted image 20230719115647.png]]
![[Pasted image 20230719115701.png]]
- Measure the temperature $T_2$ at the junction with a thermometer and add the value to the difference, so we obtain $T_1$.
- $V_G$ is a controlled voltage generator depending on $T_1$, so that $V$ will be equal to $V_{AB}(T_2, 0°C)$
- So it's linearly related to the temperature $T_1$, so usually I can simply build a voltage generator which transforms the temperature measurement into a voltage using the right sensitivity, the right coefficient, and then by putting it in series with my thermocouple I can obtain the compensation for the temperature of the cold junction.

---