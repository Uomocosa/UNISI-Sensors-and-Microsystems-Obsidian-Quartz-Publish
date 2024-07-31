**CMRR**: "*Common Mode Rejection Ratio*".
$$\text{CMRR} \triangleq {|A_d| \over |A_c|}$$
$$A_d = {A_2 - A_1 \over 2}$$
$$A_c = A_2 + A_1$$
$$A_1 = \left.\frac{V_0}{V_1}\right|_{V_2 = 0}$$
$$A_2 = \left.\frac{V_0}{V_2}\right|_{V_1 = 0}$$
---
[[SaM - Instrumentational Amplifier|Instrumentational amplifier]]:<br>![[Pasted image 20230626201530.png|500]]

---
[[SaM ~ CMRR of a Simple Differential Amplifier|CMRR (Stage II)]]:<br>![[Pasted image 20230718184020 1.png|333]]
$$A_1 = -{R_2 \over R_1}$$
$$A_2 = {R_4\over R_3 + R_4}\cdot \left(1+{R_2 \over R_1}\right)$$
$$\text{CMRR}_{II} = \frac{|A_d|}{|A_C|} = \frac{|A_2-A_1|}{2 \cdot |A_2+A_1|}  = \cdots$$
---
[[SaM - CMRR • Calculation of the CMRR for the First Stage of an Instrumentational Amplifier|CMRR (Stage I)]]:<br>![[Pasted image 20231106192634.png|500]]
$$(V_2' - V_1') = \frac{(2R_B + R_G)}{R_G}(V_2 - V_1)$$
$$V_2'+V_1' = V_2+V_1$$
> **NOTE**: #IMPORTANTE 
> $R_B \simeq 50k\ohm$

$$\begin{matrix} 
& \text{CMRR}_{TOT} = \\[5px]
& = \frac{1}{\frac{(2R_B + R_G)}{R_G}}\cdot \text{CMRR}_{II} \\[5px]
& = \frac{R_G}{2R_B+R_G}\cdot \text{CMRR}_{II}\end{matrix}$$

---
[[SaM - CMRR • Design Rules for Resistance Values of an Instrumentational Amplifier|Design rules]]: non ideal [[SaM - Operational Amplifier|amplfier]], specifically $A \neq \infty$.
$$\begin{array}{l}  A_{1_{II}} = {\huge{-\frac{R_2}{R_1}\frac{\beta A}{1 + \beta A}}} \\[3px]  A_{2_{II}} = {\huge{\frac{R_4}{R_3+R_4}\frac{A}{1 + \beta A}}}  \end{array}$$Where:$$\beta = {R_1 \over R_1 + R_2}$$
Design rules:
1. $A_1 = -A_2$ $\kern10px$ (So that we obtain an **infinite [[SaM - CMRR (Common Mode Rejection Ratio)|CMRR]]**)
2. $\large \frac{R_4}{R_3} = \frac{R_2}{R_1}  = \normalsize K$ $\kern10px$ (like for a [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|balanced bridge]])

$$\frac{R_2}{R_1} = \frac{R_4}{R_3+R_4}\frac{R_2 + R_1}{R_1}$$
$$K = \frac{K}{1+K}(K+1)$$

---
[[SaM - CMRR • Calculation of the CMRR (Stage II) based on Resistance Tollerances|CMRR (Resistance Tollerances)]]
$$\begin{array}{l} {\large {R_2 \over R_1}} = K \\[3px] {\large {R_4 \over R_3}} = K' \end{array}$$
$$K' - K \triangleq 2\Delta K_{\max}$$
$$\large \varepsilon_{\small \kern-2px R} \normalsize \triangleq \frac{\Delta R_{\max}}{R} = \frac{\Delta K_{\max}}{K}$$
$$\text{CMRR}_R = {2 K (1 + K) \over K'-K}$$
$$\text{CMRR}_{R} = \frac{1+K}{4 \kern2px \large \varepsilon_{\small \kern-2px R}}$$
$$\text{CMRR}_{R}(K=1) = \frac{1}{2 \kern2px \large \varepsilon_{\small R}}$$
> **NOTE**: #IMPORTANTE 
> Usually we find: $\large \varepsilon_{\small R} \normalsize  = \frac{10^{-4}}{2}$
> So the $\text{CMRR} \simeq 10^{4}$

$${1 \over \text{CMRR}_{II_\text{(R+OP.AMP.)}}} = {1 \over \text{CMRR}_{II_\text{R}}} + {1 \over \text{CMRR}_{II_\text{OP.AMP.}}}$$
$$\text{CMRR}_{\text{TOT}} = \text{CMRR}_{II_\text{(R+OP.AMP.)}} \cdot \text{CMRR}_{I}$$Where:
$$\text{CMRR}_{I} = \frac{R_G}{2R_B+R_G}$$

---
[[SaM - CMRR due to the Circuit Topology|CMRR (Topology)]]:<br>![[Pasted image 20240124171936.png|500]]
- $R_{C1} ,\ R_{C2} \neq 0$, for semplicity let's say $R_{C1} = R_{C2} = R_C$
- $R_D = \infty$
- $\Delta R$ is the resisitve variation, due to the sensor.
- $R_{C1} = R_{C2} = R_C$.
- $R_C \gg R_{TH}$.
- For this circuit given these resistance values, we have: $V_{CC} \approx V_{c}$. #NOT_SURE_ABOUT_THIS 
- $A_{d_{\text{topology}}} = A$.

$$A_{c_{\text{topology}}} = \left.{V_{D}\over V_{c}}\right|_{V_{TH}=0}$$
$$A_{c_{\text{topology}}} = A_d\frac{\Delta R}{R_C}$$
$$\text{CMRR}_{\text{topology}} = \frac{A_d}{A_{c_{\text{topology}}}}$$
$$\frac{1}{\text{CMRR}} = \frac{1}{\text{CMRR}_{\text{topology}}} + \frac{1}{\text{CMRR}_{\text{R}}}$$
