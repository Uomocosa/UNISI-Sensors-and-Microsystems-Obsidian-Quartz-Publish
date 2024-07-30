###### Memory Card
![[Samsung_SaM_Notes_05_240515_183031_1.jpg]]

---

 If we consider the Input and Output resisistances non-ideal, we can model an [[SaM - Operational Amplifier|op.amp]] like this:<br>![[Pasted image 20240124174937.png]]
So that:$$V_{out}' = A_d V_d + A_c V_c$$Where:
- $V_d = V_2-V_1$ $\kern5px$  (so the voltage on $R_D$)
- $V_C = \frac{V_2+V_1}{2}$ $\kern17.5px$ (so the voltage on $R_{C1}$ plus the voltage on $R_{C2}$)
- $A_d = \frac{A_2-A_1}{2}$
- $A_C = A_2+A_1$
	- $A_1 = \left.V_{out}\right|_{V_2=0}$
	- $A_2 = \left.V_{out}\right|_{V_1=0}$
- $R_{C1}$ and $R_{C2}$ are the "***common mode resistances***". (Ideally they are both $\infty$ #NOT_SURE_ABOUT_THIS )
- $R_D$ is the "***differential mode resisitance***". (Ideally we consider it $\infty$)
- $R_0$ is the "***output resistance***, ideally it's $0$.
- ==Normally, an **ideal op.amp.** would have only $A_d = A = \infty$ for the output, however in reality, the ouput also depends on $A_c V_c$==.

---

We can imagine it a connected to a [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|resistive bridge]], and here is a somewhat [[SaM - Thevenim and Norton Equivalent|thevenim equivalent]]
 ![[Pasted image 20240124174817.png]]
- $R_{TH}' = {R_1 \parallel R_4}$.
- $R_{TH} = {R_2 \parallel R_3}$. (This can also be a sensor, if we use a [[SaM ~ Half Bridge Example • Two Strain Gauges|half]] or [[SaM - Full Bridge|full]] bridge)
- $V_{CC} = V {R_2 \over R_2 + R_3}$ "***offset voltage***".
- $V_{TH} = V \left(\frac{R_1}{R_1+R_4} - \frac{R_2}{R_2+R_3}\right)$ is the"***changing part***" given by our sensor.
- Using this model we don't lose the $V^+$ and $V^-$ nodes that connect the bridge to the amplifer.

> The ***actual*** thevenim equivalent would have been:
> - $V_{TH} = V \left(\frac{R_1}{R_1+R_4} - \frac{R_2}{R_2+R_3}\right)$
> - $R_{TH} = (R_1 \parallel R_4) + (R_2 \parallel R_3)$
> - ***Source***: [Youtube](https://www.youtube.com/watch?v=-82oP4y-uXo).

So finally if we unite the two circuits:<br>![[Pasted image 20240124182447.png]]
- $R_C \gg R_{TH}$
-    We have that the output will be (we consider a [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|balanced bridge]]):$$V_{out}' = A_dV_d + A_c \left(V_{CC} + {V_d \over 2}\right)$$ #NOT_SURE_ABOUT_THIS (How the fuck was this result found???), mentioned in: **Lecture 11_03**, **Lecture 12_02**, **Lecture 12_03**
- ***What are some common values for differencial input resistance, common input resistance, and output resistance, of an operational amplifier?*** (*ChatGPT*)
	- The input and output resistances of an operational amplifier (op-amp) can vary depending on the specific model and manufacturer.<br>However, I can provide you with some typical values that you might encounter in general:
	1. **Differential Input Resistance ($R_{in}$​)**:<br>Commonly in the range: $\left[10^{5} \ \ohm\div 10^{14} \ \ohm\right]$.
	2. **Common Input Resistance ($R_{c}$​)**:<br>Commonly in the range: $\left[10^{9} \ \ohm\div 10^{12} \ \ohm\right]$.
	3. **Output Resistance ($R_{0}$​)**:<br>Generally low: $\lt 100 \ \ohm$.
	- Remember, these are rough values, and actual specifications can vary.<br>Always refer to the datasheet of the specific operational amplifier you are working with for precise information.<br>If you have a particular op-amp in mind, I can provide more specific details using the mathjax format you specified.
