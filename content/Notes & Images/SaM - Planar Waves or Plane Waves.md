##### ***Remeber***:

> A ***plane [[SaM - Ultrasonic Waves|wave]]*** propagates only in a single direction, let's call it $x_1$, and all the variables which describes the waves are **constant on planes perpendicular to $x_1$**. <br>![[Pasted image 20230719131543 1.png|500]]
> 
> When we perform the derivative on $x_2$ and $x_3$, both will result in a $0$, so remember #IMPORTANTE :$${\partial u_i \over \partial x_2} = {\partial u_i \over \partial x_3} = 0$$Using the [[SaM - Elastic Waves and Acustic Waves • Calculation of the Wave Equation|wave equation]]:$$\rho \ddot{u}_j = c_{ijkl}{\partial u_k \over \partial x_j \partial x_l}$$For a **planar wave** we find (specifically for [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic materials]], so that we can use the [[SaM - Collapsed Stiffness Tensor for Isotropic Materials|collapsed stifness tensor]]): #IMPORTANTE  $$\begin{array}{l}  \rho \ddot u_1 =  c_{11}{\partial^2 u_1 \over \partial x_1^2}  \\[3px]  \rho \ddot u_2 =  c_{44}{\partial^2 u_2 \over \partial x_1^2}  \\[3px]  \rho \ddot u_3 =  c_{44}{\partial^2 u_3 \over \partial x_1^2} \end{array}$$Where:
> - $x_1$ direction in which the wave propagates.
> - $\vec u$ direction in which the material or particles that form the wave move. #NOT_SURE_ABOUT_THIS
> 
> If we look at the definitions of [[SaM - Longitudinal Waves or Compressive Waves|longitudinal wave]] and [[SaM - Transverse Waves or Shear Waves|transverse wave]], we can say that the planar wave is a combination of the two. #NOT_SURE_ABOUT_THIS 

---
###### Memory Card
![[Samsung_SaM_Notes_18_240516_152828_1.jpg]]

---
We take into account a **plane wave**, which propagates along $x_1$.
![[Pasted image 20230719131543.png]]
- ***What is a Planar Wave?***
	- A planar wave, also known as a plane wave, is a type of electromagnetic or acoustic wave characterized by the property that the wavefronts, which are surfaces of constant phase, are flat and planar.<br>In other words, a plane wave's wavefronts are parallel planes, and the wave propagates uniformly in a single direction without spreading out as it travels.
- ***What is a Planar Wave?*** (Professor's Explenation)
	- All the variables which describes the waves are constant on plates perpendicular to $x_1$. 
- So the Hooke's formula is much more compact, since we have to evalutated only for $j = l = 1$, where $j$ and $l$ are referning tho this part: $\frac{\partial^2 u_k}{\partial x_j \partial x_l}$ and using the symmetry of $C$, we end up with only 3 formulas (that are not equal to $0$).
- Remeber to not look, or try to make sense of the indecies for the compressed notation for $c$, since for example $c_{44}$ does not refer to 4th dimension.
- **NOTE**: In the first formula we use $c_{11}$ and in the other two we use $c_{44}$ this is because