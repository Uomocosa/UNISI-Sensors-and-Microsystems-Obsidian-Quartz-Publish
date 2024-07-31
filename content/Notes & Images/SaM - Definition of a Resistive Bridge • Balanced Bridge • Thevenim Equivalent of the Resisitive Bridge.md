##### ***Remeber***:

> A **resisitve bridge** or "*wheatstone*" or "$1 \over 4$ bridge" has a structure like this:
> ![[Pasted image 20230611185749 1.png]]
> - $R_{1}$ is our sensor, and we will describe it with the formula:$$R_1 = R_{10}\kern2px(1+x)$$Where, based on the sensors we have seen so far $x$ can be seen as:
> 	- $x = \alpha T$, if we consider a [[SaM - Calendar Van Dusen Equation|RTD sensor]].
> 	- $x = G \varepsilon_l$, if instead we consider a [[SaM - Metal Strain Gauge • Passive Strain Sensor|metal strain gauge]].
> - The output of a "$1 \over 4$ bridge" is like so:$$V_0 = V \left(\frac{R_1}{R_1+R_4} - \frac{R_2}{R_2+R_3}\right)$$So a resistive bridge will have a **DC offset** equal to: $V\left({R_2 \over R_2 + R_3}\right)$.<br>And a changing part (given by our sensor) equal to: $V\left({R_1 \over R_1 + R_4}\right)$

> We can then define a particular resisitve bridge called a **balanced bridge**, that has the property that ==for $x=0$ the outptut will be $V=0$==.
> To achive this we just need to define the **$K$-ratio**:$$K = {R_4 \over R_{10}} = {R_3 \over R_2} $$Then the output will be:$$V_0 = V \left(\frac{1+x}{1+x+K} - \frac{1}{1+K}\right)$$

> #IMPORTANTE 
> The output $V$ is **not grounded**, this means the for the read out electronics for a resistive bridge we will need a [[SaM - Differential Amplifier|differential amplifier]].
> (*In general we will need a read-out with at least two inputs*). #NOT_SURE_ABOUT_THIS 
> We **CANNOT** use a [[SaM - Single Input Amplifier|one-input amplifeir]].

> We have also seen two variations of resistive bridges: [[SaM - Half Bridge • Calculation for the Maximum Sensitivity of a Resistive Bridge|half brige]] and [[SaM - Full Bridge|full bridge]].

> ***What is the use of a balanced resistive bridge?***
> - If we were to measure the resistance of a [[SaM - Metal Strain Gauge • Passive Strain Sensor|strain gauge]] the formula, as we have said would be: $R = R_0 \kern2px (1 + x)$.<br>In a real world scenario:
> 	- The voltage $R_0$ assumes values in the order of $[50\ \ohm \div 700\ \ohm]$
> 	- And the variation of $x$ is around $[0 \div 0.1]$, so the variation due the strain is **really low**.
> - While for [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|RTD sensors]], specifically we have seen [[SaM ~ Real World Example • Standard RTD Sensor • PT100 Sensor|the PT100 sensor]]:
> 	- $R_0=100 \ \ohm$.
> 	- $x \in [-0.78 \div 3.3]$, based on the range of temperature $[-200 °\text{C} \div 850 °\text{C}]$.
> - For startets, at rest the output will be:
> 	- For the normal passive sensor $R = R_0$.
> 	- For the **resistive brige**: $V_{out} = 0 \text{V}$.<br>⇒ The bridge corrects the **DC offset** of the passive sensor.
> - So the range of values $x$ can assume are quite limited, especially for **strain gauges**, to increase this range, we can use a resistive bridge with a "high" source voltage $V$, so that if we consider the [[SaM - Sensitivity|sensitivity]], of the output value around $x=0$, with $K = 1$, and $V=10 \text{V}$ we will have: #NOT_SURE_ABOUT_THIS 
> 	- For the normal passive sensor $\alpha = 1$.
> 	- For the **resistive brige**: $\alpha = {1 \over 4} \cdot V$, so $\alpha = 2.5$.
> - ==If we use a **balanced resisitve brige**, we will also **compensate for temperature**, since changes in temperature will affect all the resistors in the bridge equally, maintaining the balance==.
> - However note that the **resisitve brige**, results in a **non-linear** sensor, if we plot how ${V_{out}\over V}$ changes given $R_1 = R_{10}\kern2px (1+x)$, we will obtain somenthing like this:<br>![[Pasted image 20240111181615.png]]
> 
> ***Sources***:
> - [Youtube '# Basic configurations #1 - Wheatstone bridge'](https://youtu.be/ZqAM_wQ35ow?si=8V4q9BYq1ZqlsRjg) (*best explenation*)
> - [Youtube '# Why you need a Wheatstone Bridge to get accurate Strain Gauge Readings](https://www.youtube.com/watch?v=L0uW1NHYdDQ) (*simple fast explenation*)
> - [Youtube '# Wheatstone bridge & its logic | Electric current | Physics | Khan Academy'](https://www.youtube.com/watch?v=-gcBVaCIKhE) (*calculations*)

---
###### Memory Card
![[Samsung_SaM_Notes_21_240516_160358_1.jpg]]

---
![[Pasted image 20230611185749.png]]

If we do a thevenim equivalent we find:
$$V_{TH} = V_0 = V \left(\frac{R_1}{R_1+R_4} - \frac{R_2}{R_2+R_3}\right)$$
And:$$R_{TH} = (R_1 \parallel R_4) + (R_2 \parallel R_3)$$
We can then divide $V_{TH}$ in DC offest ($V_C$) that is all component that do not depend on $R_1(T)$ (our sensor), and actual sensor component, all those parts that depend on $R_1$:
![[Pasted image 20230611185826.png]]
- $R_{TH1}$ and $V_{TH}$ depend on $R_1(T)$
- While $R_{TH2}$ and $V_{C}$ are **constant**.

If we attach a Differential Amplifier to $V_o$:
![[Pasted image 20230611185952.png]]
If Ideal:<br>![[Pasted image 20230611190157.png]]
Otherwise:<br>![[Pasted image 20230611190041.png]]

The $V_C$ generator represents the DC offset of your circuit:<br>![[Pasted image 20230611190403.png]]

As we have seen, we can define $R_1$ as:
![[Pasted image 20230611190554.png]]

We define a "**balanced bridge**" if this condition is met:
![[Pasted image 20230611190651.png]]

We define the $K$ ratio:
![[Pasted image 20230611190714.png]]

And now we calculate the dependency of $V_{TH}$ (the output) on the resisitances:
![[Pasted image 20230611190800.png]]
We perform a simple transformation, using:
- $\frac{R_4}{R_{io}} = K$ 
- $\frac{R_3}{R_{2}} = K$ 
- $R_1 = R_{io}(1+x)$ 
![[Pasted image 20230611190838.png]]

So if $x = 0$ as we have anticipated we have:
![[Pasted image 20230611190858.png]]

You can see that this ($\frac{V_{TH}}{V}$) is not a linear relationship:
![[Pasted image 20230611190838.png]]

We can also define it in a more confininet form:
![[Pasted image 20230611191153.png]]
