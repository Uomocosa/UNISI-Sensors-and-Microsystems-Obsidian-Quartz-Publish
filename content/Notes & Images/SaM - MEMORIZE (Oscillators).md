##### List of things to memorize:
![[SaM - Oscillators]]

---
###### [[SaM - Introduction to Oscillators]]
- ***Feedback structure***:<br>![[Pasted image 20230719114724 1.png|333]]
- ***Transfer function***:$${V_0 \over V_S} = {A \over 1 + \beta A}$$
- [[SaM - Barkhausen Conditions|Barkhausen Conditions]]:$$\begin{array}{l} |\beta A | \ge 1 \\ \angle{\beta A} = 180° \end{array}$$
- _To have an unstable or marginally stable (oscillating) output, i will  a [[SaM - Modes Related to Conjugate Poles|couple of poles which are complex and conjugate]] with: $\operatorname{Re}{(p_1)} = \operatorname{Re}{(p_2)} \ge 0$_.
- ***Difference between unstable and marginally unstable***:<br>![[Pasted image 20230719114744 1.png|500]]

---
![[SaM - MEMORIZE (Capacitive Sensors)#SaM - Square Wave Oscillator]]
######
###### [[SaM - Barkhausen Conditions]]
- To create an oscillating output:
1. ***Transfer function***: ${V_0 \over V_S} = {A \over 1 + \beta A}$
2. I need a (preferably) marginally stable output, so: $1 + \beta(j\omega)A(j\omega) = 0$
3. Solution: "***Barkausen conditions***":$$\begin{array}{l} |\beta A | \ge 1 \\ \angle{\beta A} = 180° \end{array}$$(_If $|\beta A|$ is exactly $1$, we will have a **marginally stable** output_)
- ***Frequency stability***: _the two parameters ($\beta$ and $A$), which are the gain of the amplifier and the gain of the feedback network, **have to be stable in time, not changing**_.<br>⇒ _We can "take a big slope" when crossing the $-180°$ degrees line, so around $\omega_0$ (where I need to oscillate)_.
- ***"Big slope solution***:<br>![[Pasted image 20230719114850 1 1.png|333]]

---
![[SaM - MEMORIZE (Capacitive Sensors)#SaM - FM (Frequency Modulation) Based on Oscillators]]
######
![[SaM - MEMORIZE (Capacitive Sensors)#SaM - AM (Amplitude Modulation) Based on Oscillators]]
######
###### [[SaM - Oscillators based on Wien Bridge]]
- ***Circuit***:<br>![[Pasted image 20230719114922.png|500]]
- ***Formulas***:
	- $A \triangleq {\large{V_o \over V_i}} = 1 + {\large{R_2 \over R_1}}$
	- $\beta = -{\large{Z_1 \over Z_1+Z_2}}$
- _**Applying the [[SaM - Barkhausen Conditions|Barkhausen conditions]]**, after the calculations, we can satisfy them if we take_:
	1. $\omega_0 = RC$
	2. $R_2 \ge 2 \cdot R_1$
- ***Plot***:<br>*Oscillators based on Wien Bridge have a constant slope around $\omega_0$*:$$\left.{d\kern2px \varphi(\beta) \over d\omega}\right|_{\omega = \omega_0} = {2 \over 3}$$![[Pasted image 20230719114947.png|500]]
- ***Variation of the Wein Bridge***:<br>(_The **zener diodes** ensures to reduce the distortion due to an unstable behavior of the circuit_)<br>![[Pasted image 20230719115000 1.png|500]]

---
###### [[SaM - Phase Shift Oscillator]]
- ***Circuit***:<br>![[Pasted image 20230719115012.png|500]]

---
###### [[SaM - High Frequency Oscillator • 3 Point Oscillator • Colpits and Hartley Oscillators]]
- ***High frequency device***: $f \in \left[100 \ \text{kHz} \div 30 \ \text{MHz} \right]$
- ***Circuit***:<br>![[Pasted image 20230720170231 1.png|333]]
- ***Equivalent model***:<br>![[Pasted image 20230719115116 1.png|500]]
- ***Formulas***:<br>(_$Z_1$, $Z_2$, $Z_3$, are all pure immaginaries: $Z_i = jX_i$_).$$\begin{array}{l}  A = {\large{V_0 \over V_i}} = A_v \cdot {\large{Z_3 \parallel (Z_1 + Z_2) \over R_0 + Z_3 \parallel (Z_1 + Z_2)}} \\ \beta = {\large{V_f \over V_i}} = -{\large{X_1 \over X_1 +X_2}}  \end{array}$$
- ***[[SaM - Operational Amplifier|Typical open loop formula of an amplifier]]***:<br>![[Pasted image 20230719115142 1.png|333]]
- **For $f \ll f_h$ we have that***:$$A = A_v \frac{j X_3 (jX_1 + j X_2)}{jR_0 (X_3+X_1+X_2) +j X_3 (jX_1 + j X_2)}$$If we impose $X_1 + X_2 + X_3 = 0$, or more in general:$$X_i + X_j = -X_z$$We will find: $A = A_v$
	- ***Hartely oscillator***: $2$ **inductances** and $1$ **capacitance**.
	- ***Colpits oscillator***: $2$ **capacitances** and $1$ **inductances**.
- ***Barkausen Conditions***: <br>(*Also considering $X_1+X_2 = -X_3$*)<br>$$\beta = {\frac{X_1(\omega_0)}{X_3(\omega_0)}} \kern15px\Rightarrow\kern15px |\beta A |_{\omega = \omega_0} = A_v \kern2px {\frac{X_1}{X_3}}$$So:
	- If $A_v \gt 0$ ([[SaM - Non-Inverting Operational Amplifier|non-inverting amplifier configuration]]) ⇒ $X_1$ and $X_3$ must have **OPPOSITE types**:
		- if $X_1$ is a **capacitance**, $X_3$ must be an **inductance**.
		- if $X_1$ is an **inductance**, $X_3$ must be a **capacitance**.
	- If $A_v \lt 0$ ([[SaM - Inverting Operational Amplifier|inverting operational amplifier configuration]]) ⇒ $X_1$ and $X_3$ must have **the SAME types**, meaning:
		- if $X_1$ is a **capacitance**, $X_3$ must be a **capacitance**.
		- if $X_1$ is an **inductance**, $X_3$ must be an **inductance**.
- ***Terminology***:
	- $A_v$ is the open loop of the amplifier, $A_v \in \mathbb{R}$.
	- $Z_1 = jX_1$.
	- $Z_2 = jX_2$.
	- $Z_3 = jX_3$.

---
###### [[SaM - Quartz in a 3 Point Oscillator]]
- ***Using an [[SaM - AT-Cut Quartz|AT-cut quartz]] in a [[SaM - High Frequency Oscillator • 3 Point Oscillator • Colpits and Hartley Oscillators|Colpits oscillator]]***:<br>(_This circuit will oscillate only at frequency in which the quartz acts as an inductance, so for $f_0$ in the interval $[\omega_s ,\ \omega_p]$_)<br>![[Pasted image 20230720170240 1.png|333]]
- ***$Q$-factor value***:<br>(_Adding a capacitance in series or in parallel to our quartz, will reduce this value, **not goood**_)$$Q = {1 \over \omega_s R_{eq}\kern2pxC_{eq}}$$
- ***Adding a capacitance in series or in parallel to the quartz***:<br>(_Adding a capacitance in series or in parallel can reduce the frequencies $f_s$ and $f_p$, giving us more control, **good**_)
	- ***No added capacitance, base graph***:<br>![[Pasted image 20230720170240 2.png|500]]
	- ***Added capacitance***:<br>![[Pasted image 20230720170240 3.png|500]]
		- **In series**: we increase $f_s$.
		- **In paralle**: we reduce $f_p$.
		- In both cases we reduce the range $[f_s,\ f_p]$

---
###### [[SaM - Behavior of the Quartz Ocillator at High Frequencies]]
- [[SaM - AT-Cut Quartz|AT-cut quartz's impedance]]:$$Z_{eq} = C_E \parallel (L_{eq} + R_{eq} + C_{eq})$$
- ***Special frequencies***:<br>(_They depend on the [[SaM - Types of Cut Quartzes|type of cut]] of the quartz_)$$\begin{array}{l} \omega_s = {\huge\sqrt{{1 \over L_{eq} \kern1px C_{eq}}}}  \\[3px] \omega_p = {\huge\sqrt{{C_{\kern-2pxE} + C_{eq} \over C_{\kern-2pxE} \kern1px L_{eq} \kern1px C_{eq}}}}    \end{array}$$
- ***Reactance formula $\left(X_{eq} : Z_{eq} = jX_{eq}\right)$***:$$X_{eq} = - {1\over\omega C_{\kern-2pxE}}{1-{\large{\omega^2 \over \omega_s^2}}\over1-{\large{\omega^2 \over \omega_p^2}}}$$
- ***Plot of ${1-{\large{\omega^2 \over \omega_s^2}}\over1-{\large{\omega^2 \over \omega_p^2}}}$***:<br>![[Pasted image 20230720170319 1.png|500]]
- ***More realistic impedance model***:<br>(_If we work at a high frequency $(f \in [20 \ \text{MHz} \div 30 \ \text{MHz}])$, we need to consider this additional impedaces, after the first_).<br>(_If we work at lower frequencies $(\lt 10 \ \text{MHz})$ we can consider just the first $Z_{eq}$_).<br>![[Pasted image 20230720170338.png|500]]
- ***Formula for each component***:$$\begin{array}{l}   L_{m_i} = {1 \over 8}{m \over k^2 d^2}  \\[5px]  C_{m_i} = {8 \over (i \cdot \pi)^2}k d^2  \\[4px]  R_{m_i} = {(i \cdot \pi)^2 \over 8}{\lambda \over k^2 d^2} \end{array}$$And the value of $\omega_{s_i}$:$$\omega_{s_i} \approx i \cdot w_{s_1}$$
- ***Real World Measures***:
	- At $\omega = 10 \ \text{MHz}$, we gave some common values for the [[SaM - AT-Cut Quartz|AT-cut quartz's impedances]]:$$\begin{array}{l}   L_{eq} = 100 \ \text{mH}  \\[2px]  C_{eq} = 15 \ \text{fF}  \\[4px]  R_{eq} = 20 \ohm \end{array}$$
-  ***Terminology***:
	- $m,\ \lambda,\ k$ : mass, dumping coefficient, elastic coefficient of the [[SaM - Piezoelectric Effect|piezoelectric]] slice.
	- $d$ is the [[SaM - Piezoelectric Effect in Details • Direct and Inverse Piezoelectric Effect|piezoelectric coefficient]].

---
![[SaM - MEMORIZE (Piezoelectricity)#SaM - Quartz Oscillator]]
###### 
