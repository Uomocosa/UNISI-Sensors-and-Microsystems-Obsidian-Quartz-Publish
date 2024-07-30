##### ***Remeber***:

> ==Pure **transverse waves** are possible only in **solids**==.
> If the ==*displacement of the particles are **perpendicular** to the propagation of the wave*==, then it is called a ***transverse [[SaM - Ultrasonic Waves|wave]]***:<br>![[Pasted image 20230719131619.png|500]]
> Using the definition [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|Hooke's law]], we have found [[SaM - Elastic Waves and Acustic Waves • Calculation of the Wave Equation|previously]]:$$\rho \ddot{u}_j = c_{ijkl}{\partial u_k \over \partial x_j \partial x_l}$$We have that a **transverse wave** has:$$\begin{array}{l}  \rho \ddot u_1 =  0  \\[3px]  \rho \ddot u_2 = c_{44}{\partial^2 u_2 \over \partial x_1^2}  \\[3px]  \rho \ddot u_3 = c_{44}{\partial^2 u_3 \over \partial x_1^2} \end{array}$$Where:
> - $x_1$ direction in which the wave propagates.
> - $\vec u$ direction in which the material or particles that form the wave move. #NOT_SURE_ABOUT_THIS <br>==For **transverse waves** we have $\vec u \perp \vec x$==.

---
###### Memory Card
![[Samsung_SaM_Notes_18_240516_152828_1.jpg]]

---
While if the displacement of the particles and wave move in perpendicular directions, we call it a **shear** or **transfers wave**. 
![[Pasted image 20230719131619.png]]
- This waves are present **only in solid**.
- Remeber to not look, or try to make sense of the indecies for the compressed notation for $c$, since for example $c_{44}$ does not refer to 4th dimension.
- Like longitudinal waves they are defined only for $j = l = 1$, where $j$ and $l$ are referning tho this part: $\frac{\partial^2 u_k}{\partial x_j \partial x_l}$, however they do not have a $u_1$ component, we find acceleation only for $u_2$ and $u_3$, as we can see by the formula $$\rho \ddot{u}_{2,\ 3} = c_{44} \frac{\partial^2 u_{2,\ 3}}{\partial x_1^2}$$Again for the derivative of $u_2$ and $u_3$ over $x_1$ we multiply it by the coefficent $c_{44}$.<br>⇒ So the only difference between longitudinal waves and transverse waves (looking at the formulas) is that: ==longitudinal waves have a $\rho \ddot{u}_{1} = c_{11} \frac{\partial^2 u_{1}}{\partial x_1^2}$ component while for transvere waves $\rho \ddot{u}_{1} = 0$==.
- **NOTE**: #NOT_SURE_ABOUT_THIS 
	- $c_{11}$: **represents the elastic constant associated with the longitudinal (compression or dilatation) deformation of the material**.<br>It characterizes the material's resistance to changes in volume due to compression or expansion along the same direction as the applied stress.
	- $c_{44}$: **represents the elastic constant associated with shear deformation**.<br>It characterizes the material's resistance to shearing forces that cause changes in the shape of the material without changing its volume.
- ***What are Transverse Waves?*** (ChatGPT)
	- A transverse wave is a type of mechanical wave where the particles of the medium move perpendicular to the direction of the energy transfer.
	- In other words, the oscillations or vibrations of the particles occur in a direction that is perpendicular to the wave's propagation.