##### ***Remeber***:

> Now let's consider the "common mode resistances" of an amplifier, so $R_{C1} ,\ R_{C2} \neq 0$, for semplicity let's say $R_{C1} = R_{C2}$, and attached to it a [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|resistive bridge]], like we have seen [[SaM - Non-Ideal Operational Amplifier • Input and Output Resistances|before (Thevenim Equivalent)]]:<br>![[Pasted image 20240124171936.png|500]]
> - $\Delta R$ is the resisitve variation, due to the sensor.
> - $R_{C1} = R_{C2} = R_C$.
> - $R_C \gg R_{TH}$.
> - #NOT_SURE_ABOUT_THIS <br>For this circuit given these resistance values, we have: $V_{CC} \approx V_{c}$.<br>Where: $V_{c} = V_{CC} + {V_{TH}\over 2}$.<br>$V_{TH} = \left({R_1 \over R_1 + R_4}-{R_2 \over R_2 + R_3}\right)V$<br>$V_{CC} = {R_2 \over R_2 + R_3} V$
> - $A_{d_{\text{topology}}} = A$.
> - To find $A_{c_{\text{topology}}}$ we calculate:$$A_{c_{\text{topology}}} = \left.{V_{D}\over V_{c}}\right|_{V_{TH}=0}$$ #NOT_SURE_ABOUT_THIS (Why can we define it like this?)<br>Resulting in:$$A_{c_{\text{topology}}} = A_d\frac{\Delta R}{R_C}$$[[SaM - Lecture 12_03 • CMRR • Calculations|Here]]'s the calculations.
> - If we consider this ciruit topology even if the Amplifier is ideal, the CMRR will not be equal to infinity.

> The CMRR only due to circuit topology will be given by:$$\text{CMRR}_{\text{topology}} = \frac{A_d}{A_{c_{\text{topology}}}}={R_C \over \Delta R}$$Since:$$A_{c_{\text{topology}}} = A_d\frac{\Delta R}{R_C}$$So the Complete CMRR (also considering the resistance tollerances) is given by:$$\frac{1}{\text{CMRR}} = \frac{1}{\text{CMRR}_{\text{topology}}} + \frac{1}{\text{CMRR}_{\text{R}}}$$Similar to how we found [[SaM - CMRR • Calculation of the CMRR (Stage II) based on Resistance Tollerances|the CMRR due to resistance tollerances]]

---
###### Memory Card
![[Samsung_SaM_Notes_13_240515_175715_3.jpg]]

---
And the last thing that I want to take into account is the effect of the topology. 
So the **CMRR** do to the circuit topology. 
What do I mean? 
I suppose to have a perfect differential instrumentation amplifier. 
So it has a **CMRR** which is infinite. 
That could be the effect of the common mode voltage at the input of the circuit. 
Even in this case, do simply to the circuit topology.
So we go back to our source-equivalent circuit:
- $V_C$ is essentially the main source of common mode voltage, so we can approximate the common mode voltage with $V_{CC}$.<br>Because $V_{CC}$ actually would be (and we know that $V_{TH}$ is small):
- I take $R_{C1} =R_{C1}=R_C$.
- You see that I didn't put here the differential resistance, meaning that I consider $R_D$ to be infinite.

![[Pasted image 20230718184044.png]]
![[Pasted image 20230718184057.png]]
![[Pasted image 20230718184105.png]]
And at the end I can write the overall **CMRR**:
$A_D$ : $A_D$ of the overall structure. 
$A_C$ : $A_C$ of the overall structure. 