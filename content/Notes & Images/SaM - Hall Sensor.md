##### ***Remeber***:

> A magnetic sensor with a different principle with respect to [[SaM - Eddy Currents • Eddy Probe|eddy currents]], [[SaM - LVDT Sensor (Linear Variable Differential Transformer) • Transformers • Magnetic Induction|LVDT sensors]] and [[SaM - Variable Transformers|variable transformers]].<br>For **hall sensors** ==**we are not speaking about magnetic induction**==.
> Here's a basic structure of an hall sensor:<br>![[Pasted image 20230719114550 1 1.png|333]]
> - We consider to have a slice of **conductive material**, the slice has thickness $t$, width $d$ and length $l$, immerged in a [[SaM - Magnetic Permeability • Magnetic Susceptibility • Magnetic Field|magnetic field]] $\vec B$.<br>$\vec B$ could be easily genereated by current $I_B$ in a solenoid. 
> - We let a current $\vec I$ flow through this **conductive material**, and define the angle $\theta$ as the angle between $\vec I$ and $\vec B$.
> - The ==**Lorentz force**== will act on the charge carriers which are moving due to the electrical field.<br>So due to this current $\vec I$, then we will have, a force acting on the free charge which is given by:$$\vec F = q \kern2px \vec v \times \vec B$$Where:
> 	- $\vec v$ : is the velocity, the speed of the free charge moving due to the current.
> - This force acting in the $z$ direction (in general perpendicular to $\vec v$ and $\vec B$), and it will give an accumulation of electrons on one of these sides of the conductive slice.

> Let's make a scheme of what we have said:<br>![[Pasted image 20230719114550 1.png|500]]
> - The last thing to do is "measure the Lorentz force":<br>If we measure the voltage difference between the two "perpendicular" ends of the conductive slice ("perpendicular" with respect to the current $I$ and field $\vec B$), with a **voltmeter**, we will find a voltage which increases at the beginning, until it reaches an equilibrium voltage, a fixed voltage.
> - This "***steady state voltage***" is due to the equilibrium between:
> 	1. The force due to the action of the **magnetic field**.
> 	2. And the force which is instead due to the presence of the **electrical field related to the accumulation of charge**.
> - So when:$$qvB\sin\theta=qE$$We can define $E = \frac{V_H}{d}$, where $V_H$ is the **steady state voltage**.
> - And we'll end up with:$$V_H = v B d \sin\theta$$

> If we perform some calculation we will find that: #IMPORTANTE $$V_H = BI\kern2px{K_H \over t}  \sin \theta $$Where:
> 	- $K_H \triangleq {\large{1 \over nq}}$ is the "***Hall coefficient"***.<br>And since it directly affects the [[SaM - Sensitivity|sensitivity]] and is defined by the material used, we need to choose the right ones, we usually use *germanium* or *copper*. #IMPORTANTE 
> 	- $t$ is the thickness of the conductive slice.

> *And how can I use such a device?*<br>![[Pasted image 20230921224407.png]]
> ([[#Use Cases of the Hall Sensor|Read the notes]])

>Advantages of the Hall Sensor:<br>![[Pasted image 20230719114655.png]]
>- "**The package can be sealed**", so they don't need to be in contact with the environment before measurement, and **so they become insensitive to contaminants in the environment**.
>- **They have large ranges for B and quite large bandwidths**.
>- They are also **low cost devices**.

---
###### Memory Card
###### Memory Card
![[Samsung_SaM_Notes_23_240516_111131_4.jpg]]

---

---
# Index
- [[#Hall Sensor]]
- [[#Use Cases of the Hall Sensor]]
- [[#Advantages of the Hall Sensor]]

---
##### Hall Sensor
Now we go to the last sensor which can be placed in the magnetic field.
And the principle is different because **we are not speaking about magnetic induction**.
This is a magnetic sensor and it is the **hall sensor**:
![[Pasted image 20230719114550.png]]
- So we consider to have a slice of **conductive material**, the slice has thickness $t$, width $d$ and length $l$. 
- Then we consider to let a current $\vec I$ flow through this **conductive material**, which in principle can be **any conductive material**.
- We also consider to have a **magnetic field** $\vec B$, in which the material is immerged.
- We define $\theta$ as the angle between $\vec I$ and $\vec B$.
- The **Lorentz force** will act on the charge carriers which are moving due to the electrical field.<br>So due to this current $\vec I$, then we will have, a force acting on the free charge which is given by:$$\vec F = q \kern2px \vec v \times \vec B$$Where:
	- $\vec v$ : is the velocity, the speed of the free charge moving due to the current.
- This force acting in the $z$ direction (in general perpendicular to $\vec v$ and $\vec B$).
- And this force gives an accumulation of electrons on one of these sides of the conductive slice.<br>⇒ Therefore you have a **non-uniform distribution of charge**.
- If we measure the voltage difference between this two ends of the conductive slice with a **voltmeter**, so along the surface perpendicular to the $z$ axis, then we will find a voltage which increases at the beginning, until it reaches an equilibrium voltage, a fixed voltage.<br>This "***steady state voltage***" is due to the equilibrium between:
	- The force due to the action of the **magnetic field** and the force which is instead due to the presence of the **electrical field related to the accumulation of charge** are equal, so when:$$qvB\sin\theta=qE$$
	- We can define $E = \frac{V_H}{d}$, where $V_H$ is the **steady state voltage**.
	- So we end up with (in the note the $d$ is missing):$$V_H = v B d \sin\theta$$
Continuing:
![[Pasted image 20230921224121.png]]
- Remember:
	- $J = \frac{I}{A}$ in this case $A = td$
	- $\vec J = \vec v n q$
	- $V_H = v B d \sin\theta$
	- And the most important the **hall coefficient**:$$K_H = \frac{1}{n q}$$
	- As you can see the larger is the **density of the carrier** ($n$), the smaller is the sensitivity of the device, so we have to choose the right material.<br>Usually we use *germanium* or *copper*.

---
##### Use Cases of the Hall Sensor

![[Pasted image 20230921224407.png]]
- In this device I can force the current, so my sensor is this slice of semiconductor, a current generator which keeps this current constant, and then I measure the voltage.<br>So $I$ becomes a part of the sensor itself, and $K_H$ is known, I measure $V_H$, and so I can either find $B$ or $B\kern0px \sin\theta$, or if I know $V$, i can find $\sin \theta$.
- in conjunction with a **permanent magnet**, it could be used to measure the **displacement**, so you have to think about a target where you place a permanent magnet, and then your **hall sensor** will measure the intensity of the PM's magnetic field, proportional to the displacement.<br>⇒ *When the target moves the magnetic field, in front of the sensor changes, and the sensor sends that position of the target*.
- This kind of device is likely used in industrial environment, more as a **detector** actually than as a sensor, that means that what is needed is to sense the presence or the absence of the target, not the very accurate distance measurement, and **in fact many hall sensors are logical sensors**.<br>Inside a single **integrated circuit** you have the **hall sensor**, the **current generator**, a front end which has a threshold (a **comparator**), therefore you sense if there is a magnetic field or not, that means the target is in the neighborhood or you don't have any target.
- It could be used for instance to sense the passing of materials in an industrial plant on a rolling device, so to count for instance things which are passing in front of the hall sensor.

Also they can be used as **current detectors/sensors**: in this case here instead of sensing the magnetic field or generating the magnetic field with a permanent magnet, this magnetic field is generated by a current:
![[Pasted image 20230921225724.png]]
- If I place here a coil all around our slice of conductive material, if a current $I_B$ flows through the coil.
- A current flowing through a coil will generate a $B$ filed, which will be the field we use to immerge our hall sensor in.
- We will measure the voltage across the slice, and it will depend on both $I_B$ and $I$.
- One of these two current can be fixed (usually $I$) and the other one can be measured.

---
##### Advantages of the Hall Sensor
![[Pasted image 20230719114655.png]]
- "**The package can be sealed**", so they don't need to be in contact with the environment before measurement, and **so they become insensitive to contaminants in the environment**.
- **They have large ranges for B and quite large bandwidths**.
- They are also **low cost devices**.

---