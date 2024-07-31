1. [[SaM - Definition of CMRR (Common Mode Rejection Ratio)|CMRR defintion]]:$$\text{CMRR} = \frac{|A_d|}{|A_C|} = \frac{A_2-A_1}{2(A_1+A_2)}$$
2. [[SaM - Differential Amplifier|Circuit definition]]:<br>![[Pasted image 20230718184020 1.png|333]]
3. Find $A_1$ ([[SaM - Inverting Operational Amplifier|inverting amplifier]]):$$A_1 = \left.\frac{V_0}{V_1}\right|_{V_2 = 0} = -{R_2 \over R_1}$$
4. Find $A_2$ ([[SaM - Non-Inverting Operational Amplifier|non-inverting amplifier]]):$$A_2 = \left.\frac{V_0}{V_2}\right|_{V_1 = 0} ={R_4\over R_3 + R_4}\cdot \left(1+{R_2 \over R_1}\right)$$
5. Calculate $A_d$ and $A_c$:$$\begin{array}{l} A_d =  {\large{1 \over 2}} \left( {\large{R_4 \kern2px (R_2+R_1) \over (R_3 + R_4) \kern2px R_1}} + {\large{R_2 \over R_1}} \right) \\[3px] A_c =  {\large{R_4 \kern2px (R_2+R_1) \over (R_3 + R_4) \kern2px R_1}} - {\large{R_2 \over R_1}}  \end{array}$$
7. Calculate the CMRR:$$\text{CMRR} = \frac{|A_d|}{|A_C|} = {1 \over 2} {{\large{R_4 \kern2px (R_2+R_1) \over (R_3 + R_4) \kern2px R_1}} + {\large{R_2 \over R_1}} \over {\large{R_4 \kern2px (R_2+R_1) \over (R_3 + R_4) \kern2px R_1}} - {\large{R_2 \over R_1}}}$$
%%6. Simplify it: $$\text{CMRR} = {1 \over 2} +  {R_2 (R_3 + R_4) \over R_1R_4 - R_2R_3}$$%%

---
###### Memory Card
![[Samsung_SaM_Notes_13_240515_175715_2.jpg]]

---