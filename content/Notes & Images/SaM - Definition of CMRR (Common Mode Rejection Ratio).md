###### Memory Card
![[Samsung_SaM_Notes_13_240515_175715_1.jpg]]

---
![[Pasted image 20230626201407.png|333]]
- The sign is always positive. 
- And obviously ==for an ideal [[SaM - Differential Amplifier|differential amplifier]], we have a common mode rejection ratio, which is **infinite**==, since ideally $A_C = 0$.
- Where: $A_1$ and $A_2$ are the terminals of a differential amplifier.<br>Here is a simple schematic:<br>![[Pasted image 20230626201429 1.png|500]]
	- Idelly: $R_D=0$ and $R_{C1} = R_{C2} = \infty$.<br>Such that: $V_o' = A_dV_d$.

> We have also seen an [[SaM - Summary of the Calculation of CMRR for an Instrumentational Amplifier|example]], where we calculate the CMRR for an [[SaM - Instrumentational Amplifier|Instrumentational Amplifier]]. #IMPORTANTE 

---

Formula:
$$\text{CMRR} = \frac{|A_d|}{|A_C|} = \frac{A_2-A_1}{2(A_1+A_2)}$$
What you need to remember:
- $V_0 = V_C A_C + V_d A_d$
- $V_d = V_2-V_1$ &$\kern3px$ $V_C = \frac{V_2+V_1}{2}$
- $A_d = \frac{A_2-A_1}{2}$  $\kern3px$&$\kern3px$ $A_C = A_2+A_1$
- Where: 
	- $A$ is the **gain**.
	- $_d$ means "***differential***".
	- $_C$ means "***common mode***".

Professor's notes:
![[Pasted image 20230626201332.png|333]]
![[Pasted image 20230626201348.png|333]]
