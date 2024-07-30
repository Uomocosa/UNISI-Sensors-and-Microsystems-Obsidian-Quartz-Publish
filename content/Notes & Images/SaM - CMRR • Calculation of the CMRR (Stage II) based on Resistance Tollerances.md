Let's complicate the problem of calculating the [[SaM - CMRR (Common Mode Rejection Ratio)|CMRR]] of an [[SaM - Instrumentational Amplifier|instrumentational amplifier]].
We have seen [[SaM - CMRR • Design Rules for Resistance Values of an Instrumentational Amplifier|previously]] the even if we have a **non-ideal [[SaM - Operational Amplifier|op. amp.]]**, with a **finate open-loop gain** $(A \neq \infty)$, we can still have an **infinite CMRR**, as long as we have: ${R_2 \over R_1} = {R_4 \over R_3}$.

What happens, in a more realistic scenario, where we consider **different resistance ratios**, since having two resistence exactly equals is extreamly difficult, so:$$\begin{array}{l} {\large {R_2 \over R_1}} = K \\[3px] {\large {R_4 \over R_3}} = K' \end{array}$$Let's define the worst case scenario, if $K$ assumes the lowest possible value and $K'$ the highest, so we'll write it as:$$K' - K \triangleq 2\Delta K_{\max}$$And define the **resistance tollerance**:$$\large \varepsilon_{\small \kern-2px R} \normalsize \triangleq \frac{\Delta R_{\max}}{R} = \frac{\Delta K_{\max}}{K}$$
For **semplicity** we don't consider **no contribution** from the operational amplifier common mode rejection ratio, so I'm accounting only for the fact that the resistances ($R_1 ,\ \ldots ,\ R_4$) are not precisely what I would like to have from the design, so tolerances of the resistances.<br>That's why we will call it "$\text{CMRR}_{R}$".

Let's calculate the CMRR$_{R}$ based on this new rule:$$\begin{array}{l} A_1 = -K \\A_2 = {\huge{K' \over 1+K'}}(1+K) \end{array}$$So: #IMPORTANTE $$\text{CMRR}_R = {2 K (1 + K) \over K'-K}$$[[SaM - Lecture 12_02 • CMRR • Calculations|Here]]'s the calculations.
We can the use the definition we have given for the **resistance tollerance** $(\varepsilon_{\small \kern-2px R})$
$$\text{CMRR}_{R} = \frac{1+K}{4 \kern2px \large \varepsilon_{\small \kern-2px R}}$$If we consieder: $R_1 = R_2 = R_3 = R_4$ (so $K = 1$)
We obtain that the last stage of the CMRR due only to resistance tollerances is given by:
$$\text{CMRR}_{R} = \frac{1}{2 \kern2px \large \varepsilon_{\small R}}$$
> **NOTE**: #IMPORTANTE 
> Usually we find: $\large \varepsilon_{\small R} \normalsize  = \frac{10^{-4}}{2}$
> So the $\text{CMRR} \simeq 10^{4}$<br>
> If these resistances are realized in an **integrated circuit** (**IC**), so with the same process, at the same moment, very close one to the other, then the matching is a parameter that could have a very high accuracy.
> This is the reason why we can't build our own instrumentation amplifier we have to buy it, in an integrated form.

---

If we want to get the **complete CMRR**, also considering the contribution based on the resistances' tollerance, we can calculate:$${1 \over \text{CMRR}_{II_\text{(R+OP.AMP.)}}} = {1 \over \text{CMRR}_{II_\text{R}}} + {1 \over \text{CMRR}_{II_\text{OP.AMP.}}}$$Where:
- $\text{CMRR}_{II_\text{R}}$ is the one we have just calculated, so ${1 + K \over 4 \varepsilon_{\small \kern-2px R}}$
- $\text{CMRR}_{II_\text{OP.AMP.}}$ was calculated [[SaM - CMRR • Calculation of the CMRR for the Second Stage of an Instrumentational Amplifier|here]], and we found it equal to: ${1 \over 2} {{\large{R_4 \kern2px (R_2+R_1) \over (R_3 + R_4) \kern2px R_1}} + {\large{R_2 \over R_1}} \over {\large{R_4 \kern2px (R_2+R_1) \over (R_3 + R_4) \kern2px R_1}} - {\large{R_2 \over R_1}}}$

Then we need to calculate:$$\text{CMRR}_{\text{TOT}} = \text{CMRR}_{II_\text{(R+OP.AMP.)}} \cdot \text{CMRR}_{I}$$Where:
- $\text{CMRR}_{I}$ was calculated [[SaM - CMRR • Calculation of the CMRR for the First Stage of an Instrumentational Amplifier|here]], and we found it equal to: $\frac{R_G}{2R_B+R_G}$

---
###### Memory Card
![[Samsung_SaM_Notes_13_240515_175715_3.jpg]]

---