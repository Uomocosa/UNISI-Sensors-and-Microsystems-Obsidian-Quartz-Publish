1. [[SaM - Sensitivity|Sensitivity]]
2. [[SaM - Resolution|Resolution]]
3. [[SaM - Working Range & Safe Range|Working Range & Safe Range]]
4. [[SaM - Accuracy or Maximum Error|Accuracy]] (or **Maximum Error**)<br>You want to know the quantity $g_v$ (real value), you use a sensor to measure it, the sensor is not perfect (we expect the sensor to have an input-output function $f$ instead this specific sensor has a function $f_N$ different from the real one $f$).<br>So instead of reading the value $e_v$ (expected/real value)  you will read an electrical value $e_m$, then you will "traduce" this already wrong value into the measured value $g_m$ using this formula $g_m = f^{-1}(e_m)$ where $f$ is the correct function, given by the producer, but not the nominal one $f_N$ so it will introduce another error.<br>So this are the passages:
	1. $e_m = f(g_v)$ 
	2. $g_m = f_N^{-1}(e_m)$
	3. $\tilde{e}_g = g_v - g_m \kern25px \text{or} \kern25px \tilde{e}_g = g_v - f_{N}^{-1}(f(g_v))$
	4. We define the accuracy as: $\max\left({\tilde{e}_g}\right)$
5. [[SaM - Calibration|Calibration]]
6. [[SaM - Non-Linearity Error|Non-Linearity Error]] (only for linear sensors)
7. [[SaM - Rise Time|Rise Time]]