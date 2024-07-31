![[Pasted image 20230718200738.png|500]]
- We take the primary sensor **mass spring damper** and we think of a fixed frame, as we have seen for strain gauges.
	- $M_s$ : sismic mass.
	- $K$ : spring coefficient.
	- $\lambda$ : damper coefficient.
	- $A(s) = \mathcal{L}[a(t)]$, where $a(t)$: acceleration
	- $R(s) = \mathcal{L}[r(t)]$l, where $r(t)$: displacemente between the resting position of the sismic mass and actual positon.
	- $r_{\infty} = \frac{M_S}{K}a_0$ : obtaing by using the final value theorem:$$\lim_{s \to 0} s \cdot F(s) = \lim_{t \to \infty} f(t)$$In this case we are ander the hypotesis of a constant acceleration ($a_0$)
	- $\alpha_r$ : sensitivity
- In this case, ==I have a sensor, which can turn an acceleration into a variation of a capacitance==.
- The capacitance value of capacitive accelerometer can calculated as:$$C = {C_0 \over 1 + \alpha \kern1px a_0}$$Where:
	- $C_0$ is the capacitance value at rest.
	- $a_0$ is the value of the constant accerelation.
	- $\alpha$ is the [[SaM - Sensitivity|sensitivity]].
---
###### Memory Card
![[Samsung_SaM_Notes_22_240516_105346_2.jpg]]

---