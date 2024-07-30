So instead of [[SaM - Quartz Oscillator|using a piezoelectric material]], we can construct a capacitance with a fixed and a **vibrating membrane**, and making it vibrate via a simple **AC exitation**:
![[Pasted image 20230720162340.png|500]]
- So capacitive sensors were especially used in air and they were of the "**polaroid type**".
- We also need a **DC exatation** value which was called "**the biasing**".
- You need to excite at the right frequency which is in accordance to the resonance of the structure.
- And you should provide many periods in order to get enough signals, so the excitation was a burst of many large 50 Volts-signals.


Now a special type of capacitive sensor which are called "**CMUT**" which is same structure as I show you but in *[[SaM - Traditional Sensors vs. MEMS • MEMS Technology|MEMS technology]]*.
It allows to use an **capacitive US transducer** for many different applications, because they succeeded in making a very small structure, and are used for obtaining **arrays**.
So you have many of these capacitive US transducer in a chip, in a single chip, which form an array.
We will see how and why the array can be considered very useful.

We have considered everything ideal up till now, that means that the medium is a perfect elastic medium without any losses.
**Obviously you always have some losses** due to **friction** due to **viscose** behavior and therefore you have to take into account that we have also an **attenuation in propagation**, we can measure the attenuation like so:
![[Pasted image 20230720162351.png|500]]
- So you need a  function which describes the attenuation:$$A(f,\ x_1) = A_0 e^{\large{- \alpha_0 \kern0px f  x_1}}$$This function here is an **exponential** function of the frequency $f$ and of the [[SaM - Generic Ultrasonic Wave Function • Longitudinal and Transvers Propagation Velocities of an Ultrasonic Wave|direction of propagation of the wave]] $x$
- The "***attenuation coefficient***" $\alpha_0$ changes a lot in different materials, ==in solid it is the smallest== #IMPORTANTE<br>==A smaller $\alpha$ means less attenuation==.


#IMPORTANTE 
So ==the higher is the frequency the smaller is the wavelength ⇒ the less we have strange phenomena== (like [[SaM - Scattering and Diffuse Reflection of an Ultrasonic Wave|scattering]]), instead we tend to have **[[SaM - Reflection of an Ultrasonic Wave|simple reflections]]**.
This is because if the wavelength becomes small it is like having a small scale of observation of the medium.
But ==the higher is the frequency the shorter is the [[SaM - Measurements & Measurement Types for Ultrasonic Beams|penetration depth of the wave]]==.

