##### Remember

> We take for instance a sine plane wave, and we take only a forward-propagating wave, so we define $U_{1F}$ that we said was a generic function as:$$U_1(t,\, x_1) = U_{1F}\left(t - \frac{x_1}{v_l}\right) + 0 = A \sin\left(2\pi f_0\left(t-\frac{x_1}{v_l}\right) + \varphi\right)$$Where: $f_0$ is decided by the freqency at which the [[SaM - Ultrasonic Transducers (Piezoelectric Device)|piezoelectric ultrasonic transducer]] vibrates.

> Here's a plot of the wave:<br>![[Pasted image 20230719131639 1.png|500]]
> - "TX" is the **ultrasonic trasnducer**.<br> It vibrates at a frequency $f_0$, related to the ratio $\sqrt{\frac{K}{m}}$.
> - So I generate the wave in the medium with a **wavelenght** $\lambda_{w}$ well known.
> - Remember the **wavelenght** is defined as:$$\lambda_w = {v_l \over f_0}$$The wavelenght is defined using the **longitudinal velocity of a wave**.<br>For [[SaM - Transverse Waves or Shear Waves|transverse waves]], we have approximately **half the wavelength**, since $v_t \simeq {1 \over 2}v_l$.

> We can look at some standard values of the **frequency range** and resulting **wavelenght range**, used for different materials: #IMPORTANTE <br>![[Pasted image 20230720162038.png]]
> - Ultrasonic transducers use different frequency to perform ultrasonic analysis in different media.
> - ==For transverse wave, we have approximately half the wavelength, since $v_t \simeq {1 \over 2}v_l$==.
> - ==The wavelength is an important parameter of the wave field==.
> - Depending on the wavelength, different interaction with obstacle occurs.<br>We can have: [[SaM - Reflection of an Ultrasonic Wave|reflection]], [[SaM - Scattering and Diffuse Reflection of an Ultrasonic Wave|scattering or diffuse reflection]] of the wave, ==depending on the size difference between the obstacle and the wave==.

---
###### Memory Card
![[Samsung_SaM_Notes_18_240516_152828_2.jpg]]

---
We take for instance a sine plane wave, and we take only a forward-propagating wave, so we define $U_{1F}$ that we said was a generic function as:$$U_1(t,\, x_1) = U_{1F}\left(t - \frac{x_1}{v_l}\right) + 0 = A \sin\left(2\pi f_0\left(t-\frac{x_1}{v_l}\right) + \varphi\right)$$

![[Pasted image 20230719131639.png]]
- We can define the wavelenght $\lambda$, related to both speed and frequency.
- $v_l$ : wave speed.
- At a fixed frequency $f$ ⇒ $\lambda$ depends linearly on the $v_l$, so the larger the speed the larger the wavelength.
- If we think about a small transduer **TX**, that vibrates at the frequency $f_0$ related to the ratio $\sqrt{\frac{K}{m}}$, so I generate the wave in the medium with a wavelenght $\lambda_{w}$ well known.
- The plot you see is a "photograph" of the wave, so the wave at a fixed time $t_0$, and you see how it propagates along $x_1$, and how the wavelength $\lambda_{w}$ is defined.
- We can use the wavelength or speed to find some difects in a material, since for example the wave travels in air 20 times slower than in steel, if a block of steel presents a pocket of air an ultrasonic sensor can find it.

![[Pasted image 20230720161946.png]]
- We consider it only going forward.
- We can also define the wave number: $K_{w}$, and the wave vector: $\vec K_{w}$

We can look at some values:
![[Pasted image 20230720162038.png]]
(this is considered the longitudinal transverse speed)

⇒ Therefore, ultrasonic transducers use different frequency to perform ultrasonic analysis in different media.

==For transverse wave, we have approximately half the wavelength, since $v_t \simeq {1 \over 2}v_l$==.

==The wavelength is an important parameter of the wave field==.
Sepending on the wavelength, different interaction with obstacle occurs.
So we can have a **reflection**, **scattering**, **diffraction**, ==depending on the ratio between the obstacle and the wave==.
