##### ***Remeber***:

> Suppose we take an [[SaM - Ultrasonic Transducers (Piezoelectric Device)|ultrasonic transducer]] made of **PZT** and we attach it to another undefined material called, their acustic impedances have this values:
> - $Z_{{\text{PZT}}} = 32.5 {\text{kg} \over \text{m}^2 \kern2px \text{s}}$
> - $Z_{{\text{?}}} = 430 {\text{kg} \over \text{m}^2 \kern2px \text{s}}$
> - The unit of measure ${\text{kg} \over \text{m}^2 \kern2px \text{s}}$ is called a $\text{Rayl}$. 
> 
> Since we know that the [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|wavelength]] has this formula:$$\lambda_w = {v_l \over f_0}$$And that given an intial value for $v_i$ (the longitudinal velocity of the wave), we have the ratio with the resulting [[SaM - Reflection of an Ultrasonic Wave|transmitted wave]] is:$${v_{\tiny T} \over v_i} = {2 Z_{\text{PZT}}\over Z_{\text{PZT}} + Z_{\text{?}}}$$The same ratio is true for the wavelength.
> ==So for this particular example the resulting wavelength and velocity are only about $14\%$ of the initial values==.

> If we wish to increase this ratio, we could consider inserting a **matching layer**, with an acustic impedance of $Z_A$, between the *PZT* and the other material "*?*", like so:<br>![[Pasted image 20230720162251 1.png |500]]
> - So the formula, now becomes (ignoring the reflections, only the transmitted parts):$${v_{\tiny T} \over v_i} = {2 Z_{\text{PZT}}\over Z_{\text{PZT}} + Z_{\text{A}}} \cdot {2 Z_{\text{A}}\over Z_{\text{A}} + Z_{\text{?}}} $$Where:
> 	- $Z_A$: acustic impedance of the matching layer
> 	- $Z_{\text{PZT}}$: acustic impedance of the *PZT* layer $\left(Z_{{\text{PZT}}} = 32.5 \ \text{Rayl}\right)$. 
> 	- $Z_{?}$ : acustic impedance of the other material, or outside material $\left( Z_{{\text{?}}} = 430 \ \text{Rayl}\right)$.
> - ==If we suppose $Z_A = 200 \ {\text{Rayl}}$ we obtain that the ratio becomes $126.33\%$ of the intial value, so we have increased it==.<br>Without the matching layer: ${v_T \over v_i} = 0.1405$, with the matching layer ${v_T \over v_i} = 0.1775$.
> - As a rule of thumb we can consider a single acustic impedance $Z_M$, that combines the impedances of the material+matching layer:$$Z_M = \sqrt{Z_{\text{A}} \kern2px Z_{\text{PZT}} \kern3px }$$
> - Given the thickness of the *PZT* layer: suppose $t_{\text{PZT}} = {\lambda_{\omega} \over 2}$, we usually take the thickness of the matching layer as $t_A = {\lambda_{\omega} \over 4}$, so half of the PZT thickness (in the figure $t_A$ = $t_M$). #NOT_SURE_ABOUT_THIS 

---
###### Memory Card
![[Samsung_SaM_Notes_18_240516_152828_3.jpg]]

---
So keeping in mind that the wavelength is an important parameter, since it decides how the wave reacts to the medium.
W go back for a moment to our transducer, to the structure that we have described at the beginning:
![[Pasted image 20230720162251.png]]
- So we have said that the transducer is based on a piezoelectric slice, which is usually ***PZT***.
- A backing which is used to enhance the damping called **damper**.
- then we have a matching layer, and now we will explain how, and why, this matching layer is needed it.
- $Z_{PZT}$ acustic impedance of PZT.
- $Z_{M}$ acustic impedance of the target material (for example air).
- $Z_{A}$ acustic impedance of the matching layer.
- If we select a **matching layer** with a certain acustic impedance $Z_A$ we will have that the propagation speed, so also the wavelenght can be changed (reduced) at will.
- So transmit a wave to the matching layer then to the target material (example air), so the final wavelength, propagating inside the target material will be:$$\lambda_{M} = \cdot \frac{Z_{PZT} - Z_A}{Z_{PZT}+Z_A}\cdot \frac{Z_A-Z_M}{Z_A+Z_M} \cdot \lambda_i$$ #NOT_SURE_ABOUT_THIS 
- **NOTE**: This opearation redcues the wavelength, it cannot increase it. #NOT_SURE_ABOUT_THIS 
- There is a name for acustic impeadance unit of measure: "**Rayl**".
- **Professor's note**:<br>"*We have very different acoustical impedance between the PZT and air, a large part if the wave is reflected back instead of being transmitted to the air.<br>The a matching layer reduces the phenomena of reflection, and the matching layer is a material with an impedance which is selected according to this rule here:*"