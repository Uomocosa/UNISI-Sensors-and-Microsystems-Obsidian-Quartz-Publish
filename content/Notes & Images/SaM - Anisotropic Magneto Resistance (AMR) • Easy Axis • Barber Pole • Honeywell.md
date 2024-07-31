##### ***Remeber***:

> ==The *Anisotropic Magneto-Resistance* (***AMR***) is a phenomenon in which the **electrical resistance** of a material depends on the direction of an applied magnetic field==:<br>![[Pasted image 20230718195930 1.png]]
> - It is usally present in ferromagnetic materials.
> - We have seen some example of materials that present AMR, like: *Ni*, *Fe* and *Permalloy* ($80\%$ *Fe* + $20\%$ *Ni*) #IMPORTANTE 
> - The formula that governs the AMR is:$$\rho(\theta) = \rho_{\parallel} - \Delta_{\rho} \sin^2\theta $$Where:
> 	- $\Delta \rho = \rho_{\parallel} -\rho_{\perp}$
> 	- $\rho_{\parallel}$ is the resisitivity when $\theta = 0°$.
> 	- $\rho_{\perp}$ is the resisitivity when $\theta = 90°$.
> 	- $\theta$ is the angle formed by $\vec J$ and $\vec M$, where:
> 		- $\vec J = {\vec I \over A}$ is the **electric current density vector**.
> 		- $\vec M$ is the total magnetization vector, accounting for the external magnetic filed $\vec H_{\text{ext}}$, and for the [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetization of the material]] $\vec M_r$.

> We need to define an **easy axis**, which will in the same direction of $\vec M_r$ (the [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetization of the material]]):<br>![[Pasted image 20230718195937.png]]
> If we have that $\vec H_{\text{ext}} \ll H_S$ than we can approximate:$$\sin \theta = {H_y \over H_S}$$Where:
> - $\vec H_{ext} = \kern2px <H_x,\ H_y>$
> - $H_S$ is the **saturation field**, it is a property of the material.

> We usually use thin films of material for AMR #NOT_SURE_ABOUT_THIS (Why?)
> 
> So if we calculate the AMR formula using the approximation found for $\vec H_{\text{ext}} \ll H_S$, we find that:$$\rho \simeq\rho_{\parallel} - \Delta \rho \left({H_y \over H_S}\right)^2$$Which is still **non-linear**.
> If we wish, we could transform the formula into resistance, instead of resisitivity:$$R = R_0 \left(1- \frac{\Delta R}{R_0}\left(\frac{H_y}{H_S}\right)^2\right)$$In this case remember that:
> - $\Delta R = \Delta \rho {l \over S}$ 
> - Where: $\Delta \rho = \rho_{\parallel} - \rho_{\perp}$.
> 
> If we plot the graph of $\rho(\theta)$ given $\theta$:<br>![[Pasted image 20230718200022.png|500]]
> We notice that for $\theta \sim 45°$ we have an almost linear graph.
> So we can linearize our passive sensor in 3 ways:
> 1. By adding an external "**biasing field**".<br>So we operate as to fix the opearitional range around the 45° point, by injecting a field.
> 2. We **rotate the current with respect to the easy axis**. (most used)
> 3. `Not discussed`

> Let's see how we can **rotate the current**:
> We can create a "barber pole" using two different conductors (for example a "*Permalloy*" and  *Metal*) and we bond them with this structure:<br>![[Pasted image 20230718200035 - Copia 1.png]]
> - This way the current (since it finds the path that minimizes $R$) will be "tilted" by 45° with respect to the easy axis.
> - We can mount $4$ barber pole like a [[SaM - Full Bridge|resistive bridge]] to form a "***Honeywell***", more on that later.
> - This way we will have a linear behaviour defined like so:$$R(H) = R_0 \mp \Delta R {H_y\over H_S} \kern2px \sqrt{1-\left({H_y\over H_S}\right)^2}$$Where: $\sqrt{1-\left({H_y\over H_S}\right)^2} \approx 1$, so we can say that:$$R(H) \approx R_0 \mp \Delta R \kern2px {H_y\over H_S}$$Remember this is still under the hypothesis that $H_{\text{ext}} \ll H_S$.<br>We can also stress that obviously if here I have put a "$\mp$", and the reason is that this minus or plus depends on the easy access direction.

> If we apply a **large** magnetic field to a barber pole, ==it could change the sensitivity, and also the sign of the sensitivity of the device==, this is know as "***Flipping Effect***" (or "***Hysteresis***" #NOT_SURE_ABOUT_THIS )
> To solve this problem we can apply a reverse and stronger external field.
> 
> Obviously since this is a magnetic material, we have the most important problem of **hysteresis**. That means that ==under the application of a high enough external magnetic field, the original magnetization can change==.  #NOT_SURE_ABOUT_THIS (It is the same problem as the flipping effect, it just changes name)

> #IMPORTANTE 
> - ==This sensor works properly for **weak external field**==. 
> - The **sensitivity** is large for these devices and also the **frequency range** can be large as well. 
> - The **temperature** span is approximately $[-50°C ,\ 200°C]$, so it is very large.

> Applications for Magnetoresistances:<br>![[Pasted image 20230718200112 1.png|500]]

> If we mount $4$ **Barber pole** in a single package we can create a [[SaM - Full Bridge|full bridge]]:![[Pasted image 20230718200128 1.png|300]]
> The final formula for this strucutre is: #NOT_SURE_ABOUT_THIS $$V_{\text{TH}} = \alpha_r \cdot V$$Where:
> - $V_{\text{TH}} = V_+ - V_-$ is the output. #NOT_SURE_ABOUT_THIS 
> - $\alpha_r$ is the [[SaM - Sensitivity|relative sensitivity]], and for this structures it is usually $10^{-3}$.
> - $V$ is the input voltage.
> 
> We can also calculate the relative sensitivity as: #NOT_SURE_ABOUT_THIS $$\alpha_r = {\Delta R \over R_0}\kern2px {H_y \over H_S}$$Remember that: $\Delta R = \left(\rho_{\parallel} - \rho_{\perp}\right) \cdot {l \over S}$

 > We can also pack more honeywell in a single chip or package to create magnetoresistor that measures magnetic fields in more than one dimension, for example:<br>![[Pasted image 20230718200136.png]]
 > 
 > There are also other kind of devices, similar to this one, which are made to operate with larger fields, like **magnetic position sensors***:<br>![[Pasted image 20230718200155.png|500]]
 > Here we have that we can measure the angle $\theta$ of the magnetic field as:$$\tan \left(2 \kern1px \theta \right) = {V_{\text{THA}} \over V_{\text{THB}}}$$Where:
> - $A$ refers to the bridge sensing along the $x$ axis.
> - $B$ refers to the bridge sensing along the $y$ axis.
 > 

---
###### Memory Card
![[Samsung_SaM_Notes_08_240515_123317_3.jpg]]

---
# Index
- [[#Anisotropic Magnetorestance]]
- [[#Thin Film Geometry Variation]]
- [[#Linearization of a Magnetoresistive Sensor]]
- [[#Flipping Effect]]
- [[#Conclusion on Magnetoresistive Sensors]]
- [[#Applications for Magnetoresistances and Hysterisis Problem]]
- [[#Honeywell]]
---
##### Anisotropic Magnetorestance
![[Pasted image 20230718195930.png]]
- These devices are ==used for measurement of the magnetic field of the earth, so for compasses==. 
- ==Usually they are based on the **AMR** (*Anisotropic Magneto Resisitivity*)==.
- We find for this kind of materials, that the scattering of electrons, therefore the **mobility** ($\mu$) and **resistivity** ($\rho$) depends on the vector $M$, which is the **magnetization** or the **magnetic moment**.
- In general for this material, we find that if I have the certain direction for the vector $\vec M$, and $\vec J$ (**current density vector**) ⇒ the resisitivity $\rho(\theta)$, is related to this angle $\theta$ by this equation:$$\rho(\theta) = \rho_{\parallel} - (\rho_{\parallel} - \rho_{\perp}) \sin^2\theta = \rho_{\parallel} - \Delta\rho\sin^2\theta$$

![[Pasted image 20230718195937.png]]
- $\vec M_r$ or $\vec M_0$ when there in't any applied external magnetic field ⇒ so I think of a permanent magnet. 
- First of all, we call the direction of this permanent magnetization "**easy axis**", so i take as reference ($x$) this easy axis.
- if I apply an external magnetic field, then the overall magnetic moment will rotate (by an angle $\varphi$).
- $\vec H_{ext} = \kern2px <H_x,\ H_y>$
- $H_x$: This is the magnetic field component in the horizontal ($x$) direction.
- $H_y$: This is the magnetic field component in the vertical ($y$) direction.
- $Hs$ is a property of the material, and it is called **saturation field**. 
- ***What is the Saturation Field?*** (ChatGPT)
	- The saturation field, also known as the saturation magnetization or saturation magnetic field, is a characteristic property of a ferromagnetic material. <br>It represents the strength of an applied external magnetic field at which the material becomes fully magnetized. <br>==In other words, it's the point at which the magnetic domains within the material are aligned in the direction of the applied field, and further increases in the field strength do not result in additional magnetization==.

![[Pasted image 20230718195950.png]]
- $H_y$: This is the magnetic field component in the vertical ($y$) direction.
- $Hs$ is a property of the material, and it is called **saturation field**. 

Simarly we have said that:
![[Pasted image 20230927183813.png]]

---
##### Thin Film Geometry Variation 
![[Pasted image 20230718200011.png]]
- So the resistance of the thin film changes like so:$$R = R_0 \left(1- \frac{\Delta R}{R_0}\left(\frac{H_y}{H_S}\right)^2\right)$$
	- In this case remember that $\Delta R = \Delta \rho {l \over S}$ where $\Delta \rho = \rho_{\parallel} - \rho_{\perp}$.

Graph of how the fucntion $\rho(\theta)$ changes with $\theta$.
![[Pasted image 20230718200022.png]]

---
##### Linearization of a Magnetoresistive Sensor

So there is a linearization of the sensor.
And this can be done in 3 ways:
1. By adding an external "**biasing field**".<br>So we operate as to fix the opearitional range around the 45° point, by injecting a field.
2. We **rotate the current with respect to the easy axis**. (most used)
3. `Not discussed`


***Biasing Field***:<br>![[Pasted image 20230718200035.png]]
- $H_B$ : external "biasing" field.

***Rotate the current***:
![[Pasted image 20230718200035 - Copia.png]]
- Usually we do something different, we **rotate the current with respect to the easy axis**. <br>And this rotaion has to be close to 45°.<br>And this can be done in 2 way:
	1. Magnetize the the film material with a different angle with respect of its axis. So $\vec M_r$ is rotated by applying a very strong field during the position for instance. 
	2. But the best solution and the one which is commonly used, is to build a thin film resistance which presents a special structure which is called "**barber pole**".<br>So this is the thin film, and what happens is that actually the film is made of different domains:<br>So these strips here represents different materials:<br>$\huge{\huge {\cdot}}$ Black should be metal metal like gold, so large conductivity.<br>$\huge{\huge {\cdot}}$ This is the permalloy for instance.<br>$\huge{\huge {\cdot}}$ The angle should be 45°.<br>⇒ So If we introduce a metal target, and a permalloy, in this disposition, we have that the current (indicated by current density $\vec J$) will "travel in a $45°$ angle" as show in the picture, that is due to the fact that "current finds the path which minimizes $R$".

So we have a linear behavior:<br>![[Pasted image 20230718200041.png]]
- And this is true under certain hypothesis for instance, the field $\vec H_{\text{ext}}$ (especially the $y$ component $H_y$) has to be not so large compared to the saturation $H_S$.<br>⇒ So the range is limited by the material characteristics. 
- And we can also stress that obviously if here I have put a "$\pm$", and the reason is that this minus or plus depends on the easy access direction.


---
##### Flipping Effect
The application of large external field can affect the behavior of a **Barber Pole**, it can change the sensitivity, and also the sign of the sensitivity of the device. 
This phenomenon here which occurs under strong external fields is called the **flipping effect**.
Sometimes the magnetization can be reset, so ==the flipping effect can be solved by applying a reverse and stronger external field==. 

---
##### Conclusion on Magnetoresistive Sensors
- ==This sensor works properly for **weak external field**==. 
- The **sensitivity** is large for these devices and also the **frequency range** can be large as well. 
- The **temperature** span is approximately $[-50°C ,\ 200°C]$, so it is very large.<br>![[Pasted image 20230718200104 - Copia.png]]

---
##### Applications for Magnetoresistances and Hysterisis Problem
![[Pasted image 20230718200112.png]]
- Obviously since this is a magnetic material, we have the most important problem of **hysteresis**. 
- That means that ==under the application of a high enough external magnetic field, the original magnetization can change==. 

---
##### Honeywell
To conclude, let's see the devices which exist based on these kind of sensors here. And so I refer to some devices of the "***Honeywell***". 
![[Pasted image 20230718200128.png]]
- Where:
	- $S$ :  ??? #TODO 
	- $B$ : flux density, ember that actually we sense along the $y$ axis.
- Each resistence is formed by a **Barber Pole** strucure like we have seen before.
- This is magnetic sensitivity axis, which was $y$, $H_y$ is in this direction here:
- As we have said in theory: ==we are operating with weak magnetic fields==, and thanks to the barber poles which ==rotate the current at $45°$== <br>⇒ ==We can linearize everithing==.

To measure the magnetic field in more direction we can just mount more sensors on the same chip:
![[Pasted image 20230718200136.png]]
- One which sens along $y$, and the other which is mounted as to sense the $x$ component of the field. 

There are also other kind of devices, similar to this one, which are made to operate with larger fields:
![[Pasted image 20230718200155.png]]
- Where:
	- $A$ refers to the bridge sensing along the $x$ axis.
	- $B$ refers to the bridge sensing along the $y$ axis.
	- $S$ : sensitivy.<br>They have the same sensitivity, because they are the same devices only rotated.
- ==We stress the dependency on $\theta$ this time, because here is the **non-linearized version**==
- I write better the formula for $V_{THA}$:$$\frac{V_{THA}}{V} = S \cdot \sin(2\theta)$$
- At the end by evaluating the ratio of these two voltages we can find that it is actually the tangent of the angle $\theta$.
