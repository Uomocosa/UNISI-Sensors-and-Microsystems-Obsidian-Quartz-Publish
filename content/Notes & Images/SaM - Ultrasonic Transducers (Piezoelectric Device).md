##### ***Remeber***:

> Here's a basic strucuture for an ultrasound transducer:<br>![[Pasted image 20230719131157.png|500]]
> - ***Structure***:
> 	- A [[SaM - Piezoelectric Effect|piezoelectric]] slice of material (like [[SaM - Quartz Oscillator|quartz]]).
> 	- An added dumper $\lambda$.
> 	- A source voltage for exiting the piezoelectric.
> 	- A read-out (an amplifier) to read the output from the piezolectric.
> - ***Workings***:
> 	1. We exite the piezoelectric, which is deformed [[SaM - Piezoelectric Effect in Details • Direct and Inverse Piezoelectric Effect|inverse piezoelectric effect]], and we make it vibrate.
> 	2. The vibration generates a [[SaM - Ultrasonic Waves|wave]].
> 	3. The wave bounces off the **target**, and returns to the piezoelectric, make it vibrate again.
> 	4. We measure the new vibration with the read-out.
> - $V_g$ is usually a **pulse**:<br>![[Pasted image 20230925111343.png|333]]

> This device can be used both as an **actuator** (it produces [[SaM - Ultrasonic Waves|ultrasonic waves]] via the vibration of the **piezoelectric crystal**) or as a **sensor** (so as a sensor for ultrasonic waves).<br>This is reflected in its equivalent electrical circuit:<br>![[Pasted image 20230719131223.png|500]]
> - *USTX* is the **Ultrasonic Transducer**, modelled just before.
> - The two diodes are a **protection circuit**, for read-out part, ==it protects the amplifier when using the device as a transducer==.<br>The two diodes cap the frequency that passes to the amplifier at around $\pm 600$ **mV** (this votlage is defined by the diodes).
> - This is the input-output voltage of this circuit:<br>![[Pasted image 20230925111343.png|333]]

> Things to know about this device:
> - There is a difference in the types of [[SaM - Ultrasonic Waves|waves]], depending on the type of target material:
> 	- If we use an *USTX* on a linquid (or human tissues for biomedical applications), or in a gas we are talking about [[SaM - Elastic Waves and Acustic Waves • Calculation of the Wave Equation|acustic waves]].
> 	- Instead if we use it in a solid we are talking about [[SaM - Elastic Waves and Acustic Waves • Calculation of the Wave Equation|elastic waves]]
> - Usual case scenarios are: **biomedical applications**, **non-contact measure**, **NDT** (*non estructive testing*)
> - We usually use this device in "**[[SaM - Echo Mode for Ultrasonic Beams|echo mode]]**", more on that later.
> - This is a [[SaM - Coarse Approximation of the Lumped Parameter Model of an Ultrasonic Transducer|coarse approximation]], since $\lambda_{w} \ngtr h$.
> - We don't have a sismic mass, what we are moving is the crystal, so now the mass $m$ is **quite small**, **it's only the mass of the crystal slice**.

> Here we can see the structure for when the ultrasonic transducers is used as an **actuator**.<br>So with $R_s$ **connected**, and both diodes **ON**:<br>![[Pasted image 20230719131247 1.png|500]]
> - The piezoelectric crystall, or more specifically the *USTX* is modelled as a capacitance $(C_E)$ and a **charge generator** $(Q_p)$, also an impedance $(R_A)$. #NOT_SURE_ABOUT_THIS 
> - In more details we have seen the [[SaM - Quartz Oscillator|quartz oscillator]].

> $\dot x(t)$ will have this simple form:<br>![[Pasted image 20231214122558.png|333]]
> The formula is:$$\dot x(t) = A \kern2px x_0 \kern2px e^{-\zeta \omega_0 t} \kern2px \cos\left( \omega_0 \sqrt{1-\zeta^2}\cdot  t+\varphi \right)$$And here if we plot $\left|{\dot x(\omega) \over V}\right|$:<br>![[Pasted image 20230925112924.png|500]]
> - The width of the peak is related to the value of the $\zeta$, the smaller is $\zeta$, the smaller is this peak.<br>And if we have a large $\zeta$ ⇒ we'll have a large bandwitht, ==ultrasonic transducers are considered **wide band devices**==.
> - A large $\zeta$ also means a short transient.

> Here's instead when it is used as a **sensor**.<br>So with $R_s$ **disconnected**, and both diodes **OFF**:<br>![[Pasted image 20230719131256.png|500]]
> The output of the transducer used as a sensor is a **charge**: #IMPORTANTE $$Q_p = k \kern2px d \kern2px x$$Where:
> - $d$ is the [[SaM - Piezoelectric Effect in Details • Direct and Inverse Piezoelectric Effect|piezoelectric coefficient]].
> - $k$ is the elastic constant of the material.
> - $x$ is the measured quantity, measured in $[\text{m}]$.
> 
> The transfer function will be: $${V \over F_{ext}} = {R_p \kern2px d \over 1 + j \omega R_p C_p} \kern2px H_u(\omega)$$Where:
> - $R_p = R_A \parallel R_i$
> - $C_p = C_E \parallel C_i$
> - $Z_i = R_i + C_i$ (impedance of the amplifier, usually a [[SaM - Charge Amplifier|charge amplifier]]).
> - $C_E = {\large{\varepsilon A \over h}}$ found [[SaM - Complete Piezoelectric Device (Actuator + Sensor)|previously]].
> - $R_A \sim \text{G}\ohm$ found [[SaM - Complete Piezoelectric Device (Actuator + Sensor)|previously]].
> - And $H_u$ is the mechanical response:$$H_u(\omega) = \frac{s}{\frac{m}{K}s^2 + \frac{\lambda}{K}s + 1}$$If we plot ${R_p \kern2px d \over 1 + j \omega R_p C_p}$ and $H_u(\omega)$:<br>![[Pasted image 20230719131324 1.png|500]]
> - ***NOTE***: It has the same equivalent circuit as the [[SaM - Piezoelectric Accelerometer|piezoelectric accelerometer]], however the final graph (and formula) is different, in this case we use $H_u(s)$, while for the **accelerometer** we used $H(s)$, why?. #NOT_SURE_ABOUT_THIS 
> - Then $\left|{V \over F_{ext}}\right|$ is the multiplication between the two.
> - I write better:
> 	- $\omega_N = \omega_0 \sqrt{1-2 \zeta^2}$
> 	- ${1 \over R_p C_p} \gg \omega_N$
> 	- ***Remember***: to find $\omega_0$ and $\zeta$ we need to transform $H_u$ in its [[SaM - Second Order System (OLD)|Bode form]], and then we have: $\omega = \sqrt{1 \over a_2}$ and $\zeta = {a_1 \over 2 \sqrt{a_2}}$.<br>In this case we have that: $\omega_0 = \sqrt{K\over m}$ (like many other times) and $\zeta = {\ldots}$ (*NOT IMPORTANT*).
> - $\frac{1}{R_p C_p}$ is defiend by the [[SaM - Charge Amplifier|amplifier]], and if it is designed well (so $\frac{1}{R_p C_p} \gg \omega_N$) it will not distort the sensed value, it will only amplify it.
> - **NOTE**: That the external force is given by the bouncing wave created by the crsytal (in case of **echo-mode**)
> - ==So it is a resonant device in any case, which needs to be excited at the frequency close to its **[[SaM - AT-Cut Quartz|natural resonance]]**==.

> - An ultrasonic transducer device can be used in **echo-mode**, first we send a signal by using the device as an actuator: we induce the crystal to vibrate with an **AC** exitation, and then we use the same device as a sensor, to sense the bounginc waves.
> - In any case, if we don't operate in **echo-mode**, so we transmit a wave with a device and we receive the wave with another device, it is important to match the two devices.<br>==*They must have the same resonant frequency in order to be able to use them together*==.

---
###### Memory Card
![[Samsung_SaM_Notes_14_240516_113346_2.jpg]]
![[Samsung_SaM_Notes_14_240516_113346_3.jpg]]

---
![[Pasted image 20230719131157.png]]
- Ultrasonic transducers are intended for generating and receiving **ultrasonic waves**.<br>Ultrasonic waves are **pressure waves in fluid** or **stress/strain waves in solid**, which can propagate through solids, **can be reflected by obstacles** and go back to the transducer to be received.
- So ==this kind of device is actually both an **actuator** and a **sensor**==.
- And mainly this kind of transducer are used in **echo mode**, (we'll see more detail later) in order to sense the generation from distant targets
- The applications of ultrasonic transducer are mainly in **biomedical fields**.<br>And in this case, we consider the wave to propagate in a liquid, because *human tissues can be seen as mainly as liquids*.
- They can also be used to measur distances, obviously non-contact, and in this case, usually it's in air.<br>so mainly they are used in in **air** or **liquid**.
- Finally, there is also an application in the so-called **non-destructive testing** or **non-destructive evaluation**, and in this case, the waves propagated in **solid** media.
- **NOTE**: this device also has a backing/dumper, this will increase the value of the dumping coefficient $\lambda$ as we will see in the lamped parameter system.


So the ultrasonic transducer structure is similar to the one of an accelerometer, but there is a difference, which is this:
- We have the crystal, the **piezoelectric** crystal, which is induced to vibrate, for instance, from an external generator.
- By vibrating, the surface vibrates and generates a wave, which propagates in a medium.
- If the wave founds a target, the wave is reflected.
- The reflected wave goes back to the surface, it exert stress over the surface, a pressure in the liqui, so it induces a new vibration, an **echo** if you will.
- Now the same crystal is used as a sensor, and is able to detect the **echo**, by detecting/sensing a vibration on the surface and translating this vibration into an electrical signal (like how we have seen before).

The difference with respect to an accelerometer is that in this case, we don't have any seismic mass. 

If we go to the mechanical equivalent circuit:
![[Pasted image 20230925111259.png]]
- We have the same $1 \over K$, which represents the **elastic behavior**.
- The damper $\lambda$ is larger because there is this added element.
- Whereas the sensor mass, I cancel this pedix $_S$ (previously seen when talking about the seismic mass $m_S$), because we don't have a sismic mass.<br>Also now the mass $m$ is **quite small**, **it's only the mass of the crystal slice**.
- This kind of devices has to operate at larger frequency, with respect to piezoelectric accelerometer.
- The transient of this mechanical device is shorter, ==larger $\lambda$ means shorter transient==.<br>Therefore, if this generator gets, for instance, a pulse, a shock, a delta function, then the transient response will be a short pulse and not a long one.
- This is really a *coarse approximation*.<br>So we will use it, but take into account the results we find, which can give us an idea of what happens, are **largely inaccurate**.<br>Since in this case (usually) we don't have that the **wavelength** of the mechanical wave ($\lambda$, unforntunately has the same letter as the dumping coefficient), so the displacement field is NOT larger than the **dimension of the crystal** ($h$).<br>So $\lambda \ngtr h$ ⇒ ***coarse approximation***.

So if this is $V_G$, then we expect a mechanical output, which is something like this, with a short duration:
![[Pasted image 20230925111343.png]]
- So usually they are, let's say, **wide band devices**.

Another thing is the name "*ultrasonic*" means that we are operating at frequencies within in general are higher than the frequency of the sound.<br>This is the reason why we speak about high frequency vibrations and high frequency devices.

We have seen that it can both generate and receive:
![[Pasted image 20230719131223.png]]
- The *USTX* is the **UltraSonic Transducer**, actually this part reperesents the crytsal, which we have just modelled. #NOT_SURE_ABOUT_THIS 
- Around the reciver there is a **protection circuit**, which protects the amplifier when using the device as a transducer.
- Note the switch after $R_s$, when it is closed the sensor is used as an actuator, while when it is opened it is used as a sensor, and its output gets amplified by the amplifier.
- The two diodes cap the frequency that passes to the amplifier at around $\pm 600$ **mV** (this votlage is defined by the diodes).<br>They are used to keep this input to a voltage lower than beyond voltage of the diode.<br>==$V_i$ is "protected" by the diodes==.

I can find the vibration of the surface as a function of the voltage, which also depends on the frequency (as always):
![[Pasted image 20230719131247.png]]
-  Lastly we simulate what happens with a pulse or step input (so $u(t) = \mathbb{1}(t)$)

If we plot it:
![[Pasted image 20230925112924.png]]
- The width of the peak is related to the value of the $\zeta$, the smaller is $\zeta$, the smaller is this peak.<br>And if we have a large $\zeta$ ⇒ therefore we have large bandit.

==After having finished this generating part, then the same device can be used as a sensor.==<br>Therefore now this switch here is disconnected, and we have:
![[Pasted image 20230719131256.png]]
- As always $F_p$ can be regarded because usually this $F_{ext}$ is larger but in any case it will be here, no matters.
- The two diodes are now off (open) because the signal now is very small, (it is the received signal), so we can neglect their existence.

Some calculations:
![[Pasted image 20230719131312.png]]
- We have used some different terms from before: $R_i = R_f$ and $C_i \sim C_f + C_C$ #NOT_SURE_ABOUT_THIS 


So we can go back here and call this function "ultrasound in frequency domain": $H_u(\omega)$, so: $$H_u(\omega) = \frac{s}{\frac{m}{K}s^2 + \frac{\lambda}{K}s + 1}$$If we plot it:
![[Pasted image 20230719131324.png]]
- Here we have two plots, the one is the $H_u$ plot and the other the $V \over F_{ext}$ plotted for $H_u = 1$, the complete plot is the multiplication of the two.
- The $H_u$ is the mechanical response.
- While $\left.{V \over F_{ext}}\right|_{H_u=1}$ is the electronic response.
- $\frac{1}{R_p C_p}$ is the cutoff frequency of the (ideal) amplifier, and if it is designed well (so $\gg \omega_N$) is will not distort the sensed value, it will only amplify it, (for frequency in which the device can be used around $\omega_N$)
- The overall transfer function is resonant because of the large value of the damping.


We need that spectrum of external force to be in this range here in order to have a good response.
**NOTE**: That the external force is given by the bouncing wave created by the crsytal (in case of **echo-mode**)
![[Pasted image 20230719131333.png]]
- ==So it's like a tuned device, a resonant device in any case, which needs to be excited at the frequency close to its **natural resonance**==.
- And in this case, we are analyzing which is the Echo-mode operation, whether the center is used both to excite the wave and to receive the wave.
- ==In any case, if we don't operate in echo-mode, so we transmit a wave with a device and we receive the wave with another device, it is important to match the two devices==.<br>==They must have the same resonant frequency in order to be able to use them together==.

---