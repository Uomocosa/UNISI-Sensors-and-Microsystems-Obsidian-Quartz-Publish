Look at this structure:
![[Pasted image 20231106192634.png|500]]
We can define $V_2'-V_1'$ and $V_2'+V_1'$ based on $V_1$ and $V_2$, so:
$$(V_2' - V_1') = \frac{(2R_B + R_G)}{R_G}(V_2 - V_1)$$
But we also have that:
$$V_2'+V_1' = V_2+V_1$$

> **NOTE**: #IMPORTANTE 
> $R_B \simeq 50 \ \text{k}\ohm$

We have calulated the [[SaM - CMRR (Common Mode Rejection Ratio)|CMRR]] for the [[SaM - CMRR • Calculation of the CMRR for the Second Stage of an Instrumentational Amplifier|next stage]], already and we found:$$\text{CMRR}_{II} = \frac{1}{2} \large \frac{\frac{R_4}{R_3+R_4}\frac{1}{\beta}+\frac{R_2}{R_1}}{\frac{R_4}{R_3+R_4}\frac{1}{\beta}-\frac{R_2}{R_1}}$$Or:$$\text{CMRR}_{II} =  {1 \over 2} +  {R_2 (R_3 + R_4) \over R_1R_4 - R_2R_3}$$
If we add what we just said:
- $(V_2'- V_1') = \large \frac{(2R_B + R_G)}{R_G} \normalsize (V_2 - V_1)$
- $(V_2'+V_1') = 1\cdot(V_2+V_1)$

So we can say:
$$\begin{matrix} 
& \text{CMRR}_{TOT} = \\[5px]
& = \frac{1}{\frac{(2R_B + R_G)}{R_G}}\cdot \text{CMRR}_{II} \\[5px]
& = \frac{R_G}{2R_B+R_G}\cdot \text{CMRR}_{II}\end{matrix}$$