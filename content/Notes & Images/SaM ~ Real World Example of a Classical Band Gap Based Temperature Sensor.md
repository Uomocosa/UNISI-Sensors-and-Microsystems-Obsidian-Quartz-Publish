##### ***Remeber***:

> - This is **linear**, but only if the [[SaM - Defintion of Thermocouples • Law of Thermocouples • Types of Thermocouples • Extension Wires|thermocouple]] is linear. 
> - Basic **TMP35** sensor: $\alpha = 41 {\mu\text{V} \over \text{°C}}$. (used for compensation)
> - Using this structure (thanks to both sensor and thermocouple) we go from the original sensitivity which is $41$ **micro volt** per degree, to a larger sensitivity which is $10$ **millivolt** per degree.

---

![[Pasted image 20230719123914.png]]
- So this is an example and it is a **complete instrumentation amplifier and thermocouple called junction compensator on a monolithic chip**.
- You only have to add the thermocouple, which is the only external part here, everything else is in the chip.
- So it becomes a cold junction, so there is the need for a isothermal block, since you need to measure the temperature of this junction here, and this is performed by means of this internal voltage $V_R$, "output" of the **TMP35** (actually the output is a resistance).
- At the end we have also this amplifier here which amplifies the voltage and we go from the original sensitivity which is $41$ **micro volt** per degree, to a larger sensitivity which is $10$ **millivolt** per degree. #NOT_SURE_ABOUT_THIS (The increase in sensitivity should be mostly due to the termocouple)
- This is **linear**, but only if the thermocouple is linear. 
