##### List of things to memorize:
![[SaM - Stress and Strain • Strain and Stress]]

---
###### [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector]]
- *"Stress" ⇒ "Stress*"
- *"Strain" ⇒ "Deformazione"*
- ***Stress***:$$\begin{array}{l} \text{Monodimensional :} & \sigma = {\large\frac{F}{A}} \\[5px] \text{In higher dimensions :} & T_{ij}  = \lim_{\Delta A(j) \to 0}\kern3px{\large\frac{F_i}{\Delta A(j)}}   \end{array}$$
- ***Strain***:$$\begin{array}{l} \text{Monodimensional :} & \varepsilon = {\large\frac{\Delta x}{x_o}} \\[5px] \text{In higher dimensions :} & \varepsilon_{ij} = {\large \frac{1}{2}\left(\frac{\partial u_i}{\partial x_j} + \frac{\partial u_j}{\partial x_i}\right)}  \end{array}$$
- ***Terminology***:
	- $\sigma$, $\sigma_{ij}$, $T_{ij}$ : stress.
	- $\varepsilon$, $\varepsilon_{ij}$, $s_{ij}$ : strain.
	- $F$ : force.
	- $A$ : area.
	- $\Delta A(j) \to 0$ : ==an infinitesimal small surface area of the solid, perpendicular to the "*normal vector*" $\vec n_j$==.
	- $\Delta x$ : displacement.
	- $\vec u$ : **strain direction vector**, so ==in which direction the strain is applied==.<br>While $x_k$ : $k$-th axis.

---
###### [[SaM - Young and Poisson Modulus]]
- ***Young Modulus***:$$E = {{F \over A} \over {\Delta l \over l}} = {\sigma \over \varepsilon_{\parallel}}$$
- ***Poisson Modulus***:$$\nu= - {{\Delta r \over r} \over {\Delta l \over l}} = {\varepsilon_{\perp} \over \varepsilon_{\parallel}}$$
- ***Terminology***:
	- $F$ : force.
	- $A$ : area.
	- $r$ : radius.
	- $l$ : lenght.
	- $\sigma$ : stress
	- $\varepsilon$ : strain.
		- $\varepsilon_{\parallel}$ : parallel strain.
		- $\varepsilon_{\perp}$ : perpendicular strain.

---
###### [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials]]
$$\sigma_{ij}=\sum_{k=1}^{3}\sum_{l=1}^{3}c_{ijkl}\cdot\varepsilon_{kl}$$Or:$$\varepsilon_{ij}=\sum_{k=1}^{3}\sum_{l=1}^{3}s_{ijkl}\cdot\sigma_{kl}$$
- ***Hooke's Law for Isotropic Materials***:$$\sigma_i = c_{ij} \cdot \varepsilon_{j}$$Or:$$\varepsilon_i = s_{ij} \cdot \sigma_j$$
- ***Terminlogy***:
	- $\sigma_{ij}$ : [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|stress]].
	- $\varepsilon_{ij}$ : [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|strain]].
	- $c_{ijkl}$ is the **elastic constant** (depends on the material), and comes from the **Stifness Tensor** (*In Italian "Tensore di Rigidezza"*)
	- $s_{ijkl}$ is the **yieldness constant** (depends on the material), and comes from the **Yieldness Tensor** (*In Italian "Tensore di Cedevolezza"*)
	- $c_{ij}$ refers specifically for the [[SaM - Collapsed Stiffness Tensor for Isotropic Materials|collapsed stiffness tensor]]:<br>If we expand the terms:<br>![[Pasted image 20240207105453.png]]
		- $c_{11} = c_{22} = c_{33}= \lambda + 2\mu$
		- $c_{12} = c_{13} = c_{23}=\lambda$ (**lame modulus**)
		- $c_{44} = c_{55} = c_{66}=\mu$ (**shear modulus**)
	- While $s_{ij}$ to the **collapsed yieldness tensor**:<br>![[Pasted image 20240206191557.png]]

---
![[SaM - MEMORIZE (Base Knwoledge on Sensors)#SaM - Definition of Isotropic and Anisotropic Materials]]
###### [[SaM - Collapsed Stiffness Tensor for Isotropic Materials]]
**Collapsed stiffness tensor**:<br>![[Pasted image 20230719131518 1 1.png]]
- $c_{11} = c_{12} + 2\kern2.5pxc_{44}$
- Or we can write:
	- $c_{11} = \lambda + 2\mu$
	- $c_{12} = \lambda$ (**lame modulus**)
	- $c_{44} = \mu$ (**shear modulus**)

While the **collapsed yieldness tensor**:<br>![[Pasted image 20240206191557.png]]

---