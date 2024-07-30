##### ***Remeber***:

> _**Piezoresisitivity** : by applying a preassure on a material we will change its lattice structure, so the [[SaM - Drift Current • Current Density Equation|average free path]] will change, then the [[SaM - Conductivity and Mobility of Intrisinc Silicon|conductivity]] and [[SaM - Recap of Basic Components • Resistance, Capacitance, Inductance • Resistivity, Permittivity, Permeability|resisitvity]] of the material will change as well_.

> For **metals** the changes in its resisitivity, due to [[SaM - Piezoresistivity Effect in Details|piezoresisitivity]], is calculated as:$${d\rho \over \rho} = c {dV \over V}$$So if we also account for the variation of resisitivity given by the [[SaM - Recap of Basic Components • Resistance, Capacitance, Inductance • Resistivity, Permittivity, Permeability|basic formula of resistivity]], we get: #NOT_SURE_ABOUT_THIS $${d\rho \over \rho} = {dl \over l}\left(c+1 \right)+ {dS \over S}\left( c-1\right)$$We have considered metals as [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic materials]]. #NOT_SURE_ABOUT_THIS 

> While for Semiconductor, specifically for *[[SaM - Doping of Silicon|doped Silicon]]* (an [[SaM - Definition of Isotropic and Anisotropic Materials|anisotropic material]]), the piezoelectricity effect has to consider also the direction of preassure, to do this we use tensors:$${d\vec\rho \over \rho_0} = \overline{\overline{\Pi}}\cdot\overline{\overline{c}}\cdot\overline{\overline{\varepsilon}}$$Where:
> - $\overline{\overline{\Pi}}$ is the [[SaM - Piezoresistivity Effect in Details|piezoresistive coefficent tensor]].
> - $\overline{\overline{c}} \cdot \overline{\overline{\varepsilon}} =\overline{\overline{\sigma}}$ is the [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|Hooke's law]].
> 	- $\overline{\overline{c}}$ : stifness tensor (we have seen the [[SaM - Collapsed Stiffness Tensor for Isotropic Materials|stiffness tensor for isotropic materials]]).
> 	- $\overline{\overline{\varepsilon}}$ : [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|strain]] matrix (or displament matrix).
> 	- $\overline{\overline{\sigma}}$ : [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|stress]] matrix.
> - We represent everthing with tensors, since the piezoresistive effect can change depending on the direction of the strain applied to the material, this way we also account for [[SaM - Definition of Isotropic and Anisotropic Materials|anisotropic materials]].

---
###### Memory Card
![[Samsung_SaM_Notes_11_240515_173535_1.jpg]]

---
![[Lecture 6_230911_165051_9 1.jpg]]
- This formula can be furhter improved, since we can write $V = l\cdot S$, then:  #NOT_SURE_ABOUT_THIS $${d\rho \over \rho} = c\left({dl \over l} + {dS \over S}\right)$$Where:
	- $l$ is the lenght of the metal.
	- $S$ is the surface area of the metal.
- **NOTE**: This formula functions only for [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic]] metals (most of them are).
- **NOTE**: An increase of surface area **increases the resistivity ($\rho$)**, while also in metals an increase of surface area **decreases the resistive value ($R$)**, as we know from the [[SaM - Recap of Basic Components • Resistance, Capacitance, Inductance • Resistivity, Permittivity, Permeability|basic formula of resistance]] ($R = \rho \frac{l}{S}$).<br>So from the same deformation we also get: #NOT_SURE_ABOUT_THIS$${d\rho \over \rho} = {dl \over l} - {dS \over S}$$Then the complete variation is given by #NOT_SURE_ABOUT_THIS :$${d\rho \over \rho} = {dl \over l}\left(c+1 \right)+ {dS \over S}\left( c-1\right)$$
- **NOTE**: (*NOT IMPORTANT*)<br>Some metals display piezoresistivity that is much larger than the resistance change due to geometry. <br>==In platinum alloys, for instance, piezoresistivity is more than a factor of two larger, combining with the geometry effects to give a strain gauge sensitivity of up to more than three times as large than due to geometry effects alone==. <br>Pure nickel's piezoresistivity is -13 times larger, completely dwarfing and even reversing the sign of the geometry-induced resistance change.<br>**Source**: [Wikipedia](https://en.wikipedia.org/wiki/Piezoresistive_effect#:~:text=Some%20metals%20display,induced%20resistance%20change.)

For semiconductor the variation of volume is not so significative, so we can reduce the formula to:
![[Lecture 6_230911_165051_9 2.jpg]]

---
![[Pasted image 20240227183559.png]]