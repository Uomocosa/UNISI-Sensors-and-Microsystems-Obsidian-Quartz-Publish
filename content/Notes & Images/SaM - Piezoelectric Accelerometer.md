##### ***Remeber***:

> The structure is the same, a simple sismic mass accelerometer with a spring dump system:<br>![[Pasted image 20230719130505.png|500]]
> - However ==the spring is made up of quartz==, or more generarly of a **piezoelectric layer**.
> - The two surfaces above and below the piezoelectric layer, are covered by a **conductive layer**, each surface is connected to a wire and this two wires are brought out of the case.<br>This way like for all piezoelectric sensor we have created a capacitance, from which we can measure the stored charge, usually by using a [[SaM - Charge Amplifier|charge amplifier]].
> - The mass of the crystal usually can be neglected, and ==the mass of this primary sensor coincides with the seismic mass==.

> - Here's the equivalent circuit:<br>![[Pasted image 20230924180117 1.png|500]]
> - We can neglect $F_p$, since this force is usually so small, very small with respect to $F$ (the external force).

> ***Output formula***:$$V(s) = {R_T \kern2px k \kern2px d \kern2px s \over 1 + s \kern1px R_T C_T}\cdot H(s)\cdot a(s)$$Where:
> - $\omega_n$ : natural frequency $\left(\omega_n \simeq \omega_0 = \sqrt{k \over m_s}\right)$
> 	- $k$ is the spring consntant of our accelerometer, and $m_s$ the sismic mass.
> - $C_T = C_E + C_L$
> - $R_T = R_L \parallel R_A \approx R_L$
> - ==$C_L$ and $R_L$ depend on the **wire's lenght** (bad)==.
> - $a(s)$ : laplace transform of the acceleration $a(t)$.
> - $H(s)$ : [[SaM - Accelerometer|accelerometer's transient function]] $\left(H(s) = {\huge\frac{m_{\tiny{S}}}{k} \frac{1}{{m_{\tiny{S}} \over k}s^2 + {\lambda \over k}s + 1}}\right)$

> - Here is the bode plot of the overall function:<br>![[Pasted image 20230719130657.png|500]]
> - If we measure at the right frequency, inside the measurement frequency range, mening, if we take:$$f \in \left[{10 \over R_T C_T} \div {\omega_n\over 10}\right]$$Where:
> 	- $\omega_n \simeq \sqrt{k \over m_s}$
> 		- $k$ is the spring consntant of our accelerometer, and $m_s$ the sismic mass.
> 	- $C_T = C_E + C_L$
> 	- $R_T = R_L \parallel R_A \approx R_L$
> 	- ==$C_L$ and $R_L$ depend on the **wire's lenght** (bad)==.
> - Then we will have a linear sensor, since the response has an approximately constant magnitude, so the output will be:$$\alpha = {V(\omega) \over a(\omega)} = {m_s \cdot d \over C_T}$$
> - So we will have a constant [[SaM - Sensitivity|sensitivity]].

> Let's list some "pecularities" of this accelerometer:
> - The overall system is [[SaM - AC-Coupled Amplifier|AC-coupled]]. ⇒ ==You cannot sense **static** acelerations==.
> - The lower cutoff frequency:$$f_L = {1 \over 2 \pi C_T R_L}$$ comes from the electric part here: $1 \over R_T C_T$, and you see that it depends on the total parallel resistance and the total capacitance.<br>⇒ ==Therefore, if the cable used to connect the device to the front end varies/changes, then also this frequency here will change==.<br>**NOTE**: we have said before that the lower cutoff frequency was $f_L = {10 \over C_T R_L}$ and i belive it to be more accurate. #NOT_SURE_ABOUT_THIS <br>**NOTE**: probably the professor got confused with the [[SaM - Charge Amplifier|charge amplifier lower frequency limit]]. #NOT_SURE_ABOUT_THIS 
> - And what is more severe, worst problem, is that also ==the sensitivity depends on this capacitance $C_T$==:$$\alpha = {m_s \cdot d \over C_T}$$

> To solve the "dependecy from the cable" problem we can make the amplifier (read-out electronics) a part of the sensor itself, this particular kind of piezo-accelerometer are called **IEPE** or **ICP**:<br>![[Pasted image 20230719130803.png|500]]
> - So in this case, $C_T$ is fixed. ⇒ Problem Solved.

> Also look at [[SaM - Charge Output Accelerometer|charge output accelerometer]]

---
###### Memory Card
![[Samsung_SaM_Notes_14_240516_113346_2.jpg]]

---
![[Pasted image 20230719130505.png]]
- The structure is the same, a simple sismic mass accelerometer with a spring dump system.
- However ==the spring is made up of quartz==, let's say it's a **piezoelectric layer**.
- As usual this two surfaces (**above and below the piezoelectric layer**) are covered by a **conductive layer**, each surface is connected to a wire and this two wires are brought out of the case.
- Above all this there is a seismic mass case, which can be made of steel, for instance.
- Therefore, the mass of the crystal usually can be neglected, and ==the mass of this primary sensor coincides with the seismic mass==.

Here is the structure of a real life piezoelectric accelerometer.
![[Pasted image 20230719130511.png]]

Now, we can draw the equivalent circuit:
![[Pasted image 20230719130534.png]]
![[Pasted image 20230924180117.png]]
- For the mechanical part, is the same as usual.
- For the electronic part instead is similar to what we have seen before, for piezoelectric sensor, but in this case we have also $R_L$ and $C_L$, this represent the input of an amplifier ($R_L$, really large) and the parasitic capacity of the cable ($C_L$, really small).<br>Also remember that $R_A$ is also very large.
- Before going on, I remember that we can neglect $F_p$, since this force is usually so small, very small with respect to $F$ (the external force).

So now we are, first of all, finding $\dot x$, as we have already seen many times:
![[Pasted image 20230719130609.png]]
- $G$ is unused and $C_C$ did not exist previously, maybe it refers to $C_L$, and the formula should be: $C_T = C_E \parallel C_L$ #NOT_SURE_ABOUT_THIS 

Now we can write $V$:
![[Pasted image 20230719130620.png]]
- $\omega_n \simeq \omega_0$ : **natural frequency** or **resonating frequency**.


We can draw the input-output relationship module in the frequency domain:
![[Pasted image 20230719130633.png]]
- In black the mechanical function we have seen before $H(s)$
- In blue the response of the electrical system, so the output voltage dived the acceleration, however we still need to multiply it by $H(s)$<br>**NOTE**: In the drawing the colors are inverted #NOT_SURE_ABOUT_THIS 
- $1 \over R_T C_T$ is a pole.


The overall function is:
![[Pasted image 20230719130657.png]]
- So if we measure at the right frequency (inside the measurement frequency range) we will have a linear sensor, since the response has an approximately constant magnitude.

So we'll also have a constant sensitivity.
![[Pasted image 20230719130716.png]]
- We see that this kind of sensor and frontend, so the overall system is [[SaM - AC-Coupled Amplifier|AC-coupled]].<br> ⇒ You cannot sense static acelerations.
- So this device **can be used only for dynamic acceleration measurements**, that is for **vibrations measurement**.
- The low frequency cutoff comes from the electric part here  $1 \over R_T C_T$, and you see that it depends on the total parallel resistance and the total capacitance.<br>⇒ Therefore, if the cable used to connect the device to the front end varies/changes, then also this frequency here will change.
- And what is more severe, worst problem, is that also ==the sensitivity depends on this capacitance $C_T$==.


So:
![[Pasted image 20230719130728.png]]
![[Pasted image 20230719130740.png]]
- So **sensor voltage output measurement** (which is crucial for readable outputs) can be performed only if the front end electronic, which is a voltage amplifier, is placed inside the case or connected with **fixed wiring**.
- And we speak about **IEPE or ICP piezo-accelerometer**, which are:

**IEPE or ICP piezo-accelerometer**
![[Pasted image 20230719130803.png]]
- The voltage amplifier becomes a part of the sensor itself.
- So in this case, $C_T$ is fixed. ⇒ Problem Solved.
- These two output wires are needed both for power in the amplifier and also for reading the output.<br>Since the output is an **AC**, you can exploit the same two wires, because the power supply needed by the amplifier is a **DC value**, whereas the output of the sensor is an **AC value**, so you can filter and use the same wires to give both
- Sometimes you can use devices where the front end is integrated into the case of the sensor, and in this case the ouptut wires are directly connected to the crystal, so what we have as output is a **charge**.

