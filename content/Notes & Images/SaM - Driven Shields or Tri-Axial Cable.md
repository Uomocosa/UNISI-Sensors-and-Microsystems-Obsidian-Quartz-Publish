##### ***Remeber***:

> To reduce [[SaM - Electrical Noise|electrical noise]] we can [[SaM - Shields|shield]] our circuit, using a [[SaM - Coaxial Cable|coaxial cable]]
> However this does not solve the problem of having a [[SaM - Triboelectric Noise|long cable]].
> To solve both problems we need a **tri-axial cable**:<br>![[Pasted image 20230718201119.png|500]]
> - In this cables we have:
> 	- An **internal shield** called **guard** that surrounds the wire.
> 	- An **external shield** which is usually **grounded**.
> 	- In this types of cables the **guard** is kept at the same voltage as the wire.
> - The various coupling capacitances of the **tri-axial cables** are:
> 	- $C_G$ : **Guard capacitance** between wire and **internal shield**.<br>Tho since wire and **internal shields** are at the same voltage, this capacitance is empty of charge, so the special property of **tri-axial cables** is that:$$C_G = 0\kern2px F$$
> 	- $C_2$ : **Second shield capacitance**, this has charge, so its value is different from $0$.

> Let's draw better the circuit:<br>![[Pasted image 20230718201134.png|500]]
> - The sensor will see a capacitance $Z_i = C_{eq}$ equal to:$$C_{eq} = {C_G \over A + 1}$$
> - I will need an amplifier which has a **large gain**.<br>But remember that now we are operating at AC obviously, so it has to use **large frequency** because of the small value of the capacitance of the sensor ($C_S$).<br>Usually we need to operate, around the operating range (depending on the value of the sensor) of $100 \kern2px \text{kHz} \div 2 \kern2px \text{MHz}$.<br>⇒ So we need this **open loop gain** to be $\sim 100$ or $1000$, at around $1 \kern2px \text{MHz}$.
> - So in conjunction to tri-axial cables we need **wideband operational amplifiers**.
> - The last thing we need, since we have a variable signal, is a filter to remove the drifts at low frequency.

> I write here the equivalent we find at the end for the tri-axial cable system:<br>![[Pasted image 20230718201200.png]]

---
###### Memory Card
![[Samsung_SaM_Notes_21_240516_160358_7.jpg]]

---

So if we need a [[SaM - Triboelectric Noise|long cable]], we need to use tri-axial cables:
![[Pasted image 20230718201119.png]]
- In this cables we have:
	- An **internal shield** called **guard** that surrounds the wire.
	- An **external shield** which is usually **grounded**.
- In this types of cables the **guard** is kept at the same voltage as the wire.
- The various coupling capacitances of the **tri-axial cables** are:
	- $C_G$ : Guard Capacitance between wire and **internal shield**.<br>Tho since wire and **internal shields** are at the same voltage, this capacitance is empty of charge, so the special property of **tri-axial cables** is that:$$C_G = 0\kern2px F$$
	- $C_2$ : Second Shield Capacitance, this has charge, so its value is different from $0$.

Let's draw better the circuit:
![[Pasted image 20230718201134.png]]
- $C_G$ is the guard capacitance.
- $C_2$  is the outer shield capacitance.
- So the idea is to have changed this input resistance here ($Z_i$), so to have a reduced the effect of the capacitance of the cable.
- You see that the feedback, keeps the two terminal $+$ and $-$ at a very very close voltage with respect of one to the other, so almost a short circuit, no current flowing there.<br>So we don't have any effect in this case of loading and reduced sensitivity on the voltage divider in this part.

So:
![[Pasted image 20230718201144.png]]
- $C_{eq}$ is the capacitance seen by the sensor.
- I will need an amplifier which has a **large gain**.<br>But remember that now we are operating at AC obviously, so it has to use **large frequency** because of the small value of the capacitance of the sensor ($C_S$).<br>Usually we need to operate, around the operating range (depending on the value of the sensor) of $100 \kern2px \text{kHz} \div 2 \kern2px \text{MHz}$.<br>⇒ So we need this **open loop gain** to be, I don't know, $100$ or $1000$, at around $1 \kern2px \text{MHz}$.

So in conjunction to tri-axial cables we need **wideband operational amplifiers**.
![[Pasted image 20230718201152.png]]

The last thing we need, since we have a variable signal, is a filter to remove the drifts at low frequency.
There are still other problem, but at least we can the sensor even if we have a long cable.

I write here the equivalent we find at the end for the tri-axial cable system:
![[Pasted image 20230718201200.png]]
