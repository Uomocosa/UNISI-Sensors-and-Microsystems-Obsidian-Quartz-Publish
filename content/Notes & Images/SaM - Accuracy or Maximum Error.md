###### Memory Card
![[Samsung_SaM_Notes_02_240515_104233_1.jpg]]

---
You want to know the quantity $g_v$ (real value), you use a sensor to measure it, the sensor is not perfect (we expect the sensor to have an input-output function $f$ instead this specific sensor has a function $f_N$ different from the real one $f$).<br>So instead of reading the value $e_v$ (expected/real value)  you will read an electrical value $e_m$, then you will "traduce" this already wrong value into the measured value $g_m$ using this formula $g_m = f^{-1}(e_m)$ where $f$ is the correct function, given by the producer, but not the nominal one $f_N$ so it will introduce another error.<br>So this are the passages:
	1. $e_m = f(g_v)$ 
	2. $g_m = f_N^{-1}(e_m)$
	3. $\tilde{e}_g = g_v - g_m \kern25px \text{or} \kern25px \tilde{e}_g = g_v - f_{N}^{-1}(f(g_v))$
	4. We define the accuracy as: $\max\left({\tilde{e}_g}\right)$
***

![[Pasted image 20230624095623.png]]
- ==Accuracy of a sensor is usually intended as **maximum error**==. 

![[Pasted image 20230624100728.png]]
- $g_v$ : true value of $g$
- $g_m$ : measured value of $g$

Which is equivalent to:
- $g_v$ : true value of $g$
- $f^{-1}(e_m)$ : inverse function of the measured output of the sensor ($e_m$). 

![[Pasted image 20230624101613.png]]
- This is ==$f(g)$, the true relationship between $g$ and $e$ of your sensor==, of the specific sensor that you are using, ==you don't know this one, this is the **true** one==. 

![[Pasted image 20230624101031.png]]
- $f(g)$ : **true input-output function**. 

![[Pasted image 20230624101136.png]]
![[Pasted image 20230624101539.png]]
![[Pasted image 20230624101838.png]]
