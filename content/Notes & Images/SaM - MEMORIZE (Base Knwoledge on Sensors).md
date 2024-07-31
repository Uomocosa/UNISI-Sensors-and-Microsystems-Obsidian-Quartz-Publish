##### List of things to memorize:
![[SaM - Base Knwoledge on Sensors]]

---

![[SaM - Types of Sensor]]

---
![[SaM - Types of Active Sensors]]

---
![[SaM - Traditional Sensors vs. MEMS • MEMS Technology]]

---
![[SaM - Definition of Primary Sensor]]

---
![[SaM - Types of Primary Sensors]]

---
![[SaM - Front End Electronics Strategies]]

---
###### [[SaM - Characteristics of a Sensor|Characteristics of a Sensor]]
1. [[SaM - Sensitivity|Sensitivity]]:$$\alpha = {df \over dg}$$Relative sensitivity:$$\alpha_r = {1 \over V}{df\over dg}$$
2. [[SaM - Resolution|Resolution]]: it is the minimum variation of the input, which causes an output variation, **recognizable from noise**.<br>Usually we take **10 times larger** than noise.
3. [[SaM - Working Range & Safe Range|Working Range & Safe Range]]:<br>![[Pasted image 20230624095558.png|500]]
4. [[SaM - Accuracy or Maximum Error|Accuracy]] (or **Maximum Error**)<br>You want to know the quantity $g_v$ (real value), you use a sensor to measure it, the sensor is not perfect (we expect the sensor to have an input-output function $f$ instead this specific sensor has a function $f_N$ different from the real one $f$).<br>So instead of reading the value $e_v$ (expected/real value)  you will read an electrical value $e_m$, then you will "traduce" this already wrong value into the measured value $g_m$ using this formula $g_m = f^{-1}(e_m)$ where $f$ is the correct function, given by the producer, but not the nominal one $f_N$ so it will introduce another error.<br>So this are the passages:
	1. $e_m = f(g_v)$ 
	2. $g_m = f_N^{-1}(e_m)$
	3. $\tilde{e}_g = g_v - g_m \kern25px \text{or} \kern25px \tilde{e}_g = g_v - f_{N}^{-1}(f(g_v))$
	4. We define the accuracy as: $\max\left({\tilde{e}_g}\right)$
5. [[SaM - Calibration|Calibration]]:<br>![[Pasted image 20230624102000.png|500]]
6. [[SaM - Non-Linearity Error|Non-Linearity Error]] (only for linear sensors): the maximum distance between the nominal or **ideal linear value** ($f_N(g)$, *given by the producer*), and the **real value** ($f(g)$, *specific to the sensor at hand*).
7. [[SaM - Rise Time|Rise Time]]: For first order system we can also define the rise time which is the time needed to the output to pass from 10% of the final value to 90% of the final value

---
###### [[SaM - Sensor Linearization]]
[[SaM - End Point  Linear Approximation & Linear Regression|End Point  Linear Approximation & Linear Regression]]:<br>![[Pasted image 20230417153940.png]]

[[SaM - Linearized Sensors for a Small Range|Linearized Sensors for a Small Range]]:<br>![[Pasted image 20230624112425.png]]

---
###### [[SaM - Ideal Linear Sensor]]
The ideal sensor is linear.
A linear sensor will have constant **sensitivity** $(\alpha \in \mathbb{R})$.

An ideal sensor will have a **linear dynamic description, with infinite speed**:$$e(t) = \alpha \cdot g(t) + k$$**Infinite speed**: "*no delay between input and output*".

---
###### [[SaM - Definition of Isotropic and Anisotropic Materials]]
- Isotropic materials exhibit the **same mechanical properties in all directions**.
- Anisotropic materials, on the other hand, have **different mechanical properties in different directions**.

---
###### [[SaM - Physical Dependencies of a Sensor]]
We will see 3 different accelerometer *each with a different kind of operational principle*:
1. Using the ==**material properties**==: "***Charge Accelerometer***" (Piezoelectric).
2. Using the ==**dependency on the geometry**==: "***Capacitive Accelerometer***".
3. Using the ==**electromagnetic coupling**==: "***Magnetic Accelerometer***".