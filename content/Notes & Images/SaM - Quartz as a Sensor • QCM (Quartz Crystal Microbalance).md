###### Memory Card
![[Samsung_SaM_Notes_14_240516_113346_3.jpg]]

---
Taken a quartz slice in between two "***functionalization layer***":
![[Pasted image 20230720170400.png|500]]
- ==The "***functionalization layer***" is a special material that can absorb a "special target molecule", and when it does so it increases its mass==.<br>We will model this added layer with an added mass, so an impedance of this value will be added in the ciruit: $$Z_{M} = \Delta m \kern15px \Rightarrow \kern15px  {Z_{M}\over k^2 d} ={\Delta m\over k^2 d}$$Where:
	- $\Delta m$: mass of the "***functionalization layer***"
	- $K$ : cosntant defined by the geometry of the piezoelectric crystal
	- $d$ : piezoelectric coefficient.
- The rest of the circuit is [[SaM - AT-Cut Quartz|as before]].<br>==This time we cannot the mass of the quartz $\left(Z_m\right)$==, [[SaM - Quartz Oscillator|as we have done before]].

So we can change the $L_{eq}$ value incorporating $Z_{\Delta M}$:$$L_{eq}' = L_{eq} + {\frac{\Delta m}{K^2 d}} \kern15px\Rightarrow\kern15px \left\{\begin{array}{l} \omega_s' = {\huge{1 \over {\sqrt{L_{eq}' \cdot C_{eq}}}}}   \\[5px] \omega_p' = {\huge\sqrt{{C_{\kern-2pxE} + C_{eq} \over C_{\kern-2pxE} \kern1px L_{eq}' \kern1px C_{eq}}}}  \end{array}\right.$$

![[Pasted image 20230720170409.png]]
- So we have a relation between $\omega_s'$ and $\Delta m$, so as the "***functionalization layer***" absorbs the target molecule we will se a decrease of $\omega_s'$.
- The name of this sensor is: **QCM** (*Quartz Crystal Microbalance*), and it is based on the concentration of the target species (that gets absorbed by the functionalization layer).
