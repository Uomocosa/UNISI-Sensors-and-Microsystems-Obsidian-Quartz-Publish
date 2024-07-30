##### ***Remeber***:

> This is the scheme of a complete system for measuring temperature:<br>![[Pasted image 20231120190224.png|500]]<br>Where:
> - $T_x$ is the real temperature we want to measure, while $T_S$ is the temperature the sensor measures.
> - These two temperatures ($T_x$ and $T_S$) are not the same, since there is a ***Coupling with the Mesurand*** (drawned as a blank box $1.$), so remember that we cannot actual measure the real temperature, the temperature, specific heat and other properties of the sensor and all the other electronics will alter the measured value.
> - Also we also need to note that other errors are due to the **non-idealities** of the **sensor** ($2.$), **Read-Out Electronics** ($3.$), and **A/D** ($4.$).

> *We have also seen a simple example using the [[SaM ~ Real World Example • Standard RTD Sensor • PT100 Sensor|PT100 sensor]]*:<br>![[Pasted image 20231120191120.png|500]]
> - $I_{DC}$ is the current source.
> - $R(T)$ is the PT100 sensor.
> - $V_{io}$ is the bias voltage of the amplifier (read-out electronics).
> - We measure $V_A$ and we will convert it using the **A/D**, however we don't account for that in this example.<br>What we account for is the "complete accuracy" of the complete system, which is:$$\alpha \triangleq \frac{dV_A}{dT} = I_{DC} \cdot A_0 \cdot A \cdot R_0$$Where:
> 	- $R_0$ and $A$ are the resistance value at the reference temperature (usually **$0$°C**), and the first coefficient specific to the platinum resistance sensor, both defined by the [[SaM - Calendar Van Dusen Equation|Calendar Van Dusen Relationship]].
> 	- $A_0$ is the open-loop gain of the amplificator.
> - So it is important to notice that the [[SaM - Sensitivity|sensitivity]] of the complete system depends on the **current source** ($I_{DC}$), that means that a higher current improves the **SNR** (Signal to Noise Ratio), however it can create a [[SaM - Self-Heating|self-heating problem]].

---
###### Memory Card
![[Samsung_SaM_Notes_15_240515_183959_2.jpg]]

---
![[Lecture 9_230926_222449_8 2.jpg]]
![[Lecture 9_230926_222449_9 2.jpg]]
