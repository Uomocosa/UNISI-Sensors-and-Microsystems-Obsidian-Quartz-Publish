Here's the [[SaM ~ CMRR of a Simple Differential Amplifier|first stage]], just remembering these formulas:
- $V_0 = V_C A_C + V_d A_d$
- $V_d = V_2-V_1$ &$\kern3px$ $V_C = \frac{V_2+V_1}{2}$
- $A_d = \frac{A_2-A_1}{2}$  $\kern3px$&$\kern3px$ $A_C = A_2+A_1$

And the structure of the Stage II:
![[Pasted image 20231106193135.png|500]]

We first calculate $A_1$ for $V_1'$:
$$V_0|_{V_2'=0} = -\frac{R_2}{R_1}\frac{\beta A_d}{1 + \beta A_d}V_1'$$

Then $A_2$ for $V_2'$:
$$V_0|_{V_1'=0} = \frac{R_4}{R_3+R_4}\frac{1}{\beta}\frac{\beta A_d}{1 + \beta A_d}V_2'$$
So: 
$$A_1 = -\frac{R_2}{R_1}\frac{\beta A_d}{1 + \beta A_d}$$
$$A_2 = \frac{R_4}{R_3+R_4}\frac{1}{\beta}\frac{\beta A_d}{1 + \beta A_d}$$
Finally:
$$\text{CMRR}_{II} = \large \frac{1}{2} \frac{\frac{R_4}{R_3+R_4}\frac{1}{\beta}+\frac{R_2}{R_1}}{\frac{R_4}{R_3+R_4}\frac{1}{\beta}-\frac{R_2}{R_1}}$$
Remember:
$$\beta = \frac{R_1}{R_1+R_2}$$
###### Memory Card
![[Samsung_SaM_Notes_13_240515_175715_1.jpg]]

---