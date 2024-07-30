###### Memory Card
![[Samsung_SaM_Notes_15_240515_183959_3.jpg]]
![[Samsung_SaM_Notes_21_240516_160358_3.jpg]]

---
Suppose we want to measure a temperature in a small temperature range $T \in \left[T_{MIN} \div T_{MAX}\right]$.
We measure it with a [[SaM - Ideal Linear Sensor|linear sensor]], suppose an [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|RTD]], this is its function:<br>![[Pasted image 20240116182444.png|500]]

And for the input to the read-out electronics we use a simple **voltage divider** like so:<br>![[Pasted image 20240116182412.png|333]]

So we will have the output:$$V_0 = V_{DC} {R_{REF} \over R(T) + R_{REF}}$$With a maximum, minum, and the reference value voltage defined as:$$\begin{array}{l} V_{0_{MIN}} = V_{DC} {\large{R_{REF} \over R_{MAX} + R_{REF}}} \\[5px] V_{0_{MAX}} = V_{DC} {\large{R_{REF} \over R_{MIN} + R_{REF}}} \\[5px] V_{\small {REF}} = V_{DC} {\large{R_{REF} \over R(T_{REF}) + R_{REF}}} \end{array} $$Where: $T_{REF}$ is taken as $T_{MAX} - T_{MIN} \over 2$.

So the output of this system will have this function:<br>![[Pasted image 20240116183300.png|333]]
- $V_{\small {REF}}$ can be seen as the **offset** of the system.
- While $\left[V_{0_{MIN}} ,\ V_{0_{MAX}}\right]$ is its **dynamic range**, the information given by the sensor lies all in this small range that we will call $\Delta V$.

This way we don't fully utlize the range given by the **acquisition system** (**A/D**) in a [[SaM - Accuracy of the Complete Measurement System|complete measurement system]], that goes for example between $\left[-V_{DC},\ + V_{DC} \right]$.
Ideally I wold select an amplifier that amplify the small range $\Delta V$ into the whole range of the **aquisistion sysmtem**, so $2 V_{DC}$.
But in this case we cannot do so becasue we have an **offset**.

To solve this we need to compensate the offset, so bring the output signal to have a $V_{\small{REF}} = 0$:<br>![[Pasted image 20240116183919.png|500]]
To do so we can use a [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|balanced bridge]], instead of a **voltage divider**, like so:<br>![[Pasted image 20240116184017.png|500]]

And even if we use a good linear solution for meauring a resisitance sensor:<br>![[Pasted image 20240116184754.png|333]]
We need to consider that the sensor may be distant from the read-out electroncis, and we might need to consider the [[SaM - 2 Wires Measurement with Wire Resisitances|wires resistances]], and this will result into another offset.

---
##### Conclusion on Amplifier's DC Offsets
![[Pasted image 20230717114244.png]]
- ==And the part which cannot be corrected are the drifts of the offset==, and this can't be corrected.
- ==And usually you can consider drift as $1\over 10$ of the value of the offset==, in a span of about, let's say, $50$ degrees, the whole temperature span, which you can have.