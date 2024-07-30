We have seen the [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|quarter bridge]], the [[SaM - Half Bridge • Calculation for the Maximum Sensitivity of a Resistive Bridge|half brige]].
Let's see how we can design a **full bridge** with $4$ [[SaM - Metal Strain Gauge • Passive Strain Sensor|strain sensors]], on a [[SaM - MEMS Cantilever|cantilever]]:
![[Pasted image 20230625114330.png|500]]
- $\varepsilon$ : [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|strain]]
- $w$ is the width. 
- $E$ is the [[SaM - Young and Poisson Modulus|Young modulus]]. 
- $F$ is the force, the force magnitude. 

Design of a full bridge:<br>![[Pasted image 20230625114341.png|200]]

$\frac{V_{TH}}{V}$ is equal to:<br>![[Pasted image 20230625114021.png|500]]
- $R_1 = R_3 =  R_0 (1 + G \varepsilon)$
- $R_2 = R_4 =  R_0 (1 - G \varepsilon)$

Continuing:<br>![[Pasted image 20230625114032.png]]

> So it is important to remember that: #IMPORTANTE $${V_{TH}\over V} = G \kern1px \varepsilon $$Supposing that we have taken $K = 1$, and [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|remember]] that $K$ is defined as:$$K = {R_{40}\over R_{10}} = {R_{30}\over R_{20}}$$

==So this is a linear circuit, the voltage output is related to the strain in a linear way, **always**==. 
==It's a **differential sensor**: that means that if I have variations, which are of the same sign like the ones due to temperature variation, they are cancelled by the structure of the brigdge==. 

 > **NOTE**:
 > I've put a zero in the subscript of the resitances to represent that they are sensors.
 
So ==**the full bridge is always linear and it rejects common mode disturbances**==. 

%% What?
==If I use the [[SaM - Metal Strain Gauge • Passive Strain Sensor|strain gauge]] in a [[SaM - Definition of a Resistive Bridge • Balanced Bridge • Thevenim Equivalent of the Resisitive Bridge|one-fourth bridge]], as we have found already, with $K=1$, which I actually can select, because strain gauges have a very small variation, so the $x$ is small, so with the value of $K=1$, so i will find the **maximum sensitivity** of a one fourth bridge==. 
%%

> ***What are the gains of using a full bridge instead of a half brige?***
> - If $(1+K) \gg x_1$ and $(1+K) \gg x_2$ the half bridge behaves linearly.<br>While ==the full bridge always behave **linearly**==.
> - It has higher [[SaM - Sensitivity|sensitivity]] than the **half bridge**.
> - However it requires four sensors, so requires more space, and has a higher cost.