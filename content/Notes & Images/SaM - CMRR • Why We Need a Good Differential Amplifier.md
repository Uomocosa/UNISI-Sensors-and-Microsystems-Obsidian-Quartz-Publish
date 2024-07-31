##### ***Remeber***:

> Consider a simple [[SaM - Operational Amplifier]], used as a [[SaM - Differential Amplifier]], however non-ideal, specifiaclly we consider these internal resistances:<br>![[Pasted image 20230626201429 1.png|500]]
> Also attached to this amplifier an [[SaM - Half Bridge • Calculation for the Maximum Sensitivity of a Resistive Bridge|half bridge]]:<br>![[Pasted image 20230626201510 1.png|500]]
> If we consider $R_{10} = R_{20} = R_3 = R_4$, or $K = 1$, so that we can [[SaM - Half Bridge • Calculation for the Maximum Sensitivity of a Resistive Bridge|maximize the sensitivity]], we will have that the output of this simple bridge+amplifier is equal to:$$V_0' = A_d V_d + A_c \left(V_{CC} + \frac{V_d}{2}\right)$$If we talk about [[SaM - Metal Strain Gauge • Passive Strain Sensor|strain gauges]], my "informative part", $V_d$ is **really small**
> ⇒ I'll have a very small variation of the signal $V_d$ (maybe about some ***millivolts*** or even ***microvolts***).
> ==This is the reason why I need a good differential amplifier==
> Also a good differential amplifier is an amplifier with high [[SaM - CMRR (Common Mode Rejection Ratio)|CMRR]], ideally infinte.

---

Why We Need a Good Differential Amplifier?
![[Pasted image 20230626201332.png|500]]

We consider a simple scheme of a differential amplifer, considering some non linearities as the **common mode resistance** ($R_C$) and **differential resistance** ($R_D$).
![[Pasted image 20230626201429 1.png|500]]
- $V_c$ is the voltage on $R_{C1}$ (the common mode resistance)
- $V_d$ is the voltage on $R_{d}$ (the differential resistance)

We attach a **resistive bridge** before it:
![[Pasted image 20230626201510 1.png|500]]

If we consider $R_1 = R_2 = R_3 = R_4$, so $K = 1$, we will have that the output of this simple bridge+amplifier is equal to:
$$V_0' = A_d V_d + A_c \left(V_{CC} + \frac{V_d}{2}\right)$$
If we talk about **strain gauges**, also my "informative part", $V_d$ is **really small**, so I'll have a very small variation of the signal $V_d$ (maybe about some ***millivolts*** or even ***microvolts***).
==This is the reason why I need a good differential amplifier==.
Also a good differential amplifier is an amplifier with high CMRR, ideally infinte.
