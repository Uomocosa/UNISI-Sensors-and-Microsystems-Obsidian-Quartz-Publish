##### ***Remeber***:

> A conductive proximity sensor, without a target and with a conductive target:<br>![[Pasted image 20230718200559.png|500]]
> - No conductive target found, the measured capacitance will be a small value equal to $C_{\infty}$
> - Conductive target found, then $$C = \varepsilon \frac{A}{d}$$
> - So what happens is this:<br>![[Pasted image 20230718200617.png|333]]

> _What happens, instead, if I have a **large**, **conductive** target, which is also **not grounded**?_
> ⇒ The **parasitic capacitance** formed between the ground and target **can be ignored**.
> More specifically if: $$C_S \ll C_{GT}$$(*And this is true if the area of the sensor is much smaller that that of the target*)
> Then the parasitic capacitance $C_{GT}$ can be ignored:<br>![[Pasted image 20230718200647.png|500]]
> - $C_{MEAS}$: measured capacitance.
> - $C_S$ : sensor's capacitance.
> - $C_{GT}$ : parasitic capacitance between ground ($_G$) and target ($_T$).
> - ==If the **sensor is small** (if its area $A$ is small) relative to the **large target**==: Then we have that $C_S \ll C_{GT}$ and $C_{MEAS} \simeq C_S$.<br>⇒ ==So it's like always having a grounded conductive target, which is good==.

> We have seen an example of a capacitance sensor, with real world values, remember this:
> ==A **circular** capacitive proximity sensor with radius $r = 10 \text{ mm}$, measuring an object $1 \text{ mm}$ away will assume a capacitance of about $2.7 \text{ pF}$==.

> Remember, and this is **==very important==**, impedance of a capacitance in module is this one: $$| Z | = {1 \over \omega C_0}$$
> - ==**So small capacitance means high impedance**==.
> - If proximity capacitive sensor have a reasonable size, they will be a very **high impedance sensor**.
> - ==This **can be mitigated by operating this sensor at high frequency**, but we know that the higher the frequency the most critical is the design of the electronics==.
> - ==So we have to cope between these two requirements to **keep this impedance small enough to be measured** and to operate at a **not too high frequency**, in order for the design and for the parasitic effect which comes together with the high frequency electronic design==.

> ==Actually proximity sensors can be used also for non-conductive target, under the assumption that the electrical permittivity of the medium of the target is different from the one of the vacuum==:<br>![[Pasted image 20230718200707 - Copia.png|500]]
> When we have the target close to our measuring plate, the electrical field will find a medium with a different permittivity<br>⇒ ==**Like for conductive targets**, the capacitance measured by the sensor changes (it increases), if we get closer to the target, even if it is **non-conductive**==.<br>For this reason also a non-conductive target can be sensed.

---
###### Memory Card
![[Samsung_SaM_Notes_22_240516_105346_1.jpg]]

---
# Index
- [[#Capacitive Proximity Sensors]]
- [[#Large Non-Grounded Conductive Target for Capacitive Proximity Sensors]]
- [[#~Ex. Simple Sensor]]
- [[#High Impedance Sensor]]

---
##### Capacitive Proximity Sensors
![[Pasted image 20230718200559.png]]
- In the middle there is the sensing plate, which is polarized (biased)
- ==In a proximity sensor, what is needed is to sense the proximity of a **conductive target**==.<br>So we imagine to have a target, which is moving, and can arrive close to the sensing plate.
- This represents two conditions:
  1. No conductive target found, the measured capacitance will be a small value equal to $C_{\infty}$
  2. Conductive target found, then $$C = \varepsilon \frac{A}{d}$$

*How can I sense the presence of this target?*
![[Pasted image 20230718200603.png]]

This is a commercial proximity sensor:
![[Pasted image 20230718200608.png]]

So what happens is this: 
![[Pasted image 20230718200617.png]]
- $d$ : the distance of the target.
- $C$ : measured capacitance, which goes to the infinite value, which is the one related to this first condition (where no conductive target are present).

---
##### Large Non-Grounded Conductive Target for Capacitive Proximity Sensors
*What happens, instead, if I have a **large**, conductive target, which is also **not grounded**?*
⇒ We need to account for a non-ignorable **Parasitic Capacitance**:
![[Pasted image 20230718200647.png]]
- $C_{MEAS}$: Capacitance Measured
- $C_S$ : Sensor Capacitance.
- $C_{GT}$ : Parasitic Capacitance between ground ($_G$) and target ($_T$).
- ==If the **sensor is small** (if its area $A$ is small) relative to the **large target**==: Then we have that $C_S \ll C_{GT}$ and $C_{MEAS} \simeq C_S$.<br>⇒ ==So it's like always having a grounded conductive target==, which is good.

----
##### ~Ex.: Simple Sensor

> ***Remeber***:
> ==A **circular** capacitive proximity sensor with radius $r = 10 \text{ mm}$, measuring an object $1 \text{ mm}$ away will assume a capacitance of about $2.7 \text{ pF}$==.

Here we can see a numerical example of a simple capacitive sensor (no parasitic capacitances considered):
![[Pasted image 20230718200657.png]]
- $A$ : area of the sensor (radius of **1 cm**)
- $\varepsilon_0$ : absolute permittivity (we consider to have air as the isolating material, usual scenario).
- $C(d)$ : Sensor capapitance
- $C_0 = C(d=1\kern2px mm)$ : Capacitance for the sensor distance **1 mm** from the target.

---
##### High Impedance Sensor
Remember, and this is very, very important, impedance of a capacitance in module is this one:
![[Pasted image 20230718200707.png]]
- ==**So small capacitance means high impedance**==.
- So proximity capacitive sensor, if they have a reasonable size, they will be a very **high impedance sensor**.
- ==This **can be mitigated by operating this sensor at high frequency**, but we know that the higher the frequency the most critical is the design of the electronics==.

==So we have to cope between these two requirements to **keep this impedance small enough to be measured** and to operate at a **not too high frequency**, in order for the design and for the parasitic effect which comes together with the high frequency electronic design==.

---
##### Non-Conductive Target for Capacitive Proximity Sensors

![[Pasted image 20230718200707 - Copia.png]]
- ==Actually proximity sensors can be used also for non-conductive target, under the assumption that the electrical permittivity of the medium of the target is different from the one of the vacuum==.
- When we have the target close to our measuring plate, the electrical field will find a medium with a different permittivity<br>⇒ ==**Like for conductive targets**, the capacitance measured by the sensor changes (it increases), if we get closer to the target, even if it is **non-conductive**==.<br>For this reason also a non-conductive target can be sensed.