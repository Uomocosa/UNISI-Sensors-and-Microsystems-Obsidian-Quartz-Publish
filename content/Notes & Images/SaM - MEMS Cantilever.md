##### ***Remeber***:
> - "*Cantilever*" in italian: "*Mensola*", "*Trave a sbalzo*"
> - Primary sensor for force are **Deformable Structures** and **Cantilevers**.
> - **Deformable Structures** change a force in a displacement:<br>![[Pasted image 20231119194947.png|333]]
> - While **Cantilevers** change a force in a **deflection** or in **two strains** (an **elongation** and a **compession**):<br>![[Pasted image 20231119195139.png|500]]
> - ==Both primary sensor apply a **linear transformation to the force**.==<br>That is, the "new quantity output" is the force scaled by a constant, decided by the specifics of the sensor:$$\text{new\_quantity} = \alpha \cdot F$$More specifically:
> 	- $\varepsilon = \alpha_{\text{stress}} \cdot F$
> 	- $D_z(x) = \alpha_{\text{deflection}} \cdot F$
> - The calculations of the coefficient for **MEMS Cantilever** are quite complex both in case for transformation in deflection and in strains, but you need to remember that: ==using the **MEMS Cantilever** for converting into **strain** results in a ***DIFFERENTIAL PRIMARY SENSOR***==, that means that the output is **differential**:<br>![[Pasted image 20231127120608.png|500]]
> 	- We can take advantage of a differential output using a [[SaM - Differential Amplifier|Differential Amplifier]].

---
###### Memory Card
![[Samsung_SaM_Notes_06_240515_120818_3.jpg]]

---
![[Lecture 3_230907_175256_9 1.jpg]]
![[Lecture 3_230907_175256_10 1.jpg]]
