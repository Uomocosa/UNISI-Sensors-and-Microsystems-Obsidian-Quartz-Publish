*In Italian:* #IMPORTANTE 
- *"Stress" ⇒ "Stress"*
- *"Strain" ⇒ "Deformazione"*

---
##### Stress (In 1 Dimension)
While for **stress** ($\sigma$) using this formla:$$\sigma = \frac{F}{A}$$Where:
	- $F$ : **force** applied, unit of measaure $\left[N\right]$ (newton), $\left[N = {\text{Kg} \cdot \text{m} \over \text{s}^2}\right]$.
	- $A$ : **surface area** over which the force ($F$) is applied, unit of measure $\left[ {\text{m}^2}\right]$.

---
##### Strain  (In 1 Dimension)
- We can calculate the **strain** ($\varepsilon$) as:$$\varepsilon = \frac{\Delta x}{x_o}$$Where:
	- $x_0$ is the size of a body at rest, unit of measure $\left[ {\text{m}}\right]$.
	- $\Delta x$ is the size of the **deformation**, unit of measure $\left[ {\text{m}}\right]$.

---
##### Stress (In Higher Dimensions)
We define the strain ($T_{ij}$ or $\sigma_{ij}$) as:$$T_{ij} = \sigma_{ij} \triangleq \lim_{\Delta A(j) \to 0}\frac{F_i}{\Delta A(j)}$$Where:
- $F_i$ : $i$-th component of the force vector $\vec{F}$
- $\Delta A(j) \to 0$ : ==an infinitesimal small surface area of the solid, perpendicular to the "*normal vector*" $\vec n_j$==.

We can distinguish between two stresses:
- **compressive or extensive preassure**: $\sigma_{kk}$ (the force is perpendicular to the face)
- **shear stress**: $\sigma_{ij} : i \neq j$.<br>*Here's an example*:<br>![[Pasted image 20231127170922.png]]

Good explenation, especially for visualizing stress in higer dimensions, can be found [here (Youtube)](https://www.youtube.com/watch?v=D6DTb4tXfOQ) (Don't listen, skip through the video)

---
##### Strain  (In Higher Dimensions)
==In higher dimensions both stress and strain are **symmetrical tensors**==.

The complete formula for strain ($s_{ij}$ or $\varepsilon_{ij}$) is given by: $$s_{ij} = \varepsilon_{ij} \triangleq \frac{1}{2}\left(\frac{\partial u_i}{\partial x_j} + \frac{\partial u_j}{\partial x_i}\right)$$Where:
- $\vec u$ is the **strain direction vector**, so ==in which direction the strain is applied==, and $u_k$ is one of the dimension of the strain direction vector.
- $x_k$ is the $k$-th axis.

We can distinguish between two stains:
- **normal strain**: $\varepsilon_{kk}$ (change in lenght along the direction $k$).
- **angular deformation**: $\varepsilon_{ij} : i \neq j$.

==Simple way to understand==:
- **normal strain**: $\varepsilon_{kk}$ provoked by a **compressive or extensive preassure**: $\sigma_{kk}$:<br>![[Pasted image 20240514175527.png|333]]
- **angular deformation**: $\varepsilon_{ij} : i \neq j$, provoked by a **shear stress**: $\sigma_{ij}$:<br>![[Pasted image 20240514175601.png|150]]
- ***Source***: [Youtube](https://www.youtube.com/watch?v=AKsIEe1c4ac) 


Let's make two examples, to better understand the strain formula:
- ***Source***: [Youtube](https://www.youtube.com/watch?v=aKq1xV39d4k)
- ***Extensive or compressive strain***:<br>![[Pasted image 20240206184016.png|500]]
- ***Shear strain***:<br>![[Pasted image 20240206183913.png|500]]

Good explenation, especially for visualizing strain in higer dimensions, can be found [here (Youtube)](https://www.youtube.com/watch?v=AKsIEe1c4ac) (Don't listen, skip through the video)

---
- From this definitions we have (specifically when talking about [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|collapsed yieldness tensor for isotropic materials]]) seen also:
	- Defintion of the **strain vector**: #IMPORTANTE  $$\left<\varepsilon_{11},\ \varepsilon_{22},\ \varepsilon_{33},\ 2\cdot\varepsilon_{23},\ 2\cdot\varepsilon_{13},\ 2\cdot\varepsilon_{12}\right>$$And the **stress vector** is defined:$$\left<\sigma_{11},\ \sigma_{22},\ \sigma_{33},\ \sigma_{23},\ \sigma_{13},\ \sigma_{12}\right>$$
	- [[SaM - Young and Poisson Modulus|Young and Poisson Modulus]].
	- [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|Hooke's Law]].
---
###### Memory Card
![[Samsung_SaM_Notes_09_240516_122356_1.jpg]]
![[Samsung_SaM_Notes_09_240516_122356_3.jpg]]

---