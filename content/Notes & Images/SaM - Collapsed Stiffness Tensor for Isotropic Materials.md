When we talk about [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|Hooke's law]]:$$\sigma_{ij}=\sum_{k=1}^{3}\sum_{l=1}^{3}c_{ijkl}\cdot\varepsilon_{kl}$$As we have said, there is a special case for [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic material]].

The **stiffness tensor** $c$ in the formula should be formed by 84 elements, but for **isotropic materials** (like **Silicon**), it can be collapsed using needs $3$ **elastic constants**, and they can be represented with only $2$ **indipendent constants**:<br>![[Pasted image 20230719131518 1 1.png]]
Where as we have said only 2 are independent variables, and **for example** we can say that:$$c_{11} = c_{12} + 2\kern2.5pxc_{44}$$We have also defined $c_{11}$, $c_{12}$ and $c_{44}$ as: #IMPORTANTE 
- $c_{11} = \lambda + 2\mu$
- $c_{12} = \lambda$ (**[[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|lame modulus]]**)
- $c_{44} = \mu$ (**[[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|shear modulus]]**)

If we expand the **collapsed stifness tensor** we can find: (*NOT IMPORTANT*)<br>![[Pasted image 20240207111119.png]]
**NOTE**: _This definition was found on [the internet](https://solidmechanics.org/text/Chapter3_2/Chapter3_2.htm), the professor has made other definitions, that i don't think are correct.

To get an idea, about what $c_{11}$, $c_{12}$ and $c_{44}$, represent:
- $c_{11}$: **represents the elastic constant associated with the longitudinal (compression or dilatation) deformation of the material**.<br>==*It characterizes the material's resistance to changes in volume due to compression or expansion*== along the same direction as the applied stress.<br>We can see it clearly in the definition of [[SaM - Longitudinal Waves or Compressive Waves|longitudinal wave]].
- $c_{44}$: **represents the elastic constant associated with shear deformation**.<br>==*It characterizes the material's resistance to shearing forces*== that cause changes in the shape of the material without changing its volume.<br>We can see it clearly in the definition of [[SaM - Transverse Waves or Shear Waves|transverse wave]].

> Instead if we consider an [[SaM - Definition of Isotropic and Anisotropic Materials|anisotropic materials]], let's take **Quartz** for instance: it has $6$ independant components (still very few), however other anisotropic materials can have more.

---
##### Professor's Definition
#NOT_SURE_ABOUT_THIS 
In the lectures we have found:<br>![[Pasted image 20230719131518 1.png]]
And:<br>The [[SaM - Young and Poisson Modulus|Young Modulus]]: $$E = \frac{c_{12}}{3}$$And the [[SaM - Young and Poisson Modulus|Poisson Modulus]]: $$\nu = \frac{c_{12}}{2(c_{11} - c_{44})}$$
But the result is not the same as this matrix:<br>![[Pasted image 20240207111119.png]]
- ***Source***: [Internet](https://solidmechanics.org/text/Chapter3_2/Chapter3_2.htm)
