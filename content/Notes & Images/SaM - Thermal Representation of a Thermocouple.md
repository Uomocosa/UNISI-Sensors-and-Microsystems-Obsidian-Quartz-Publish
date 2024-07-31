The [[SaM - Lumped Parameter Systems|lumped parameter system]], specifically the [[SaM - Thermal Lumped Parameter System|thermal lumped parameter system]] of a thermocouple is like so:
![[Pasted image 20230719123615.png]]
- $T_X$ is my the temperature of the target body.
- $T_2-T_1$ is what I sense.
- ==The thermocouple is characterized by a very small capacitance ($C_1$), since it is a conductive metal==.
- The rest is a standard thermal circuit with $T_A$ : ambience temperature.
- Becouse of thermal coupling and thermal capacitances, this gives you always a temperature $T_1$ which is different from $T_x$.
- Tho there are some strategy for obtaining good measurement, so this problem can be neglected.

---

And we have already seen that there is a possibility of performing an **ACJC** (*[[SaM - Cold Junction for Thermocouples|automatic cold junction compensation]]*), using for example an [[SaM - Definition of RTD Sensors • Resistive Temperatrure Detector Sensors • TCR (Temperature Coefficient of Resitance)|RTD sensor]].
![[Pasted image 20230719123624.png]]
- The front-end will contain another sensor, and a Voltage amplifier (we suppose a slow-varying signal)<br>We suppose to operate with slow varying quantities, because usually the temperature doesn't vary fast.<br>So we are operating with **DC coupled amplifier**.
