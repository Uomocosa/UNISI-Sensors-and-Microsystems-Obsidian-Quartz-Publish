##### ***Remeber***:

> - The Calendar Van Dusen equation simplifies the relationship between the resistance of an [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|RTD]] to its temperature:$$R(T) = R_0 \cdot \left[1 + A  T + B  T^2 + CT^3 \cdot \kern2px (T - 100°) \right]$$Where:
> 	- $T$ is the temperature expressed in Celsius \[**°C**\], and it need to be $T\gt 0$**°C**
> 	- $R(T)$ is the resistance of the ***RTD*** at temperature $T$,
> 	- $R_0$​ is the resistance of the ***RTD*** at the reference temperature (usually $0$**°C**).
> 	- $A$, $B$, and $C$ are coefficients that depend on the specific ***RTD***.
> - Also in the previus formula we have considered $T\gt 0$**°C**, while if $T\lt 0$**°C** we need to discard the $C$ coefficient:$$R(T) = R_0 \cdot \left[1 + A T + B T^2 \right]$$
> - For the [[SaM ~ Real World Example • Standard RTD Sensor • PT100 Sensor|PT100 Sensor]] we have seen that the usual values are:
> 	- $A = 3.9 \times 10^{-3} \, \text{°C}^{-1}$
> 	- $B = -5.8 \times 10^{-7} \, \text{°C}^{-2}$
> 	- $C = -4.2 \times 10^{-12} \, \text{°C}^{-4}$
> 	- **NOTE**: We can also see the coefficent temperature $A$ as its [[SaM - Sensitivity|sensitivity]], but if we want a more accurate sensitivity (for example if we want a more precise accuracy at higher temperature $\overline{T}$) we might want to use the following formula:$$\alpha(\overline{T}) = \left.\frac{R_0A + 2R_0BT}{R_0}\right|_{T=\overline{T}}$$

> - For [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|RTD sensors]] also we have seen the ***TCR*** (Temperature Coefficient of Resistance), we can define as:$$\text{TCR}= {R_{100}-R_0\over100°C \cdot R_0}$$Where:
> 	- $R_{100}$ is the resistance the sensor assumes at $100°\text{C}$
> 	- $R_{0}$ is the resistance the sensor assumes at $0°\text{C}$
> 

> - We have also seen the [[SaM - Accuracy or Maximum Error|maximum error]] for using the **Calendar Van Dusen Equation**.<br>Here's how to find it:
> 1. Define the formula $f$: $R = f(T)$.<br>Which is the calander van dausen equation, so again:$$R(T) = R_0 \cdot \left[1 + A  T + B  T^2\right]$$(We didn't write the $C$ coefficient since it is really small, so we can ommit it for simplicity)
> 2. Define the inverse formula $T= f^{-1}(R)$.
> 3. Find the **Maximum Error** in the **Worst Case Possible**:$$\Delta T_{WC} = \frac{dT}{dA}\Delta A +  \frac{dT}{dB}\Delta B +  \frac{dT}{dR_0}\Delta R_0 +  \frac{dT}{dR}\Delta R$$Note that: 
> 	- $\frac{dT}{dR}\Delta R$ is the **maximum measurement error** and depends on the circuit used, not just on the sensor, ==so we forget about it==.
> 	- $\Delta A,\ \ldots ,\ \Delta R$ are the maxium possible variations, since we took the worst case possible.
> 4. Finally we perform the derivatives and find the formula for the maximum error.
> 5. To have a proper value we need to know the values $\Delta R_0 \over R_0$ and $\Delta A \over A$, which are the relative variations.
> 	- For the PT100 sensor we know that: ${\Delta R_0 \over R_0} = 6\cdot 10^{-4}$, or: $R_0 = 100\ohm \pm 0.06 \ohm$.
> 	- Also for **Class A Devices** the **Maximum Error** is $0.15 °\text{C}+0.002T$.<br>So it is important to note that even if a little, ==it depends on the temperature==.

---
###### Memory Card
![[Samsung_SaM_Notes_15_240515_183959_1.jpg]]

---
# Index
- [[#Defintion of the Calendar Van Dusen Relationship]]
- [[#Linearization]]
- [[#Errors and Accuracy of RTDs]]

---
##### Defintion of the Calendar Van Dusen Relationship
![[Lecture 8_230912_154531_8.jpg]]- There is an error:$$\text{TCR}= {R_{100}-R_0\over100°C \cdot R_0}$$

---
##### Linearization
![[Lecture 8_230912_154531_9.jpg]]

---
##### Errors and Accuracy of RTDs
![[Pasted image 20230713164236.png]]
![[Pasted image 20230713164252.png]]


