##### ***Remeber***:

> [[SaM - Ultrasonic Waves|Ultrasonic waves]] can be devided in two types:
> - The "***elastic waves***" are waves that propagates in solids.<br>These are also called **pressure wave or stress wave** and are related to the **elastic behavior** of solids.
> - In fluids instead, they are usually called "***acoustic waves***".<br>We talk about acustic waves also for waves that propagate in air or human tissues. 

> To simplify things a lot, in our studies we have considered:
> - Perfect continuous elastic medium.
> - Wave of small intensity, which grants a linear phenomena.
> - No dissipation or loss.

> Here is the setup we have used to describe the propagation trough solids:
> 1. Take a small ideal small cube of volume and we select a generic vertex $P$ on it:<br>![[Pasted image 20230719131407.png|500]]<br>So we define its small voulume as: $\Delta V = dx_1 \cdot dx_2 \cdot dx_3$.<br>Then take a the opposite vertex $(P')$ on the cube, opposite with respect to $P$. 
> 2. Using this small volume, [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|the definition of stress]] $\left(T = {F \over A}\right)$ and the second newton's law $(F = m\cdot a)$, and considering $F = \left< F_1 , 0 , 0 \right>$ for simplicity.<br>Then we describe the force $F_1$ as athe sum of all the stresses multiplide by their corresponing surface $(T_{1j} \cdot \kern3px dx_k \kern3px dx_l)$.<br>Here is the complete formula (*NOT IMPORTANT*):<br>![[Pasted image 20231214185722.png]]<br>$\ddot u_1$ is the acceleration on the axis $1$, since we have considered only $F_1$.
> 3. We perform the limit $\Delta V \to 0$ and we find: $$\lim_{\Delta V \to 0} \rho \kern2px \ddot{u_1} = {\partial T_{11} \over \partial x_1} + {\partial T_{12} \over \partial x_2} + {\partial T_{13} \over \partial x_3}$$
> 4. We define know that the [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|Hooke's law]] is: #IMPORTANTE $$T_{ij}=\sum_{k=1}^{3}\sum_{l=1}^{3}c_{ijkl}\cdot\varepsilon_{kl}$$Where the [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector#Strain (In Higher Dimensions)|strain]] $\varepsilon_{kl}$ is defined as #IMPORTANTE :$$\varepsilon_{kl} = \frac{1}{2} \left( \frac{\partial u_k}{\partial x_l} + \frac{\partial u_l}{\partial x_k} \right)$$
> 5. Using the two formulas (and considering a general force $\vec F = <F_1, ,\ F_2, ,\ F_3>$) we find an usuful **wave equation** that relates a derivative in time with a derivative in space:$$\rho \ddot{u}_j = c_{ijkl}{\partial u_k \over \partial x_j \partial x_l}$$This particular definition is useful when talking about [[SaM - Ultrasonic Waves|ultrasonic waves]].<br>Where: 
> 	- $x_i$ is the $i$-the axis on which ==the waves propagates==. #NOT_SURE_ABOUT_THIS 
> 	- While $\vec u$ defines the ==direction where the particles that compose the wave move==. #NOT_SURE_ABOUT_THIS 
> 	- For [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic materials]] we have defined the [[SaM - Collapsed Stiffness Tensor for Isotropic Materials|collapsed stifness tensor]].

---
###### Memory Card
![[Samsung_SaM_Notes_18_240516_152828_1.jpg]]

---
![[Pasted image 20230719131352.png]]
- The elastic waves are these waves in solids, usually the name of waves in solids.<br>These are **pressure wave or stress wave** and are related to the **elastic behavior of solid**, elastic behavior. 
- Whereas when we are speaking about waves in fluid, they are usually called **acoustic waves** through fluid, or in general, ultrasonic waves, which gives the overall description of the phenomena. 
- So we think about a **continuous elastic medium**. 

To simplify things, a lot, we consider:
- Perfect ontinuous elastic medium.
- Wave small intensity, which grants a linear phenomena.
- No dissipation or loss

We take a small ideal small volume and we select a generic point $P$:
![[Pasted image 20230719131407.png]]
- Then we take $P'$ a point in the opposite site of the cube with respect to $P$.
- It is a small volume: $\Delta V = dx_1 \cdot dx_2 \cdot dx_3$


Now we try to write the Newton's law for this small volume, which is:
![[Pasted image 20230719131416.png]]
- This force $F$ applied to the volume, which causes the acceleration $a$.
- It will then be resisted by the elastic force, which tends to keep this volume in its own position.
- We want to understand which is the acceleration applied to the small volume. 
- We need to find the result of the force applied to this small portion of our solid $\Delta V$, which is internal to the solid, and we know that the force distribution in the solid is described by the **stress tensor** $T$.

So $F_1$ the $x_1$ component of the force $F$ applied to the whole volume $V$, will be equal to:
![[Pasted image 20230719131439.png]]
- We consider all possible sheer forces in our small solid $\Delta V$, so by taking two opposite points $P$ and $P'$ we can add all the sheer forces apllied at each of the solid ($6$ faces in total, we can call them: $1$, $1'$, $2$, $2'$, $3$, $3'$), all having the same direction of the force $1$ (half will point towards $1$ and the other will point at the opposite direction)
	- **NOTE**: In the drawings $T_{21}$ and $T_{21}'$ are wrongly directioned, they should be pointing in the direction $1$.
	- **NOTE**: In the drawings $T_{13}$ should be called $T_{31}'$.
- Each small force $T_{i1}A$ has its counterpart that causes stress in the material $-T_{i1}A$, this way we can model the "streches"/stress of the material. #NOT_SURE_ABOUT_THIS <br>Professor explonation:<br>"*I try to zoom on the volume and let you understand maybe what happens:<br>So I have to combine $T_{11}$ applied to this face here, with the one applied to the opposite face $T'_{11}$, then I have to combine, let's change color $T_{31}$, $T'_{31}$, $T_{21}$, $T'_{21}$.<br>So I have to take into account all the components along this first direction here*."
- $\rho$ : density of the solid. 
- $\ddot u_1 = a_1$, where $\vec a$ is the acceleration and $\vec u$ the position.

So we can define the limit:
![[Pasted image 20230719131448.png]]
- For $\Delta V \to 0$ is exacty the definition of derivative.

Equal to:
![[Pasted image 20230719131505.png]]
- I write it better: $$\rho \ddot u_j = \sum_{i=1}^{3} \frac{\partial T_{ij}}{\partial x_i}$$Where:
	- $i$ is the normal direction to each normal.
	- $j$ is each component of the force/acceleration.



We can then define the **Hooke's Law**:
![[Pasted image 20230925130532.png]]
- $c_{ijkl}$ : coefficients of the $C$ matrix.
- $\mu_k$ : position along the $k$-direction or axis. 
- $x_l$ : $l$-axis.
%%- **NOTE**: The hooke's law is know as: $F = kx$ where $k$ is the elastic constant, it make sense since we are talking about elastic materials%%
- Let's break down this formula:
	- $i$ $j$, $k$, $l$ all represent the $3$ axis, and can be seen as the combination them
	- $i$ is derived by the first index of the $T$ matrix, we have seen before the example where we studied the $F_1$ component and used all $T_{1j}$, in that case $i = 1$.
	- $j$, $k,$ and $l$ are not derived by anythin in particular.
	- We can define the strain as: $$\varepsilon_{kl} = \frac{1}{2} \left( \frac{\partial u_k}{\partial x_l} + \frac{\partial u_l}{\partial x_k} \right)$$This formula is due to the fact that for **anisotropic materials** (like piezoelectric materials) the shear strain is not $0$, so for $k=l$ the strain is the same definition as before, so $\varepsilon_i = {\Delta x_1 \over x_1}$ or for more complex materials: ${\partial \over \partial x_1}\Delta x_1$, and in this case we defined the displacement as $u_i = \Delta x_i$.<br>Insted if we applied a shear force to the materail, we would need to account for the **sheer strain**.
	- So we can have seen that the realationship between stress and strain like:$$T_{ij} = \sum_k \sum_l c_{ijkl}\cdot \varepsilon_{kl}$$So the stress is the summation of all the strains both perpendicular and paralle to the vector $<i, j>$, it is similar to how we have defined the stress for **isotropic materials**, but this time we need to consider all the strains, not just the parallel one, since we are working with **anisotropic materials**, also the coefficient (previously for isotropic materials called the *Young Modulus* $E$) will not be a single constant, but it will depend on the surface and type of material, it can be represented by a **4D** matrix $C$.
	- Remeber that we have defined for **isotropic materials**:
		- **Young Modulus**: $E = \frac{\sigma}{\varepsilon_{\parallel}}$
		- **Poisson Modulus**: $\nu = - \frac{\varepsilon_{\perp}}{\varepsilon_{\parallel}}$
		- **Stress**: $\sigma = \frac{F}{A}$, where $F$: force, and $A$: area
		- **Strain**: $\varepsilon = \frac{\Delta x}{x}$, where we use the $_\perp$ and $_\parallel$ indices to mean the variation, the axis parallel or perpendicular to the direction of the force.


So we have this structure here, of the full matrix:
![[Pasted image 20230719131518.png]]
- So given $\lambda$ and $\mu$ we can find the whole $C$ matrix.
- If derivete a planar wave which propagates in the $x_1$ direction, in $x_2$ or $x_3$ the result is $0$.
- $C$ tensor: "***stiffness tensor***" or "***elasticity tensor***", due to symmetry the $81$ elements of this matrix can be reduced to $21$ elements for orthotropic materials and $36$ for transversely isotropic materials.<br>In this case we taked as an example an **isotropic medium**, like **Silicon** which only needs $3$ elastic constants, and can be represented with only $2$ indipendent constants.
- **Quartz** instead has $6$ independant components (still very few), other **anisotropic materials** can have more.
- To get an idea, with $c_{11}$, $c_{12}$ and $c_{44}$, we can find:
	- Young Modulus: $$E = \frac{c_{12}}{3}$$
	- Poisson Modulus: $$\nu = \frac{c_{12}}{2(c_{11} - c_{44})}$$


So finally the complete ***Hooke's Law*** is defined as:
![[Pasted image 20230719131526.png]]
- So actually we ==need only **two parameters** to fully describe, the elastic behavior of this kind of isotropic material==. 
- And therefore now we have a simplified version of the equation because we have many zeros here. 
- So in practice for **isotropic materials**, we can always assume $j = l = 1$, for the other cases $j = 2, l = 1$ for example, $c_{ijkl} = 0$
