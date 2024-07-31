##### ***Remeber***:

> The **3 point oscillator** is a device that can operate at **high frequency**, in numbers: $$f \in \left[100 \ \text{kHz} \div 30 \ \text{MHz} \right]$$Here's its circuit:<br>![[Pasted image 20230720170231 1.png|333]]

> For this devices we need a special amplifier, **NOT** an operational amplifier, since we are working at **high frequency**.
> Often we use a **single stage amplifier**, so like a [[SaM - Sensors Based on Silicon Junctions (BJT and Integrated Circuits)|BJT]], a **MOS**, ...

> We need define the coefficients for [[SaM - Introduction to Oscillators|the feedback loop of an amplifeir]], so here's a more usuefull schematic for the **3 point oscillator**:<br>![[Pasted image 20230719115116 1.png|500]]
> Looking at this we define:$$\begin{array}{l}  A = {\large{V_0 \over V_i}} = A_v \cdot {\large{Z_3 \parallel (Z_1 + Z_2) \over R_0 + Z_3 \parallel (Z_1 + Z_2)}} \\ \beta = {\large{V_f \over V_i}} = -{\large{X_1 \over X_1 +X_2}}  \end{array}$$Where:
> - $A_v$ is the open loop of the amplifier, $A_v \in \mathbb{R}$.
> - $Z_1 = jX_1$.
> - $Z_2 = jX_2$.
> - $Z_3 = jX_3$.

> Then we apply the [[SaM - Barkhausen Conditions|Barkhausen conditions]], so:$$\begin{array}{l} |\beta A | \ge 1 \\ \angle{\beta A} = 180° \end{array}$$But if $Z_1$, $Z_2$,  $Z_3$,  are imaginary (so if we use only capacitances and inductances, as we have supposed in the construction of the oscillator) then $\beta$ is a real negative number.

> I need that the cut-off frequency $f_H$ of the amplifier, has to be much larger than the working frequency of the oscillator $f_0$.<br>So this means that I suppose to operate with in this region here, where $A(f)$ can be considered a real number (with no imaginary part), so where $A(f) = A_v$ :<br>![[Pasted image 20230719115142 1.png|333]]
> I talk about $A(f)$ and $A_v$ interchangably, since in this case they are equal, but the formula that binds the two is:$$A(f) = A_v {1 \over 1 + j{\large{f \over f_h}} }$$ #NOT_SURE_ABOUT_THIS (Like an [[SaM - Operational Amplifier|operational amplifier]])

> So for $f \ll f_h$ we have that:$$A = A_v \frac{j X_3 (jX_1 + j X_2)}{jR_0 (X_3+X_1+X_2) +j X_3 (jX_1 + j X_2)}$$If we impose $X_1 + X_2 + X_3 = 0$ we will find:$$A = A_v$$As per hypotesys.

> So $X_1 + X_2 + X_3 = 0$ for $X_1 + X_2 = -X_3$, (this is one of many solution).
> Or more in general if $X_i + X_j = -X_z$.
> We can define:
> - $Z_i$ and $Z_j$ **capacitances** and $Z_z$ an **inductance**, (so $2$ capacitances and $1$ inductance), and we will have a **Colpits oscillator**
> - $2$ **inductances** and $1$ **capacitance**, and we will have a **Hartley oscillator**.

> And if we evaluate the first [[SaM - Barkhausen Conditions|Barkhausen condition]] $\left(|\beta A |_{\omega = \omega_0} \ge 1\right)$, we find:$$ \beta = \frac{X_1(\omega_0)}{X_3(\omega_0)} $$And$$|\beta A |_{\omega = \omega_0} = A_v \kern2px \frac{X_1}{X_3} $$This is $\ge 1$ (better if $|\beta A |_{\omega = \omega_0} = 1$), given: 
> #IMPORTANTE 
> - $A_v \gt 0$  ⇒ [[SaM - Non-Inverting Operational Amplifier|non-inverting amplifier]], $X_1$ and $X_3$ must have **opposite types**, meaning:
> 	- if $X_1$ is a **capacitance**, $X_3$ must be an **inductance**.
> 	- if $X_1$ is an **inductance**, $X_3$ must be a **capacitance**.
> - $A_v \lt 0$  ⇒ [[SaM - Inverting Operational Amplifier|inverting operational amplifier]], $X_1$ and $X_3$ must have **the same types**, meaning:
> 	- if $X_1$ is a **capacitance**, $X_3$ must be a **capacitance**.
> 	- if $X_1$ is an **inductance**, $X_3$ must be an **inductance**.
---
###### Memory Card
![[Samsung_SaM_Notes_24_240516_113108_2.jpg]]

---
The name of this device is "***3 Point Oscillator***".
![[Pasted image 20230719115116.png]]
- So we take an amplifier and **this is not an operational amplifier because we are operating at high frequency**.<br>So $A$ is an **amplifier**, often it is a single stage amplifier, so like **BJT**, a **MOS**, ...
- In this circuit $\beta$ is not well defined, so we can use a more mathematical approch, using the defintion of $\beta$: $$\beta = \frac{V_f}{V_i}$$

![[Pasted image 20230719115131.png]]
- If all three $Z_i$ are imaginary (so if we use only capacitances and inductances) then $\beta$ is a real negative number.
- $A_v$ is the open gain loop of the amplifier.

![[Pasted image 20230719115142.png]]
- Again: $A_v$ is the open gain loop of the amplifier, and I consider it to be a real number.<br>⇒ So i need It means that this frequency $f_H$ of the amplifier, has to be much larger than the working frequency of the oscillator $f_0$.<br>So this means that I suppose to operate with in this region here, where $A_v$ can be considered a real number.
- Also if we work at low frequency the phase of $A_v$ is equal $0$.
- Let's look at the rest of $A$, such that I will rewrite is as, so:$$A = A_v \frac{Z_A}{R_0+Z_A}$$Where:$$Z_A = \frac{j X_3 (jX_1 + j X_2)}{j (X_3+jX_1+jX_2)}$$
- If make a simple "commun divisore":$$A = A_v \frac{j X_3 (jX_1 + j X_2)}{jR_0 (X_3+X_1+X_2) +j X_3 (jX_1 + j X_2)}$$
- So if we impose $jR_0 (X_3+X_1+X_2) = 0$, so $(X_1+ X_2+ X_3) = 0$ we have that $A$ is a real and positive number (same as $\beta$ as long as we only use capacitance and inductors)

So, to have $\angle \beta A = -180°$, we need:
![[Pasted image 20230719115153.png]]
- Since a capacitance in the frequency domain is $\frac{1}{j\omega C} = -j \frac{1}{\omega C}$ 
- And an inductance: $j\omega L$
- Remember also that $X_1$ and $X_2$ are the same type (capacitance or inductance) while $X_3$ needs to be the other type (inductance or capacitance)


Now I need to evaluate the second rule:
![[Pasted image 20230719115158.png]]
- So remember:$$\beta = \frac{X_1(\omega_0)}{X_3(\omega_0)}$$And $$A = A_v$$Actually this should be $A_v(\omega_0)$ but I have supposed to work way under the cut-off frequency $f_H$ of the amplifier, so $A_v(\omega_0) \simeq A_v$

In case $A_v$ is a negative gain:![[Pasted image 20230719115207.png]]

