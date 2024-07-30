##### ***Remeber***:

> ==This is more like a **detector** than a real sensor, because it usually doesn't show large [[SaM - Accuracy or Maximum Error|accuracy]], but it's a sensor which shows, instead, very high [[SaM - Sensitivity|sensitivity]], low **selectivity**==
> **Selectivity** in this case means: "_**which** chemichal compound we can detect_".

> The output is a resistance, which is a function of this concentration, so $R\left[C\right]$.
> $C$ : could be oxygen, it could be nitrogen dioxide, it could be carbon monoxide, ...

> The [[SaM - Sensitivity|sensitivity]]:$$\alpha = {dR \over d [C]}$$is **higly non-constant**, so this is a **non-linear** sensor.
> Also as we have said these are **non-selective** devices, in fact for $x$ a different compound than the one we want to measure, we have:$$\alpha_x = {dR \over d [x]} \neq 0$$A selective device would have $\alpha_x = 0$.

> This is an **active** sensor, so it requires power to operate, the power of the overall device can be calculated as:$$P_W = R_H \cdot I^2 = G \left(T_S - T_A\right)$$Where:
> - $P_W$ : power of the overall device.
> - $G = {1 \over R}$ : [[SaM - Recap of Basic Components • Resistance, Capacitance, Inductance • Resistivity, Permittivity, Permeability|conductance]].
> - $I$ is the current we feed it.
> - We can instead calculate the power as a formula of the temperature we need it to reach, se we measure $T_S$.<br>And usually the temperature range is relatively high: $T_S \in [150°\text{C},\ 450°\text{C}]$.
> - ==The reason why it is necessary to bring this resistive sensor to a very high temperature is because the chemical reaction are faster at this higher temperature, which are needed to get the variation of the resistance==. 

> A **chemical reisistive sensor** is made of:
> - **Thick film ceramic resistances**:
> 	- It is usually ceramic, ==so, it is **inert**==, meaning it doesn't interact with chemical compounds.
> 	- Its thickness is usually **around $100$ micrometers**, thats why we call it **thick film**.<br>For a **thin film** we mean having a thickness of **less than $10$ micrometers**.
> - **Two metal electrodes**.
> - **An active layer**:
> 	- It's the material which builds up the sensing device.<br>Usually, this film is not properly ceramic, because it's made up of many different grains, so like powder which stays together.
> 	- ==It has a lot of pores, so that gas can reach all the film in its whole thickness==.
> - **Thick film metal resisitance** (on the backside):
> 	- Acts as a heater (using the current we provide).

> Here's a scheme of the topside:<br>![[Pasted image 20230718200234 - Copia 1.png|500]]
> And backside:<br>![[Pasted image 20230718200255 1.png|500]]

> The principle of operation for this sensor here is based on **absorption**:
> We take only two grains from the thick film, the current has to pass through these two grains:<br>![[Pasted image 20230718200308 1.png|500]]
> On the surface of these grains here, the gas, which I want to sense, (let's consider oxygen for instance) is absorbed.
> After being absorbed on the surface, there is a transfer of charge from the sensor (from the metal oxide) to the gas, and vice versa.
> So for instance, oxygen tends to take an electron from the metal oxide, and it traps this electron, this negative charge, on the surface.
> Now I have a charged species on the surface, with a certain density, which I call $N_S$:<br>![[Pasted image 20230718200308 2.png|500]]
> 
> In these metal oxide semiconductors, there are **defects** which are naturally present which acts as dopants.<br>⇒ ==So at these temperature these intrinsic semiconductors **behave as extrinsic**==:<br>![[Pasted image 20230718200326 1.png|500]]
> Now that I have depleted the layer under the surface, meaning the layer has no electrons, since they have been taken by the absortment compound, which is oxygen in this case.<br>⇒ ==We have a plus charge region under the surface, like in a **diode**==.
> 
> So obviously you have a minus charged layer, a positive charged layer, so you have an **electrical field**, and associated with this electrical field, you have a **voltage barrier**, like this:<br>![[Pasted image 20230718200335 1.png]]
>  When you place two grains together and you want the current to flow through, at the surface of each grain there is the potential barrier.<br>⇒ ==So only the electrons which have enough energy to overcome this barrier can pass through to the next grain==, and so contribute to the overall current in the film.
>  ==This is like a diode==, and for this reason at the end, we can find the conductivity of the film:$$G = G_0 e^{-\huge\frac{q^2 N_S^2}{2\varepsilon K T_S N_D}}$$Where:
> - $q V_S$ : height of the potential barrier between each grain of the substrate.
> - $N_S$ : density of the absorbed and charged chemical compound.
> - $T_S$ : temperature of the sensor.
> - $N_D$ : [[SaM - Instrinsic Semiconductor • Density of Carriers • Energy Gap and Carriers Dependance on Temperature|density of donors]].
> - $k = 1.38\cdot 10^{-23} \ {\large{\text{J}\over\text{°K}}}$ : Boltzmann's constant.
> - $\varepsilon$ : [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|electric permittivity]] $(\varepsilon = \varepsilon_0 \varepsilon_r)$
> 	- $\varepsilon_0$ : electric permittivity of the void $\left(\varepsilon_0 = 8.85 \cdot 10^{-12} \ {\text{C}^2 \text{m}^2 \over \text{N}}\right)$
> 	- $\varepsilon_r$ : relative electric permittivity

> Note from this formula:$$G = G_0 e^{-\huge\frac{q^2 N_S^2}{2\varepsilon K T_S N_D}}$$The temperature of the sensor ($T_S$) has to be kept very, **very constant**, otherwise you have a reaction due to temperature which is of the same intensity as the reaction due to chemical compound concentration.

> ==The **Selectivity** of these devices is decided by the chemistry, some materials tend to absorb some gases, others instead other gases==. 
> So by selecting this specific type of material or the dopants put into the material, you can change which kind of gas is absorbed. 

> Also, ==these are sensors which are **not so reproducible**==. 
> The processes which happen at the surface are quite not so known. 
> The final equation gives only an **approximation** of what really happens, and it can be very different on the basis of different material and different microstructure of the field.<br>⇒ ==Read carefully the data-sheet==.

> ==One of the most important influence factor is the **humidity** which is the water vapor, always present in the environment==. 
> ==And also the **change of temperature** may really change the behavior of the sensor==. 

---
###### Memory Card
![[Samsung_SaM_Notes_10_240515_182746_2.jpg]]

---
# Index
- [[#Chemical Resistive Sensor]]
- [[#How is a Chemical Resistive Sensors Made]]
- [[#Analysis of Two Grains of Material for Chemical Resisitve Sensors]]
- [[#Conclusions]]
- [[#~Ex. Data Sheet of a Hydrogen Gas Sensor]]
---
##### Chemical Resistive Sensor
![[Pasted image 20230718200219.png]]
- **Sensitivity** means that the variation of resistivity is very high, with respect to the variation of concentration. 
- **Selectivity** means "which chemichal compound we can detect".
- ==This is more like a **detector** than a real sensor, because it usually doesn't show large accuracy, but it's a sensor which shows, instead, very high sensitivity, low selectivity==
- $C$ : could be oxygen, it could be nitrogen dioxide, it could be carbon monoxide, ...
- The output is a resistance, which is a function of this concentration here. 

![[Pasted image 20230718200234.png]]
- $\alpha$: sensitivity
- $\alpha_x$: sensitivity to a differnt compound ($x$).<br>$\alpha_x \neq 0$ ⇒ This devices are **NOT** selective.
- It's highly non-linear, non-constant.<br>So ==this kind of device has **no linear behavior**==.<br>Obviously, if as usual, we consider very small range for the input quantity, we will have an almost linear behavior for the output quantity. 

---
##### How is a Chemical Resistive Sensors Made
![[Pasted image 20230718200234 - Copia.png]]
- ==They are **THICK** film resistances, so with a thickness, which is usually **around $100$ micrometers**==. 
- ==When we speak about **THIN** film, instead, we think to films, which have a thickness of **less than $10$ micrometers==**.
- We have two electrodes, metal depositions, this may be thin, and on top, the active layer, the material which builds up the sensing device.<br>And usually, this film is not properly ceramic, because it's made up of many different grains, so like powder, which stays together, but ==it has a lot of pores, so that gas can reach all the film in its whole thickness==.
- The thick film resistances is usually ceramic, ==it is inert==, so it doesn't interact with chemical compounds.

On the backside of the ceramic insulator (**inert**) substrate, usually you find a thin or thick film metal resistance, which acts as a heater (using the current we provide). 
![[Pasted image 20230718200255.png]]
- $P_W$ : power of the ovareall device.<br>This power is something that depends on the size of the device.
- $G$ : conductivity ($=\frac{1}{R}$).
- So we can use the temperature at relatively high temperature: in the range $[150°C ,\ 450°C]$.
- ==The reason why it is necessary to bring this resistive sensor to a very high temperature is because the chemical reaction are faster at this higher temperature, which are needed to get the variation of the resistance==. 

---
##### Analysis of Two Grains of Material for Chemical Resisitve Sensors
The principle of operation for this sensor here is based on **absorption**.
![[Pasted image 20230718200308.png]]
- We take only two grains from the thick film, the current has to pass through these two grains. 
- On the surface of these grains here, the gas, which I want to sense, (let's consider oxygen for instance) is absorbed.
- After being absorbed on the surface, there is a transfer of charge from the sensor (from the metal oxide) to the gas, and vice versa.<br>So for instance, oxygen tends to take an electron from the metal oxide, and it traps this electron, this negative charge, on the surface. 
- Now I have a charged species on the surface, with a certain density, which I call $N_S$.
- In these metal oxide semiconductors, there are **defects** which are naturally present which acts as dopants.<br>⇒ ==So at these temperature these intrinsic semiconductors **behave as extrinsic**==.

So we have:
![[Pasted image 20230718200326.png]]
- what happens is that I have depleted the layer under the surface, so it mean that in this layer electrons are no longer present because they have been taken by the assortment compound, which is oxygen in this case.<br>⇒ ==We have a plus charge region under the surface, like in a **diode**==.

So obviously you have a minus charged layer, a positive charged layer, so you have an electrical field, and associated with this electrical field, you have a voltage barrier, which is like this:
![[Pasted image 20230718200335.png]]
- When you place two grains together and you want the current to flow through, at the surface of each grain there is the potential barrier.<br>⇒ ==So only the electrons which have enough energy to overcome this barrier can pass through to the next grain==, and so contribute to the overall current in the film.
- ==This is like a diode==, and for this reason at the end, we can find the conductivity of the film, where:
	- $q V_S$ : height of the potential barrier between each grain of the substrate.
	- $N_S$ : is the density of the absorbed and charged chemical compound.
	- $T_S$ : is the temperature of the sensor.
	- $N_D$ : is the density of dollars.
	- $K$ : the constant of Boltzmann.
	- $\varepsilon$ : the electric permittivity.

---
##### Conclusions
Taken the conductivity formula:$$G = G_0 e^{-\huge\frac{q^2 N_S^2}{2\varepsilon K T_S N_D}}$$
- We see that the temperature of the sensor ($T_S$) has to be kept very, **very constant**, otherwise you have a reaction due to temperature which is of the same intensity as the reaction due to chemical compound concentration.

==The **Selectivity** of these devices is decided by the chemistry, some materials tend to absorb some gases, others instead other gases==. 
So by selecting this specific type of material or the dopants put into the material, you can change which kind of gas is absorbed. 

Also, ==these are sensors which are **not so reproducible**==. 
The processes which happen at the surface are quite not so known. 
The final equation gives only an **approximation** of what really happens, and it can be very different on the basis of different material and different microstructure of the field.<br>⇒ ==Read carefully the data-sheet==.

==One of the most important influence factor is the **humidity** which is the water vapor, always present in the environment==. 
==And also the **change of temperature** may really change the behavior of the sensor==. 

---
##### ~Ex.: Data Sheet of a Hydrogen Gas Sensor
![[Pasted image 20230718200350.png]]
![[Pasted image 20230718200354.png]]
![[Pasted image 20230718200358.png]]
- This sensor is specifically for **hydrogen gas** and it's meant for **detection**.
- ==And you see that in any case the sensitivity to hydrogen is very high but you have **sensitivity also to other gases==**. 
- The response of the sensor is given as a log-log plot. 
- As you can see, we have almost three decades of response variation. <br>So a large sensitivity for this kind of concentration range. 
- And also humidity you see has a deep impact on the behavior as I have told you of the sensor. 
- ==These are ***Low Cost Devices***==.
- ==They have many limitations (***Temperature***, ***Humidity***, ***Selectivity***)==.
- ==But at least they have good ***Sensitivity***==.
