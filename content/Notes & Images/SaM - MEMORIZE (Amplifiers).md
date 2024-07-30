##### List of things to memorize:
![[SaM - Amplifiers]]

---
###### [[SaM - Operational Amplifier]]
![[Pasted image 20231007111611.png]]
- ***Open Loop Frequency Response Formula***:$$V_{out} = (V_2-V_1)\cdot \frac{A_{DC}}{1+j\frac{f}{f_H}}$$
- ***Non-Idealities of Operational Amplifier***:<br>![[Pasted image 20240102191905.png|333]]
	- $Z_{in}$ : **input resistance**, $Z_{in} \in [100 \ \text{k} \ohm \div 1\ \text{M}\ohm]$, usually we consider it $\simeq \infty$.
	- $Z_{out}$ : **output resistance**, $Z_{out} \in [100 \, \ohm \div\, 20 \ \text{k} \ohm]$, we usually consider it $\simeq 0$.
	- $V_{io}$ : **voltage input offset**, $V_{io} \in [\mu \text{V} \div \text{mV}]$.
	- $I_{\text{bias}}$ : **input bias current**, $I_{\text{bias}} \in [\text{fA} \div \mu\text{A}]$ (**Remember**: $\text{f} = 10^{-15}$, $\mu = 10^{-6}$).
- ***Terminology***:
	- $A_{DC}$ : open loop gain (ideally **infinite**, in reality $\in [10^5 \div 10^6]$).
	- $f_H$ : cut-off frequency $(f_H \in [1 \ \text{Hz} \div 1 \ \text{MHz}])$.

---
###### [[SaM - Non-Inverting Operational Amplifier]]
![[Pasted image 20240123184742.png|333]]
- ***Formula***:$$V_{out} = V_{in} {1 \over \beta}$$Where: $\beta = {\large{R_1  \over R_1 + R_2}}$
- ***Terminology***:
	- $\beta$ : feedback factor.

---
###### [[SaM - Inverting Operational Amplifier]]
![[Pasted image 20240123184928.png|333]]
- ***Formula***:$$V_{out} = V_{in} \cdot -{R_2 \over R_1}$$
---
###### [[SaM - Non-Ideal Operational Amplifier • Input and Output Resistances]]
![[Pasted image 20240124174937.png]]
- ***Formula***:$$V_{out}' = A_d V_d + A_c V_c$$Where:
	- $V_d$ : "*differential voltage*" $(V_d = V_2-V_1)$.<br>It's the voltage on $R_D$
	- $V_C$ : "*common mode voltage*" $\left(V_C = \frac{V_2+V_1}{2}\right)$<br>It's the voltage on $R_{C1}$ plus the voltage on $R_{C2}$
	- $A_d$ : "*differential gain" $\left(A_d = \frac{A_2-A_1}{2}\right)$
	- $A_C$ : "*common mode gain" $(A_C = A_2+A_1)$
	- $A_1 = \left.V_{out}\right|_{V_2=0}$
	- $A_2 = \left.V_{out}\right|_{V_1=0}$
- $R_{C1}$ and $R_{C2}$ are the "***common mode resistances***". (Ideally they are both $\infty$ #NOT_SURE_ABOUT_THIS )
- $R_D$ is the "***differential mode resisitance***". (Ideally we consider it $\infty$)
- $R_0$ is the "***output resistance***, ideally it's $0$.
- ==Normally, an **ideal op.amp.** would have only $A_d = A = \infty$ for the output, however in reality, the ouput also depends on $A_c V_c$==.

***Plus a resistive bridge***:<br>![[Pasted image 20240124174817.png]]
- Where:$$V_{TH} = V \left(\frac{R_1}{R_1+R_4} - \frac{R_2}{R_2+R_3}\right)$$
***Combining the two circuits***:<br>![[Pasted image 20240124182447.png]]
- $R_C \gg R_{TH}$
- The output:$$V_{out}' = A_dV_d + A_c \left(V_{CC} + {V_d \over 2}\right)$$
---
###### [[SaM - Non-Ideal Operational Amplifier • OZE (Out of Zero Error) • Special Kinds of Operational Amplifiers • Precision Amplifier  • Low Noise • Low Input Bias Current • Zero Drift • Low Noise Operational Amplifier]]
![[Pasted image 20240116185406.png|500]]

***Plus the Thevenim equivalent of a measurement system***:<br>![[Pasted image 20240116185532.png|500]]
- ***OZE (Out of Zero Error)***:$$\left.V_{out}\right|_{\large{V_s=0}} = \left(1 + {R_2 \over R_1} \right)\left(I_{b2} R_S - I_{b1}{R_1 R_2 \over R_1 + R_2} + V_{io} \right)$$
- ***IZE (Input out of Zero Error)***:$$\text{IZE} = I_{b2} R_S - I_{b1}{R_1 R_2 \over R_1 + R_2} + V_{io}$$

|  | $I_b$ | $V_{io}$ | **TCV** | Other |
| ---- | ---- | ---- | ---- | ---- |
| *Low input bias current op.amp.* | $<100\ \text{pA}$ |  |  |  |
| *Precision amplifiers* |  | $< 1 \ \text{mV}$ | $\lt 2 {\mu \text{V} \over ° \text{C}}$ |  |
| *Zero drift op. amp* |  | $\sim 1000$ times lower then *precision amplifiers* | $\sim 1000$ times lower then *precision amplifiers* | **Slow devices** (high [[SaM - Rise Time\|rise time]]) |
| *Low noise amplifier* |  |  |  | Minimize the white noise interferance. |

- ***Rule of thumb***:$$V_{\small{\text{DRIFT}}} = {1 \over 10} V_{io}$$
- ***Terminology***:
	- $V^+$ : $(+)$ terminal of the amplifier
	- $V^-$ : $(-)$ terminal of the amplifier
	- $V_{io}$ : input voltage offset
	- $I_{b1}$ & $I_{b1}$ : input bias current on each of the the two terminals.
	- $V_S$, $R_S$ : source voltage and source resistance (thevenim equivalent of the source).
	- **TCV**: Temperature Coefficient of Voltage ([[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|similar to TCR]])

---
###### [[SaM - Single Input Amplifier]]
- ***Representation***:<br>![[Pasted image 20240116233210.png|333]]
- ***Usually an [[SaM - Operational Amplifier|A.O.]] with one of the two inputs connected to ground***:<br>![[Pasted image 20240116233538.png|333]]


---
###### [[SaM - Differential Amplifier]]
![[Pasted image 20230626201332.png|500]]<br>![[Pasted image 20230626201359.png|500]]

A differential amplifier output functions depends only on the difference: $$V^+-V^-$$Here's an example:<br>![[Pasted image 20240131124912.png]]

---
###### [[SaM - Simple Differential Amplifier (Made from an O.A.)]]
![[circuit-20231004-1432.png|500]]

---
###### [[SaM - Instrumentational Amplifier]]
![[Pasted image 20231004153316.png|500]]
- Formula:$$V_{out} = (V_2 - V_1)\cdot\left(1+\frac{2R_1}{{R_{\text{gain}}}}\right)\frac{R_3}{R_2}$$
---
Don't know if it is a requested knowledge for the exam, here's some information on the [[SaM ~ Example of a Real Instrumentational Amplifier • INA128|instrumentational amplifier "INA128"]]

---
###### [[SaM - Thevenim and Norton Equivalent]]
![[Pasted image 20230707113000 1.png]]

***Passages***:
1. Disconnect A-B ("the **load**").
2. Find the voltage $V_{TH}$.
3. Reconect the load, disconnect all **indipendent sources**, and calculate the **Thevenim resistance** ($R_{TH}$) between A and B.

- ***Terminology***:
	- $Z_L$ : load impedance.
	- $Z_{TH}$ : thevenim impedance.

---
###### [[SaM - Voltage Amplifier]]
![[Pasted image 20240116232131.png|333]]
- ***Very ==high== input impedance, very low output impedance***
- ***Formula***:$$V_{out} = V_{i}\cdot {1 \over \beta}$$
---
###### [[SaM - Current Amplifier]]
![[Pasted image 20240116232614.png]]
- ***Very ==low== input impedance, very low output impedance***
- The output is:$$V_{out} = R \cdot I_f$$And $I_f$ is:$$I_f = {Z_N \over {R \over A(f)} + Z_N}I_N$$If $A_{f}$ is really big, as it usually is for **DC signals**, we find that:$$I_f = I_N$$
- ***Terminology***:
	- $I_f$ : feedback current.

---
###### [[SaM - AC-Coupled Amplifier]]
*Used to remove from the output signal the **DC** components*.
- ***Singol input amplifier***:<br>![[Pasted image 20240131180856.png|500]]
- ***Differential amplifier***:<br>![[Pasted image 20240131182019.png|500]]

---
###### [[SaM - Carrier Amplifier]]
![[Pasted image 20230719105500.png|500]]

---
###### [[SaM - AM Modulation with 2 Sensors • Carrier Amplifier]]
![[Pasted image 20230719105256 1.png|500]]
- ***Sensors***:$$C_1 = {{C_0 \over 1 + x}}, \kern20px  C_2 = {{C_0 \over 1 - x}}$$
- ***Output***:$$V_{out} = V_g \left({Z_f \over Z_1} - {Z_f \over Z_2}\right)$$Where:
	- $Z_f = R_f \parallel {1 \over j \omega C_f} = {R_f \over 1 + j \omega R_f C_f}$
	- $Z_1 = {1 \over j \omega C_1}$
	- $Z_2 = {1 \over j \omega C_2}$
- ***Output after calculations***:$$V_{out} = V{\kern-4px {\small{g}}} \kern2px {R_f \over 1 + j \omega R_f C_f} (j \omega2 C_0 \kern2px x) $$Where:
	- $x \in [0,\ 1]$, also $x \ll 1$
	- $C_1 = {\large{C_0 \over 1 + x}}$
	- $C_2 = {\large{C_0 \over 1 - x}}$
- ***Plot***:<br>![[Pasted image 20230719105325.png]]
	- ***Simplified output for $f_0\gg{1 \over 2 \pi R_f C_f}$ and $f_0 \gg f_{S_{MAX}}$***:$$V_0 \simeq V \cdot \frac{2C_0}{C_f}\cdot|x|$$
- ***Complete circuit with sign reovery***:<br>![[Pasted image 20230719105428.png|500]]
- ***Terminology***:
	- $V_g$ : sinusoidal (or alternating) source voltage.
	- $Z_f = R_f \parallel {1 \over j \omega C_f}$ : capacitive feedback impedance.
	- $x$ : measured quantity (in this case we can imagine to meaure the proximity, so in $m$).
	- #TODO Why $x \in [0,\ 1]$, also $x \ll 1$??, which capacitive sensor does this $C = {C_0 \over 1 + x}$?

---
###### [[SaM - Charge Amplifier]]
![[Pasted image 20240116225312.png|333]]
- ***Formula***:$$f_{\min} = {1 \over 2 \pi R_f C_f}$$
---
###### [[SaM - Logarithmic Amplifier]]
![[Pasted image 20231203170329.png]]
- ***Formula***: $$V_{out} = -V_T \ln\left(\frac{V_{in}}{I_{\kern-2pxS}\kern2px R}\right)$$Where:$$V_T = {KT \over q}$$
- [[SaM - Sensors Based on Silicon Junctions (BJT and Integrated Circuits)|BJT]] Formula:$$V_{BE} = V_T \cdot \ln\left({I_C \over I_S}\right)$$
- ***Terminology***:
	- $V_T$ : thermal voltage $\left(V_T = {KT \over q}\right)$
	- $K$ : Boltzman's constant $\left(K = 1.38 \cdot 10^{-23} \kern7px{\large{\text{m}^2 \cdot \text{kg} \over ° \text{K} \cdot \text{s}}}\right)$

---