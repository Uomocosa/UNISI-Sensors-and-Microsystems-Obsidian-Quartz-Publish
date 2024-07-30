##### ***Remeber***:

> [[SaM - MOSFET|MOSFET]]

> Here is a scheme of a **MOSFET**: #NOT_SURE_ABOUT_THIS <br>![[Pasted image 20230610200311.png|500]]
> Here another one:<br>![[Pasted image 20240113114020.png]]
> Finally here's a [video](https://www.youtube.com/watch?v=rkbjHNEKcRw) on how a MOSFET works.

> Take a thin film of $n$-type doped silicon and place metal lines at both ends, like so:<br>![[Pasted image 20230610200459 1.png]]
> We can feed it a current from the metal ends, and we define it like so:$$\vec J =  \left<J_1,\ 0,\ 0\right>$$Then we apply a [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|stress]] across two direction, with respect to the current:$$\vec \sigma = \left< \sigma_1,\ \sigma_2,\ 0,\ 0 ,\ 0 ,\ 0  \right>$$So no **shear stress**, only **extensive or compressive stress**.
> If we want to calculate the [[SaM - Piezoresistivity Effect in Details|piezoresisitve effect]] brought by this strain, and current, we can say that:$$\vec E = \rho_e \kern0px\cdot\kern-1px \left( \overline{\overline{I}} + \overline{\overline{\pi}}\cdot\overline{\overline{\sigma}} \right) \cdot \vec J$$Where $\overline{\overline{\pi}}$ is the [[SaM - Piezoresistivity Effect in Details|piezoresistive coefficient matrix]], specifically for *silcon* it is defined like so:<br>![[Pasted image 20230610193407.png|500]]

> The previous formula holds true if the applied stress follows the [[SaM - Crystallographic Axis|crystallographic axis]] of the silicon crystal, meaning: the axis on which we apply the stress coincide with the crystallographic axis, so:$$\begin{array}{l} x_{1_\text{STRESS}} = x_{1_\text{CRYSTALLOGRAPHIC}} \\ x_{2_\text{STRESS}} = x_{2_\text{CRYSTALLOGRAPHIC}}\end{array}$$However if it is not the case, we need to **rotate** the $\overline{\overline{\pi}}$ tensor, to do this we can simply calculate:$$\pi' = N^{-1} \kern2px \pi \kern2px N$$Where: $N$ is the rotation matrix.

> If instead we apply an uniaxial stress:$$\vec \sigma = \left< \sigma_1,\ 0,\ 0,\ 0 ,\ 0 ,\ 0  \right>$$The final formula would be:$$E_1 = \rho_e \kern2px (1+G \varepsilon_1) \kern2px J_1 $$Where:$$G = \pi_{11}' \cdot E$$**NOTE**:
> 	- $E$ is the [[SaM - Young and Poisson Modulus|Young modulus]].<br>A common value for the **Young modulus** in this direction $(100)$, for this sensors, is $130$ **GPa**, so we'll find at the end a $G$ factor which is quite large. #IMPORTANTE 
> 	- $E_1$ is the [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|electric field]].
> 	- $\varepsilon_1$ is the [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|strain]].
> 	- $G$ is called the **gauge factor**, we have defined it when talking about [[SaM - Metal Strain Gauge • Passive Strain Sensor|strain gagues]].

> So if we calculate the voltage:$$V = R_0 \kern2px (1+G \varepsilon_l) \kern2px I$$Where: $\varepsilon_l = \varepsilon_1$ is the **longitudinal strain**.

> What happens if we change the direction of $I$ with respect to the voltage reading, and also if we change the [[SaM - Crystallographic Axis|crystallographic axis]] of the *silicon* crystal:<br>![[Pasted image 20230611121245.png]]
> - $\pi_{ij}$ : relative piezoresistive coefficient (transverse and longitudinal).
> - ==You can see that you can either measure a **voltage along the direction of the current**, or the **perpendicular to the direction of the current**==. 

---
###### Memory Card
![[Samsung_SaM_Notes_11_240515_173535_2.jpg]]

---
# Index
- [[#p-Type Substrate Composition]]
- [[#Piezoresistivity on Planar Stress]]
- [[#Rotated Matrix]]
- [[#Uniaxial Stress]]
- [[#Piezoelectric Longitudinal Coefficient]]

***
##### p-Type Substrate Composition
![[Pasted image 20230610200311.png]]

---
##### Piezoresistivity on Planar Stress
![[Pasted image 20230610200459.png]]
![[Pasted image 20230610200529.png]]

current density vector:
![[Pasted image 20230610200707.png]]

stress tensor, we apply stress only in two directions, **planar stress**:
![[Pasted image 20230610200726.png]]
![[Pasted image 20230610200755.png]]
![[Pasted image 20230610200827.png]]

So in this case, I can write the relationship we have found before:
![[Pasted image 20230610200929.png]]

But If $x_1$, $x_2$ are rotated with respect to the crystallographic axis, 
simply when creating the resistors I rotate it with respect to the crystallographic axes:<br>![[Pasted image 20230610201101.png]]

==So if $x_2$ and $x_1$ are rotated with respect to the crystallographic axis, I have to change the $\Pi$ matrix, and I have to replace it with the matrix $\Pi'$ which is the rotated version of the "normal" resistive coefficient matrix==:<br>![[Pasted image 20230610201227.png]]

The rotated matrix does not maintain the same symmetry:<br>![[Pasted image 20230610201257.png]]
- So we may have some non-zero elements where we expected the zero. 
- So it loses the shape, the symmetry seen above. 
- It can be for instance a **full** matrix.

---
##### Rotated Matrix
So the more general formula accounting for the Rotation Matrix:
![[Pasted image 20230611120300.png]]
Where:
![[Pasted image 20230610201227.png]]

---
##### Uniaxial Stress
Obviously, if we are looking at what happens when I have a **uniaxial stress**:<br>![[Pasted image 20230611121023.png]]
![[Pasted image 20230611121038.png]]
- $G$  is the gauge factor for a piezo resistive strain gauge. 

So for piezoresistances we have found an expression which is similar to what we have found for strain gauge made of metal and this is what we found:<br>![[Pasted image 20230611121336.png]]<br>![[Pasted image 20230611121413.png]]
- $\varepsilon_{l}$ : longitudinal
- Voltage drop $E_1$

$E_1$ is proportional to the base resistances, because this is strictly related as we have seen to the current flow:<br>![[Pasted image 20230611121556.png]]


And this time the gauge factor is the product of the **Young modulus** ($E$) times the piezo coefficient in the right direction:<br>![[Pasted image 20230611121657.png]]<br>And since the Young modulus in this direction here ($(100)$), for silicon, is equal to $130$ **GPa**, you'll find again at the end a $G$ factor which is quite large. 

---
##### Piezoelectric Longitudinal Coefficient
So here is what happens in different cases with piezoresistances which are oriented according to the vector below each image:<br>![[Pasted image 20230611121245.png]]
Also you can see the relative piezo coefficient $\pi_{ij}$ (transverse and longitudinal)
==And you can see that you can either see a **voltage along the direction of the current**, or the **perpendicular to the direction of the current**==. 
