##### ***Remeber***:

> ***Piezoelectricity*** (*ChatGPT*):<br>When mechanical stress is applied to a piezoelectric material, the material's internal structure becomes distorted.
> ==This distortion causes a redistribution of electrical charges within the material, leading to the generation of an electric potential across its surfaces==. 
> This phenomenon is known as the direct piezoelectric effect:<br>![[Pasted image 20230719124105.png]]

> - We have seen already two equations for the [[SaM - Piezoelectric Effect|piezoelectric effect]]:$$\left\{\begin{array}{l} \vec{D} = \overline{\overline{\varepsilon^{\tiny T}}} \vec{E} + \overline{\overline{d}} \kern2px \overline{\overline{T}} & \text{(direct piezoelectric effect)} \\ \overline{\overline{S}} = \overline{\overline{s}} \kern2px \overline{\overline{T}} + \overline{\overline{d^{\tiny T}}} \vec{E} & \text{(inverse piezoelectric effect)} \end{array}\right.$$Where:
> 	- ==The first equation describes the ***direct piezoelectric effect***==.
> 	- ==While the second equation describes the ***inverse piezoelectric effect***==.<br>==*The inverse piezoelectric effect states that even if there is no stress applied to a piezoelectric material, but is present an external electrical field ⇒ then we will see a deformation, or strain of the material itself*==
> 	- $\vec{D}$ : ***[[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|Electric Displacement Field]]***, size: $[3\times 1]$.
> 	- $\overline{\overline{\varepsilon}}$ : ***[[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|Electric Permettivity]]***, size: $[1 \times 1]$.
> 	- $\vec{E}$ : ***[[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|Electric Field]]***, size: $[3\times 1]$.
> 	- $\overline{\overline{d}}$ : ***[[SaM - Piezoelectric Coefficient Matrix for PZT|Piezoelectric Coefficient Matrix]]***, size: $[3\times 6]$.
> 	- $\overline{\overline{T}}$ : ***[[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|Stress Tensor or Vector]]***, size: $[3\times 3]$, however we can reduce it to a $[6 \times 1]$, in collapsed notation, since by definition is a symmetrical matrix.
> 	- $\overline{\overline{S}}$ : ***[[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector|Strain Tensor or Vector]]***, size: $[3\times 3]$, however we can reduce it to a $[6 \times 1]$, in collapsed notation, since by definition is a symmetrical matrix.
> 	- $\overline{\overline{s}}$ : ***Compliance Tensor***, or ***[[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|Yieldness Tensor]]***, size: $[6 \times 6]$.<br>***NOTE***: These are the **sizes** we have seen, but they are specific to [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic materials]].<br>since for [[SaM - Definition of Isotropic and Anisotropic Materials|anisotropic materials]] for example the yieldness tensor has 4 dimensions, and not only 2.<br>==Also typically **piezoelectric materials** are **anisotrpic** (***Source***: [Google](https://www.google.com/search?client=opera-gx&q=pzt+isotropic+or+anisotropic&sourceid=opera&ie=UTF-8&oe=UTF-8#:~:text=Piezoelectric%20materials%20are%20anisotropic%3B%20that%20is%2C%20they%20do%20not%20have%20the%20same%20properties%20in%20all%20axes)), take these sizes only as a reference==.
> 	- We have already seen the realtion between ***Stress Tensor*** and ***Strain Tensor***, and we defined it as the [[SaM - Hooke's Law • Collapsed Yieldness Tensor for Isotropic Materials|Hooke's Law]]:$$\left\{\begin{array}{l}    \overline{\overline{S}} = \overline{\overline{s}} \overline{\overline{T}}      \\      \overline{\overline{T}} = \overline{\overline{c}} \overline{\overline{S}}     \end{array}\right.$$Where:
> 			- $\overline{\overline{s}}$ is the ***yieldness tensor***. ("*tensore di cedevolezza*")
> 			- $\overline{\overline{c}}$ is the ***stifness tensor***, ("*tensore di rigidità*") it describes the elastic constants of the material.
> 			- Also $\overline{\overline{c}}$ and $\overline{\overline{s}}$ are inverse of each other.

> We have different materials which show piezoelectric effect: #IMPORTANTE 
> - Quartz $(Si O_2)$ : _small losses_, almost a [[SaM - Complex Electric Permittivity|perfect dielectic]].
> - PZT (_Lead Zirconate Titanate_, _polycrystal_) : _large piezo-coefficients_ $(d_{33} = 500 \ {\text{pC} \over \text{N}})$
> - PVDF (_polymer_) : _low cost_

>  ***Acutally***: #NOT_SURE_ABOUT_THIS (this is my reasoning)
> - The ***quartz*** has: $\varepsilon_r' \approx 4.0,\ \varepsilon_r'' =  0.001$ and $d_{12} \approx 2 \ {\text{pC} \over \text{N}}$.
> - The ***PZT*** has: $\varepsilon_r' \in [500\div 2000],\ \varepsilon_r'' \in  [0.01 \div 0.05]$ and $d_{12} \approx 500 \ {\text{pC} \over \text{N}}$.
> - Their [[SaM - Complex Electric Permittivity|complex electric permettivity ratio]] is almost the same ${\varepsilon_r' \over \varepsilon_r''} \sim 10^{-3}$ but the ***PZT*** has higher $d$ value, meaning if we take into the direct and inverse piezoelectric effect formual, it will result in a higer response given the same electric field $E$ and the same stress value $T$.<br>The same is true for the capacitance value $C_E = \varepsilon {A \over h}$ and charge output $Q = d \cdot F$, the PZT will have higher value for both.<br>==So for "raw performance" the **PZT** is better==.
> - However we have studied how we can vary some characteristics of the quartz, if we [[SaM - Types of Cut Quartzes|cut it in a different way]].<br>Also we have seen how the [[SaM - AT-Cut Quartz|AT-cut quartz]] has a linear relationship between its thickness $(t)$ and the wavelength $(\lambda_{\omega})$: $t \approx {\lambda_{\omega} \over 2}$.<br>==So the quartz give us "more flexibility"==.

---
Here's a table with some properties for quartz, PTZ and PVDF: (*NOT IMPORTANT*)

| Material                                       | $d \ \left(\text{pC}\cdot \text{N}^{-1}\right)$ | $\varepsilon_r$               | $g \ \left({\text{m}^2\over \text{C}}\right)$ | $E \ \left(10^9{\text{N}\over \text{m}^2}\right)$ | $\lambda \ \left({\text{s}\cdot\text{N}\over \text{m}}\right)$ |
| ---------------------------------------------- | ----------------------------------------------- | ----------------------------- | --------------------------------------------- | ------------------------------------------------- | -------------------------------------------------------------- |
| **Quartz** $(Si O_2)$                          | $d_{11}\in [2 \div 3]$                          | $\in [4 \div 5]$              | $5.8 \cdot 10^{-2}$                           | $80$                                              | $2\cdot 10^{-5}$                                               |
| PZT (_Lead Zirconate Titanate_, _polycrystal_) | $d_{33} = 500$                                  | $\varepsilon_{r_{11}} = 2400$ | $2.4 \cdot 10^{-2}$                           | $80$                                              | $7\cdot 10^{-3}$                                               |
| PVDF (_polymer_)                               | $d_{31} = 23$                                   | $12$                          |                                               | $2$                                               | $5\cdot 10^{-2}$                                               |

---

![[Pasted image 20230719124105.png]]
- So remember that piezoelectric effect can be seen in materials which have a **crystal structure**, and this crystal structure is made of **ions**.
- For instance, in the figure you can see the structure of a **PZT material** where the blue spheres are **positive ions, metal ions**, where has the negative spheres, **negative ions, oxygen ions**.
- When the crystal gets deformed, you will have a shift of the two centers of mass, such that polarization appears because the positive charge and the negative charge are "separated" in space.<br>therefore as a macroscopic effect, you will find a **separation of charge**.

The mathematical description of this effect:
![[Pasted image 20230719124117.png]]
- We have two different equations that describes the direct and the inverse piezoelectric effect, this is the first one, called the "**direct piezoelectric effect**".
- $D$ : field ???
- $E$ : electrical field.
- $\overline{\overline{d}}^E\overline{\overline{T}}$: **piezoelectric effect**.
	- $\overline{\overline{T}}$: **stress tensor** (previously called $\sigma$, i changed the name since $\sigma$ is used for conductivity)
	- $\overline{\overline{d}}^E = \overline{\overline{d}}^T = d$ it's a symmetrical tensor. #NOT_SURE_ABOUT_THIS 
- So you can polarize the material either with an **electrical field**, or this is particular for piezoelectric effect and piezoelectric material with an **applied stress**.
- **NOTE**: this is a **static relationship**, and a **linear relationship**.
- **NOTE**: In this formula there is an error, if we consider the second term $\overline{\overline{d}} \overline{\overline{T}}$ its resulting size is $[3 \times 3 \times 3]$ which is not the same size as $\vec D$ which is $[3 \times 3]$

While the **inverse piezo electric effect**:
![[Pasted image 20230923173659.png]]
- $S$ was called before $\varepsilon$ sometimes and it is the strain tensor.<br>Its dimension is 3 by 3 or in collapse notation can sometimes be replaced by a 6 by 1 vector.
- this small $s$ here which is the **inverse of the matrix of the elastic constant**, this is called the **compliance tensor**.
- We are describing our piezoelectric material as an elastic material, it is a crystal so we know that it is true.
- ==The inverse piezoelectric effect and states that even if there is no stress applied to the material, but there is an external electrical then we will see a deformation, a strain of the material itself==.
- I drop this $^E$ and $^T$ for the  $d$ tensor, I put here just $d$ (it is still a 3x3x3 tensor), the measurement unit can be **meter over volt** or **Coulomb divided by Newton**.
- So now we can for instance take this equation here and write it more in a clear manner, so I have the $i$-th component of the displacement field $D$ is equal to:$$D_i = \sum_{j=1}^{3}\varepsilon_{ij} E_{ij} + \sum_{j=1}\sum_{k=1} d_{ijk} T_{ijk}$$

Sometimes instead of using this $d$ coefficient to describe the piezoelectric behavior, we can write this, and now I write it as if it is a scalar, so **1D**:
![[Pasted image 20230719124135.png]]
- $g$ : **voltage piezoelectric coefficients**.
- Originally the $d$ coefficients were called **charge piezoelectric coefficients**.
- For $g$ obviously you have a tensor.


I remember you that we have different materials which show piezoelectric effect:
![[Pasted image 20230719124146.png]]

---