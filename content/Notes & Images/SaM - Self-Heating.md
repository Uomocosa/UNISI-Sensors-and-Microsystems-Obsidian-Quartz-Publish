##### ***Remeber***:

> - Using a [[SaM - Thermal Lumped Parameter System|Common Thermal Lumped Parameter System]]:<br>![[Pasted image 20231123193338.png]]<br>Where the [[SaM - Heat Stored in a Body • Thermal Capacitance|Thermal Capacitance]] of the sensor is much smaller than that of the body of which we want to measure the temperature $T_X$, this is consider to have a simpler system.
> 	- **NOTE**: $\dot Q_S$ is a **current generator**.<br>$\dot Q_S$ is the **heat flux** or [[SaM - Lumped Parameter Systems|flow quantity for the thermal lumped parameter systems]], its units of measure is $\left[W\right]$.
> - The temperature of the sensor $T_S$ is what we measure, we want $T_S$ to be as much closer to $T_X$ as possible.
> - We consider to measure the temperature of the sensor **at regime** ($T_{S\infty}$), so when the **transient** has subsided.
> - As a matter of fact if we perform the calculation we obtain that:$$T_{S\infty}= T_X + R_{XS}\dot{Q}_S$$Where:
> 	- We can see $R_{XS}\dot{Q}_S$ as the difference $\Delta T$ or **measurement error**.

---

> - We also need to say that, the difference between the real and measured temperature:$$\Delta T = R_{XS}\dot{Q}_S$$Depends on:
> 	- $R_{XS}$ the **Thermal Resistance** due to [[SaM - Heat Convection • Thermal Resistance|heat convection]] or [[SaM - Heat Conduction • Thermal Resistance|conduction]], which depends on the **motion of matter**, and **material type** both of the sensor and the target, and other properties.
> 	- ==While more importantly $\dot Q_S$ depends on the voltage ($V$) and current ($I$) feeding into the sensor, from this factor we have the problem of **self-heating**, since a higher current or voltage will increase $\dot Q_S$, so it will increase the difference $\Delta T$==.
> - We have also seen [[SaM - Reduce the Effect of Self-Heating|how to reduce the effect of self-heating]].

---
###### Memory Card
![[Samsung_SaM_Notes_21_240516_160358_5 1.jpg]]

---
![[Pasted image 20230713163902.png]]
