##### ***Remeber***:

> We can create a simple oscillator using only capacitances, inductances and an [[SaM - Operational Amplifier|O.A.]], like so:<br>![[Pasted image 20230720170231 1.png|333]]
> - Moreover, we can create two different oscillators with this structure, the ***Colpits oscillator*** and the ***Hartley oscillator***.
> 	- ***Colpits oscillator***: $Z_1 = Z_3 = C$ and $Z_2 = L$.
> 	- ***Hartely oscillator***: $Z_1 = Z_3 = L$ and $Z_2 = C$.

> - For [[SaM - AT-Cut Quartz|AT-Cut quartz]] we have seen specifically the ***Colpits oscillator***, where the inductance $Z_2$ is replaced with the quartz, doing so garatnees that ==this circuit will oscillate only at frequency in which the quartz acts as an inductance, so for $f_0$ in the interval $[\omega_s ,\ \omega_p]$==:<br>![[Pasted image 20230720170240 1.png|333]]

> We can add a capacitance in series or in parallel to our quartz, doing so we will **shrink** the freqency range where the circuit oscillates (*fine tuning*), but we will also decrease the the $Q$-factor value (not good), defined as:$$Q = {1 \over \omega_s R_{eq}\kern2pxC_{eq}}$$
> Here is the base reference, with no added capacitances, so base range: $[f_s ,\, f_p]$:<br>![[Pasted image 20230720170240 2.png|500]]
> If we add a capacitance in series or in parallel:<br>![[Pasted image 20230720170240 3.png|500]]
> - **In series**: we increase $f_s$.
> - **In paralle**: we reduce $f_p$.
> - In both cases we reduce the range $[f_s,\ f_p]$

> Here is a real life example of tuning with $C_L$: #IMPORTANTE <br>![[Pasted image 20230720170247.png]]
> - Specifically we see how the bode plot changes with a capacitance $C_L$ in series to the quartz.

---
###### Memory Card
![[Samsung_SaM_Notes_24_240516_113108_3.jpg]]

---
![[Pasted image 20230720170231.png]]
- In principle $Z_i = X_i$ are reactances (capacitances or inductances)
- In the ***Colpits Oscillator*** example, this circuit will oscillate if two $Z$s are capacitances and the other is an inductances.
- If we take the ***Colpits Oscillator*** if we replace the $L$ (inductance) with the **AT-Cut Quartz***, then this circuit will oscillate only at frequency in which the quartz acts as an inductance, so for $f_0$ in the interval $[\omega_s ,\ \omega_p]$.

So, here's an example of a simple ***Colpits Oscillator***:
![[Pasted image 20230720170240.png]]
- First graph: **ideal situation**
- Second graph: If we find a capacitance **in series** to our quartz.<br>⇒ There is a shift of $f_s$.
- Third graph: If we find a capacitance **in parallel** to our quartz.<br>⇒ There is a shift of $f_p$.
- **NOTE**: In both the second and third graph, so if we add a capacitance, we **shrink** the range.<br>We can tune the frequency in this way.<br>But this will also change the $Q$-factor value, rember it is defined as:$$Q = {1 \over \omega_s R_{eq}C_{eq}}$$So there is a limit in tuning.

Real life example of tuning with $C_L$:
![[Pasted image 20230720170247.png]]

---