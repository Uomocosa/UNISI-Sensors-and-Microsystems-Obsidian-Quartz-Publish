##### ***Remeber***:

> Suppose to have an accelerometer where we measure the [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|strain]] via a [[SaM - Metal Strain Gauge • Passive Strain Sensor|strain gauge]], here's a simple structure:<br>![[Pasted image 20230625114240.png]]
> - All the springs and dumpers can be "merged" together in a single spring.
> - ==The mass can move in every direction and we don't exit from the **elastic regime**==. 
> - The resistances values will be:$$\begin{array}{l}R_{1,\,3} = R_0\left(1-G\left({m_s\over K \cdot l}a\right)\right) \\ R_{2,\,4} = R_0\left(1+G\left({m_s\over K \cdot l}a\right)\right) \end{array}$$Where: ${m_s\over K \cdot l}a = \varepsilon_l$
> - Also we have to consider that the strain gauges are **pre-deformed** so:$$\begin{array}{l}R_{1,\,3} = R_0\left(1 - G\left({m_s\over K \cdot l}a\right) + G\varepsilon_0 \right) \\ R_{2,\,4} = R_0\left(1 + G\left({m_s\over K \cdot l}a\right) + G\varepsilon_0 \right) \end{array}$$

---

![[Pasted image 20230625114240.png]]
- All the springs and dumpers can be "merged" together in a single spring.
- ==The mass can move in every direction and we don't exit from the **elastic regime**==. 

![[Pasted image 20230625114248.png]]
Where:
- $r_{\infty}$ : regime value of the elongation.
- $A$ : amplitude of the acceleration.
- $m_S$ : sismic mass.
- $K_{eq}$ : elastic constant of the equivalent system.
- $K_{S}$ or $K$ : elastic constant of a single sensor/spring.
- $l$ : length of the spring.
- $\varepsilon_1$ : strain in the single $x$ direction we are considering.
- $\varepsilon_l$ : longitudinal strain.
- $\lambda_{eq}$ : equivalent damp coefficient.
- $G$ : the **strain gauge factor**.

So I have an output, which is linearly related to the acceleration. 

Actually, since they are pre-deformed, I have to add to this deformation, due to acceleration, the ones which were impressed at the beginning, so $+G\varepsilon_0$ :<br>![[Pasted image 20230625114254.png]]
