##### ***Remeber***:

> We have seen different solutions to find the distance of an object of a target with respect to a probe **without contact**:
> - [[SaM - Capacitive Proximity Sensors|Capacitive proximity sensors]].
> - [[SaM - Inductive Proximity Sensor|Inductive proximity sensors]].
> - [[SaM - Eddy Currents • Eddy Probe|Eddy probe]]

> Now we are going to compare the different solution we have seen, in 6 different categories:
> 1. ***Mechanical Load***:<br>$F_C$: Capacitive Load (force needed to get a reading of $V$ volts): $$F_C = -\frac{1}{2}\frac{\varepsilon A}{x^2}V^2 = \frac{1}{2}\frac{CV^2}{x}$$While for inductance, using a DC current source:$$F_L = \frac{1}{2}\frac{N^2 \mu_0 A_g}{x}I^2 = \frac{1}{2}\frac{LI^2}{x}$$==Using common values the force needed for a capacitive probe is $100$ times less than than that need by inductance probe==, so usually: $$F_C \ll F_L$$
> 	- ***In electronics, what is the "Mechanical Load"?*** (*ChatGPT*)
> 		- In electronics, the term "mechanical load" ==**refers to any physical device or component that consumes power from an electrical circuit and converts it into mechanical work**==.<br>This could include **motors**, **actuators**, **pumps**, **fans**, or any other device that performs a mechanical function.<br>The electrical energy supplied to the mechanical load is typically converted into rotational motion, linear motion, or other forms of mechanical energy.<br>Understanding the characteristics of the mechanical load is crucial in designing and analyzing electronic systems, as it affects factors such as power consumption, efficiency, and performance.
> 1. ***Range of Measurement***:<br>For **inductances** ([[SaM - Eddy Currents • Eddy Probe|Eddy current]]), we can speak about a ratio of $1:3$, which refers to **range** with respect to **probe diameter**.<br>For [[SaM - Capacitive Proximity Sensors|capacitances]], instead, we have a $1:8$ **range/diameter** ratio.<br>⇒ ==So the longer range is obtained with inductive solutions==.
> 2. ***Spatial Resolution***:<br>What I sense is an **average** of the distance over a certain area, this area is called "**the spot**".<br>For **inductive** sensors the ratio between **the spot diameter** and **the probe diameter** is $1.3:1$.<br>While for **capacitive** sensors it is $3 : 1$.<br>⇒ ==So if we want to measure the avarage distance in a large area we may opt for an inductive solution, instead if our target is small we may opt for a **capacitive** one==. 
> 3. ***Complexity of Front End***:<br>==Obviously for **capacitive** sensor, the front end is **far more complex**==.<br>In fact, the **inductive probe gies large signals that don't need particular care for** conditioning, for noise and so on.
> 4. ***Environmental Conditions***:

| Eddy currents (_inductive sensors_)                                                                                                                                                                                                                                                                                                                                                                                                                                                | **Capacitive** sensors                                                                                                                                                                                                                                       |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| $\delta$: The target needs to have a minimum thickness.<br><br>Also there is some restriction on target's characteristic: $\mu$ (permeability) and $\sigma$ (conductivity).The **uniformity of the material**, and the **surface type**.<br><br>The target has to be homogeneous in order to be able to use the calibration that we have done with that specific material.<br>⇒ If you change material type or if you have a non-homogeneous material, then you can find problems. | The target is not influential, the target is uniformity is not influential, same for the target's characteristics, surface roughness and so on, because **we only need the target is conductive**.                                                           |
| Then we have the possibility of having an **external magnetic field** which disrupts the measurement.                                                                                                                                                                                                                                                                                                                                                                              |                                                                                                                                                                                                                                                              |
| And finally **temperature**.                                                                                                                                                                                                                                                                                                                                                                                                                                                       | **Temperature is not influential**, unless you go to very high temperature, which can change the directly behavior of the air or the gas in between being to plate, but this is in extreme condition (when $\varepsilon$ becomes variable with temperature)  |
| Tho if I place *dirt*, *humidity*, ..., in between the probe tip and the target, if it has the same permittivity and is not conductive ⇒ **then it doesn't matter**.<br>==For this reason, **inductive** sensors are robust for **industrial applications**==                                                                                                                                                                                                                      | Instead it is influential: **dirt**, **oxidation of the plates**, because it's like placing the different direct there, **humidity** (sometimes) or condensed water (everytime), finally the **electrical field** is also influential for conductive sensors |
> 6. ***Complexity of the Probe Itself***:<br>==For **capacitive** sensor, the probe is just a plate, it is **far less complex** than the inductive probe==.<br>The only problem for capcitive proximity probes, is to ensure there is an **sufficient insulation** between the plate and the shield and so on, so this is the only problem. 
<br>
---
##### Different Solutions for Contactless Probes
We have seen different solutions to find the distance of an object of a target with respect to a probe **without contact**.
So the different solutions: inducted, variable reluctance, eddy current, the ones that we have seen in more detail are proximity sensor, sensors which are meant to measure displacement or distance without contact.
And actually variable reluctance that we have seen are thought for the speed.
Now we are going to compare the different solution we have seen, in 6 different categories:
1. ***[[#Mechanical Load]]***
2. ***[[#Range of Measurement]]***
3. ***[[#Spatial Resolution]]***
4. ***[[#Complexity of Front End]]***
5. ***[[#Environmental Conditions]]***
6. ***[[#Complexity of the Probe Itself]]***

---
###### Memory Card
![[Samsung_SaM_Notes_23_240516_111131_3.jpg]]

---
###### Mechanical Load
![[Pasted image 20230719112812.png]]
![[Pasted image 20230719112820.png]]
- $F_C$: Capacitive Load (force needed to get a reading of $V$ volts): $$F_C = -\frac{1}{2}\frac{\varepsilon A}{x^2}V^2 = \frac{1}{2}\frac{CV^2}{x}$$
- While for inductance, using a DC current source:$$F_L = \frac{1}{2}\frac{N^2 \mu_0 A_g}{x}I^2 = \frac{1}{2}\frac{LI^2}{x}$$Here we use $A_g$ previusly we used $S_g$, they are the exact same.
- Using common values the force needed for a capacitive probe is $100$ times less than than that need by inductance probe, so usually: $$F_C \ll F_L$$
---
###### Range of Measurement
So we take for **inductive** (Eddy Current), we can speak about a ratio of $1:3$, which refers to **range** with respect to **probe diameter**.<br>For capacitance, instead, we have already seen it, we had $1:8$ **range/diameter**.
![[Pasted image 20230719112836.png]]
- So the longer range is obtained with inductive solutions.

---
###### Spatial Resolution
What I sense is an **average** of the distance.<br>I ==sense an average distance over a certain area==, which is called "**the spot**".<br>The spot is the area sensed by the sensor and depends on the shape of the field, and on the shape of the target too.
![[Pasted image 20230719112857.png]]
- As a rule of thumb, for **inductive** sensors the ratio between **the spot diameter** and **the probe diameter** is $1.3:1$.
- So if we want to measure the avarage distance in a large area we may opt for an inductive solution, instead if our target is smaller we may opt for a **capacitive** one. 

---
###### Complexity of Front End
![[Pasted image 20230719112935.png]]
- Obviously **for capacitive sensor, the front end is far more complex**.
- In fact, the **inductive probe gives large signals that don't need particular care for** conditioning, for noise and so on.
- So complexity of content, we see that the ==***capacity***: **High complexity**==.<br>While inductive, usually low complexity.
- It depends on the type of measurement, bu that usually we have this.

---
###### Environmental Conditions
![[Pasted image 20230921130016.png]]
![[Pasted image 20230719112923.png]]
- For **Eddy Currents** (inductive):
	- $\delta$: minimum thickness of the target.
	- target's characteristic: $\mu$ (permeability) and $\sigma$ (conductivity).
	- Also the **uniformity of the material**, and the **surface type**.<br>Rhe target has to be homogeneous in order to be able to use the calibration that we have done with that specific material.<br>⇒ If you change material type or if you have a non-homogeneous material, then you can find problems.
	- Then we have the possibility of having an **External magnetic field** which disrupts the measurement.
	- And finally **temperature**.
	- Tho if I place *dirt*, *humidity*, ..., in between the probe tip and the target, if it has the same permittivity and is not conductive ⇒ **then it doesn't matter**.<br>For this reason, they are robust for **industrial applications**
- For capacitive sensors, we have almost the contrary:
	- the target is not influential, the target is uniformity is not influential, same for the target's characteristics, surface roughness and so on, because **we only need the target is conductive**.
	- And also, **temperature is not influential**, unless you go to very high temperature, which can change the directly behavior of the air or the gas in between being to plate, but this is in extreme condition (when $\varepsilon$ becomes variable with temperature).
	- Instead it is influential: **dirt**, **oxidation of the plates**, because it's like placing the different direct there, **humidity** (sometimes) or condensed water (everytime), finally the **electrical field** is also influential for conductive sensors.

---
###### Complexity of the Probe Itself
![[Pasted image 20230719113010.png]]
- For capacitive, the probe is just a plate, it is far less complex than the inductive probe.<br>The only problem for capcitive proximity probes, is to ensure there is an **sufficient insulation** between the plate and the shield and so on, so this is the only problem. 

---
