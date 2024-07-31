##### ***Remeber***:

> If we take a simple circuit which contains:<br>![[Pasted image 20230718200937 1.png]]
>  - $V_R$ : reference voltage.
>  - $C_R$: reference capacitance.<br>In other cases you can have no reference capacitance, for instance if you measure **humidity**.
>  - $C_S$: sensor.
>  - $C_{CABLE}$: in case of a long cable, i need to consider it.
>  - $C_{COUP}$: parasitic capacitance with external electric potential $V_d$.<br>This $V_d$ could be for instance another appliance, or a person which moves.
>  - $R_{in}$: input resistance to front-end electroncis.
>  - $C_{P}$: parasitic capacitance (from the front-end electronics).
>  - We can consider:
> 	 - $C_P' = C_{\text{CABLE}} \parallel C_P$
> 	 - $C_{\text{TH}} = C_R \parallel C_S$
> Then $V_{in}$ across $R_{in}$, will be equal to:$$V_R \kern2px {j\omega R_{in}C_{\text{COUP}} \over 1 +j \omega R_{in} (C_{\text{COUP}} + C_{TH} + C_P')}$$

> So we have a bode plot like this:<br>![[Pasted image 20230718201005 1.png]]
> - Also at low frequency, meaning: $f \ll f_p$, we can approximate as:$$\frac{V_i}{V_d} \simeq j \omega R_{in} C_{COUP}$$Especially in this case, if this resistance $R_{in}$ is small, the sensitivity of the circuit to electrical noise becomes smaller (a good thing).<br>⇒ ==So it's better, if possible, to use a front end amplifier with **low resistance**==.<br>⇒ Meaning, that it's better to use [[SaM - Current Amplifier|current]], or [[SaM - Charge Amplifier|charge amplifiers]], so that we have the $R_{in}$ [[SaM - Current Amplifier|resistance very low]], resulting in a cutoff frequency $f_p$ very very high.
> - However in this case we cannot choose a small input resistance, since if I put the $R_{in}$ resistance at $0$, **I don't read anything** $\left(\frac{V_i}{V_d} = 0\right)$.
> - ==Still, remember that when dealing with high source measurements, the better frontend is a low input impedance amplifier==.
> - ==Another thing to underline is that it would be better to have the $f_p$ cutoff frequency much larger than $50 \kern2px \text{Hz}$==.<br>*Why?*<br>==Because one of **the most important source of electrical noise is the power line wiring**, that we have everywhere, and the power lines generate noise at $50 \kern2px \text{Hz}$==. 

---
###### Memory Card
![[Samsung_SaM_Notes_21_240516_160358_6.jpg]]

---
##### Electrical Noise
![[Pasted image 20230718200937.png]]
- Where:
	- $V_R$ : reference voltage.
	- $C_R$: reference capacitance.<br>In other cases you can have no reference capacitance, for instance if you measure **humidity**.
	- $C_S$: sensor.
	- $C_{CABLE}$: in case of a long cable, i need to consider it.
	- $C_{P}$: parasitic capacitance.
	- $C_{COUP}$: parasitic capacitance with external electric potential $V_d$.<br>This $V_d$ could be for instance another appliance, or a person which moves.
	- $R_{in}$: input resistance to front-end electroncis

I can group some capacitances:
![[Pasted image 20230718200946.png]]

So at this point I can represent everything with its Thevenin equivalent:
![[Pasted image 20230718200955.png]]
- So I would like to understand what happens to this input voltage when there is no signal, so $V_{TH}$ is shorted and the only source present is the disturbance.<br>I want to see how the input varies due to the disturbance, and not to the signal itself.

Let's draw the frequency domain, what happens here:
![[Pasted image 20230718201005.png]]
- You have a zero in zero.
- You have a pole in $f_p$
- And what happens here, you see that the best thing is to work at **low frequency**, because at this frequencies the electric noise, (which is due to the electric cable coupling of my circuit with electrical environment) is ==**off-band**: so it's cut from the high pass behavior of the disturbance coupling==<br>⇒ This means:
	- We want a low value for noise and disturbances, at high frequency we have the maximum value which is:$$\frac{V_i}{V_d} \simeq \frac{C_{COUP}}{C_{COUP}+C_{TH}+C_P'}$$So we decide to stay in **low fraquency**.
- We have that: $$f_p = \frac{1}{2\pi R_{in}(C_{COUP}+C_{TH}+C_P')}$$So the frequency $f_p$ is higher if $R_{in}$ is smaller.
- Also at low frequency, meaning: $f \ll f_p$, we can approximate as:$$\frac{V_i}{V_d} \simeq j \omega R_{in} C_{COUP}$$Especially in this case, if this resistance $R_{in}$ is small, the sensitivity of the circuit to electrical noise becomes smaller (a good thing).<br>⇒ ==So it's better, if possible, to use a front end amplifier with **low resistance**==. 

So if possible, it's better to use current, or charge amplifiers, so that we have the $R_{in}$ resistance very low, resulting in a cutoff frequency $f_p$ very very high. 
![[Pasted image 20230718201012.png]]

But **In this case, it is not possible**. 
*Why?*
Let's look at our starting excitation circuit:
![[Pasted image 20230718201018.png]]
- We find that if I put the $R_{in}$ resistance at $0$, **I don't read anything**, because I put a short circuit parallel to my capacitance.<br>So in this case, it's not viable and we have to do something different.
- ==Still, remember that when dealing with high source measurements, the better frontend is a low input impedance amplifier==.

==Another thing to underline is that it would be better to have the $f_p$ cutoff frequency much larger than $50 \kern2px \text{Hz}$==.
*Why?*
==Because one of **the most important source of electrical noise is the power line wiring**, that we have everywhere, and the power lines generate noise at $50 \kern2px \text{Hz}$==. 
And this is the reason why when this frequency here is very low, we'll have many problems of electrical coupling. 
