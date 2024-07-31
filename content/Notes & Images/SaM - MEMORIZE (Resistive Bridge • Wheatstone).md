##### List of things to memorize:
![[SaM - Resistive Bridge • Wheatstone]]

---
###### [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge]]
- ***Circuit***:<br>![[Pasted image 20230611185749 1.png|333]]
- ***Sensor $(R_1)$ formula***:$$R_1 = R_{10}\kern2px(1+x)$$
- ***Output formula***:$$V_0 = V \left(\frac{R_1}{R_1+R_4} - \frac{R_2}{R_2+R_3}\right)$$
- ***K-ratio***:$$K = {R_4 \over R_{10}} = {R_3 \over R_2} $$
- ***Output formula with K-ratio***:$$V_0 = V \left(\frac{1+x}{1+x+K} - \frac{1}{1+K}\right)$$
- ***Balanced bridge $(K=1)$ formula***:$$V_0 = V \left(\frac{1+x}{2+x} - \frac{1}{2}\right)$$
- ***Maximum Realative Sensisitivity $(\text{for} \ K = 1)$***: $$S|_{x=0 \kern2px _{MAX}} = \frac{1}{4}$$
- ***Real World Measures***:
	- $x = \alpha T$, if we consider a [[SaM - Calendar Van Dusen Equation|RTD sensor]], specifically for [[SaM ~ Real World Example • Standard RTD Sensor • PT100 Sensor|the PT100 sensor]]:
		-  $x \in \left[-0.78 \div 3.3\right]$
		-  $R_0 = 100 \ \ohm$
	- $x = G \varepsilon_l$, if instead we consider a [[SaM - Metal Strain Gauge • Passive Strain Sensor|metal strain gauge]]
		-  $x \in \left[0 \div 0.1\right]$
		-  $R_0 \in \left[50\ \ohm \div 700\ \ohm\right]$
- ***Terminology***:
	- 

---
###### [[SaM - Half Bridge • Calculation for the Maximum Sensitivity of a Resistive Bridge]]
- ***Circuit***:<br>![[Pasted image 20230611200647.png|222]]
- ***Sensors***:$$\begin{array}{l}  R_1 = R_{10} \kern2px (1+x_1)  \\  R_2 = R_{20} \kern2px (1-x_2)  \end{array}$$
- ***K-ratio***:$$K = {R_4 \over R_{10}} = {R_3 \over R_{20}} $$
- ***Output formula***:$$V_0 = V \left(\frac{1+x_1}{1+x_1+K} - \frac{1-x_2}{1-x_2+K}\right)$$
- ***For: $(1+K) \gg x_1$, $(1+K) \gg x_2$ and $x_1 = -x_2$***:$$V_0 = V \cdot \frac{2 x}{1+K}$$
- ***Maximum Realative Sensisitivity $(\text{for} \ K = 1)$***: $$S|_{x=0 \kern2px _{MAX}} = \frac{1}{2}$$
- ***Calculate the maximum relative sensitivity***:
	1. Calculate:$$S(x) = \frac{1}{V}\frac{dV_{TH}}{dx}$$
	2. Calculate $S(x=0)$, than calculate:$$\frac{dS(x=0)}{dK}$$
	3. Find $K$ such that:$$\frac{dS(x=0)}{dK}=0$$
	4. Find $K$ such that $S(x=0)$ is maximied: and you'll find $K =1$.
	5. Calculate $S_{MAX}$:$$S|_{x=0 \kern2px _{MAX}} = \frac{1}{2}$$That's why it is called "**half**" brige.

---
###### [[SaM - Full Bridge]]
- ***Circuit***:<br>![[Pasted image 20230625114341.png|222]]
- ***Sensors***:$$\begin{array}{l} R_1 = R_3 =  R_0 (1 + x) \\ R_2 = R_4 =  R_0 (1 - x) \end{array}$$
- ***Output formula $(\text{for} \ K = 1)$***:$${V_{TH}\over V} = x $$
- ***Maximum Realative Sensisitivity $(\text{for} \ K = 1)$***:$$S|_{x=0 \kern2px _{MAX}} = 1$$

---
###### [[SaM - Design of a Resistive Bridge]]
- _We take in example an [[SaM - Half Bridge • Calculation for the Maximum Sensitivity of a Resistive Bridge|half bridge]]_.
1. ***Set the output range*** $V_{TH_{MAX}}$, from this find $x_{\max}$.
2. ***Check the power ([[SaM - Self-Heating|self heating]])***:$$P = \left(V \over R_1 + R_4\right)^2 \cdot R_1$$
3. ***Check [[SaM - Accuracy or Maximum Error|accuracy or maximum error]]***:$$\Delta V_{TH} \approx {dV_{TH} \over dx}\Delta x \gt \text{Noise level, IZE (Amplifier), drifts}$$
4. ***Linearity of the bridge***: so if $1 + K \gg x$.<br>The [[SaM - Non-Linearity Error|non-linearity error]]:$$\text{NL} = \frac{x}{1+K}$$So assert that:$$\text{NL}_{\text{accettable}} \gt \frac{x_{\max}}{1+K}$$

---
###### [[SaM ~ Resistive Bridge Example • Strain Gauge]]
- _Example of the [[SaM - Design of a Resistive Bridge|design process]] of a "${1 \over 4}$ [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|balanced resistive bridge]]" using a single [[SaM - Metal Strain Gauge • Passive Strain Sensor|strain gauge]] sensor_.
- (1.) Find $x_{\max}$:<br>$x_{\max} = G \cdot \varepsilon_{\max} = 4 \cdot 50 \kern2px 000 \ \mu \varepsilon$<br>⇒ $x_{\max} = 0.2$
- (3.) Check [[SaM - Accuracy or Maximum Error|accuracy or maximum error]]:<br>$\Delta \varepsilon = 10 \ \mu\varepsilon$ ⇒ $\Delta x = 4 \cdot 10^{-5}$<br>Then:$$\left.\Delta V_{TH}\right|_{x=0} = {V \over 4}\Delta x$$And for $V = 10 \ \text{V}$ we obatain: $\Delta V_{TH} = 100 \ \mu\text{V}$

---
###### [[SaM ~ Half Bridge Example • Two Strain Gauges]]
- ***Structure***:<br>![[Pasted image 20230611201143.png]]
- ***Sensors formula (with temperature offset)***:<br>![[Pasted image 20230611201132.png]]
- ***Output formula***:$${V_{TH} \over V} \approx {2 \kern2px G \kern1px \varepsilon_l \over 1 +K}$$

---
###### [[SaM - Wire Resistance in a Resistive Bridge (2 and 3 Wires Layout)]]
- ***Circuit***:<br>![[Pasted image 20230625114046 1.png|333]]
- ***Output formula***:$$V_{TH} = V {R_0 (1 + G\varepsilon) + 2R_{{\small W}}\over 2 R_0 + R_0G\varepsilon + 2R_{{\small W}}} - {V\over 2}$$
- ***Offset and sensitivity***: #NOT_SURE_ABOUT_THIS (redo the sensitivity calculations)$$ \begin{array}{l} \text{Offset}:&\left.V_{TH}\right|_{\varepsilon = 0} = V {\large{R_0 + 2R_{{\small W}}\over 2 R_0 + 2R_{{\small W}}}}  \\[3px] \text{Sensitivity}:&\left.{dV_{TH}\over d\varepsilon}\right|_{\varepsilon = 0} = V {\large{R_0 \kern2px G\over 2 R_0 + 2R_{{\small W}}}}\end{array}$$The offset **in theory could be corrected**.<br>The sensitivity is different from the nominal one (it depends on $R_W$).
- ***Using a current suplly - circuit***:<br>![[Pasted image 20230625114138.png|500]]
- ***Formulas***:$$ \begin{array}{l} V_{TH}= I_{DC} R_0 (1 + G\varepsilon) + I_{DC} \kern2px 2 R_{{\tiny W}} - I_{DC} R_{0} \\[7px] \text{Offset}: \kern40px \left.V_{TH}\right|_{\varepsilon = 0} = I_{DC} \kern2px {2R_{{\small W}}} - I_{DC} R_0  \\[3px] \text{Sensitivity}: \kern5px \left.{dV_{TH}\over d\varepsilon}\right|_{\varepsilon = 0} = I_{DC} \kern1pxR_0 \kern1px G \end{array}$$<br>The sensitivity is constant, this is a linear sensor (good).<br>The offset still depends on $R_W$ (bad).<br>==This is a good solution for **AC measurements**==.
- ***3 wires layout - circuit***:<br>![[Pasted image 20230625114149 1.png|333]]
- ***Formulas***: #NOT_SURE_ABOUT_THIS (redo the sensitivity calculations)$$ \begin{array}{l} V_{TH} = V {\large {R_0 (1 + G\varepsilon) + R_{{\small W}} \over 2 R_0 + R_0 G\varepsilon + 2 R_{{\small W}}}} - {\large{V \over 2}} \\[5px] \text{Offset}: \kern40px \left.V_{TH}\right|_{\varepsilon = 0} = 0 \\[3px] \text{Sensitivity}: \kern5px \left.{dV_{TH}\over d\varepsilon}\right|_{\varepsilon = 0} = V{\large{G R_0 (R_{{\small W}} + R_0) \over \left(2R_{{\small W}} + 2 R_0\right)^2}} \end{array}$$We have removed the offset (good).<br>But the sensitivity still depends on $R_{{\small W}}$ (bad).

---
###### [[SaM ~ Complete Sensor • Load Cell with a Resistive Bridge]]
- ***[[SaM - Load Cells or Pillar|Load cell]] with a [[SaM - Full Bridge|full bridge]] of [[SaM - Metal Strain Gauge • Passive Strain Sensor|strain sensors]]***:<br>![[Pasted image 20240112173342.png|222]]<br>![[Pasted image 20240112173532.png|222]]
- ***Sensors***:$$\begin{array}{l} R_1 = R_0 \kern2px (1 + G\varepsilon_l ) \\ R_2 = R_0 \kern2px (1 + G\varepsilon_t ) \\ R_3 = R_0 \kern2px (1 - G\varepsilon_l ) \\ R_4 = R_0 \kern2px (1 - G\varepsilon_t ) \\ \end{array}$$
- ***Output formula using strain***:$$V_{out} = V \kern2px {G \kern2px (1+\nu) \kern2px  \over 2} \kern2px \varepsilon_l$$
- ***Output formula using force***:$$V_{out} = V \kern2px {G \kern2px (1+\nu) \kern2px  \over 2} \kern2px {E \over A} \kern2px F_1 $$
- ***Real World Measures***:
	- Usually $\nu \simeq 0.35$, [[SaM - Load Cells or Pillar|specifically for platinum]] $\nu_{{Pt}} \simeq 0.38$.

---
###### [[SaM ~ Complete Sensor • Accelerometer with a Resistive Bridge]]
- ***Strucutre***:<br>![[Pasted image 20230625114240.png|500]]
- ***Sensor formulas***:$$\begin{array}{l}R_{1,\,3} = R_0\left(1-G\left({m_s\over K \cdot l}a\right)\right) \\ R_{2,\,4} = R_0\left(1+G\left({m_s\over K \cdot l}a\right)\right) \end{array}$$Where:$${m_s\over K \cdot l}a = \varepsilon_l$$
- ***Considering the pre-deformation of the straing gauges***:$$\begin{array}{l}R_{1,\,3} = R_0\left(1 - G\left({m_s\over K \cdot l}a\right) + G\varepsilon_0 \right) \\ R_{2,\,4} = R_0\left(1 + G\left({m_s\over K \cdot l}a\right) + G\varepsilon_0 \right) \end{array}$$

---
