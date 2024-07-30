We have seen how to model a [[SaM - Thermal Lumped Parameter System|thermal system]], so let's take an example with a **target** $(x)$, our sensors with which we measure the temperature $T_S$, all coupled with the **ambience temperature** $\left(T_A \right)$:<br>![[Pasted image 20240116192926.png|333]]
We want to measure $T_X$, but we can only access it via $T_S$.
Suppose at regime $T_S$ reaches the value $T_S{_{\kern-1px \infty}}$, the complete formula is:$$T_S(t) = T_S{_{\kern-1px \infty}}\left(1 - e^{-\large{t \over \tau}}\right)  + T_S\left(0^-\right) \kern2px e^{-\large{t \over \tau}} $$Here's the graph:<br>![[Pasted image 20240116194241.png|500]]

If we perform the calculations, such that:$${T_X - T_S \over R_{XS}} + {T_A - T_S \over R_{SA}} - C_S T_S \cdot s + C_S T_S(0^-) = 0$$We will find:$$\begin{array}{l} T_S{_{\kern-1px \infty}} = {\large{T_A \kern2px R_{XS} \over R_{XS} + R_{SA}}} + {\large{T_S \kern2px R_{SA} \over R_{XS} + R_{SA}}} \\[3px] \tau = C_S  {\large{R_{XS} \kern2px R_{SA} \over R_{XS} + R_{SA}}} \end{array}$$==So if we have $R_{SA} \gg R_{XS}$, then we will find: $T_S{_{\kern-1px \infty}} \approx T_A$==.
(*Often we wait $5 \tau$, so in this case for $R_{SA} \gg R_{XS}$ we would need to wait at least $5 C_S \kern1px {R_{XS}}$)

#IMPORTANTE 
We have defined the thermal reisistance in two ways, depending if the thermal conduction happens via [[SaM - Heat Convection • Thermal Resistance|motion of matter (heat convection)]] or [[SaM - Heat Conduction • Thermal Resistance|not (heat conduction)]].
Here's a table for the value for the **thermal conductivity** ($K$):

|                                                                         | _Still Air_ | _Glass_ | _Gold_   | _Diamond_ |
| ----------------------------------------------------------------------- | ----------- | ------- | -------- | --------- |
| $K \left(\left[{\text{W} \over \text{°K} \cdot \text{m}}\right]\right)$ | $10^{-2}$   | $1$     | $10^{2}$ | $10^{3}$  |
- **_Still Air_ means**: "_A porous material filled with Air_", so we are talking about **only convection**, no conduction.
- A bigger coefficient means a **lower thermal resistance**, so a better coupling, and a **faster heat transfer**.<br>So "***still air***" is an **thermal insulator**

---
Calculations:
![[Pasted image 20230713163922.png]]
![[Pasted image 20230713163936.png]]
![[Pasted image 20240212180846.png]]

