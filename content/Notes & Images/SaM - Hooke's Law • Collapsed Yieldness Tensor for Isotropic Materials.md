Simarly to the [[SaM - Young and Poisson Modulus|Young and Poisson Modulus]] in one dimension, we can define a relationship between [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector#Stress (In Higher Dimensions)|stress and strain in higher dimensions]]:

So if we deform a material, an object, **in the elastic regime** (so linear regime), and for **small deformation** we can say: #IMPORTANTE $$\sigma_{ij}=\sum_{k=1}^{3}\sum_{l=1}^{3}c_{ijkl}\cdot\varepsilon_{kl}$$Or:$$\varepsilon_{ij}=\sum_{k=1}^{3}\sum_{l=1}^{3}s_{ijkl}\cdot\sigma_{kl}$$Where:
- $c_{ijkl}$ is the **elastic constant** (depends on the material), and comes from the **Stifness Tensor** (*In Italian "Tensore di Rigidezza"*)
- $s_{ijkl}$ is the **yieldness constant** (depends on the material), and comes from the **Yieldness Tensor** (*In Italian "Tensore di Cedevolezza"*)

For [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic materials]], we will see why, we can reduce the **Hooke's law** to just:$$\sigma_i = c_{ij} \cdot \varepsilon_{j}$$Where: this particular vectors ($\vec \sigma$ and $\vec \varepsilon$) have dimensions $\left[1 \times 6\right]$ and the **[[SaM - Collapsed Stiffness Tensor for Isotropic Materials|collapsed stifness matrix]]** is reduced to just a $\left[6 \times 6 \right]$.<br>The vectors can be reduced from a $\left[ 3 \times 3 \right]$ matrix to a $\left[1 \times 6\right]$ vectors without loss of information, because ==the strain and stress matrix are both symmetrical==.

---
==As it stands the **Stifness tensor** $\overline{\overline{C}}$ (which elements are $c_{ijkl}$) has $81$ constants, however for physcial reason only $36$ of them are **independent**==.
==However for [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic materials]] the indipendent constants are only $2$==.
[[SaM - Collapsed Stiffness Tensor for Isotropic Materials|Here]] you can find the **collapsed stiffness tensor for isotropic materials**.

We can write the ==**Stifness Tensor  $(\overline{\overline{C}})$ for isotropic materials**== is defined, in the collapsed Einstein notation, as:$$\sigma_i = c_{ij} \cdot \varepsilon_{j}$$If we expand the terms:<br>![[Pasted image 20240207105453.png]]
- ***Source***: [Internet](https://solidmechanics.org/text/Chapter3_2/Chapter3_2.htm)
- $c_{11} = c_{22} = c_{33}= \lambda + 2\mu$
- $c_{12} = c_{13} = c_{23}=\lambda$ (**lame modulus**)
- $c_{44} = c_{55} = c_{66}=\mu$ (**shear modulus**)


We have also seen other "*moduluses*" used to describe the **stifness tensor**:
==The **lame modulus** $(\lambda)$, the **shear modulus** $(\mu)$ and the **bulk modulus** $(K)$==, while their definition are *NOT IMPORTANT*, you need to know that they can be defined using the [[SaM - Young and Poisson Modulus|Young and Poisson modulus]]:$$\begin{array}{l} \lambda = {\large{\nu E \over (1 + \nu) (1-2\nu)}} \\[5px] \mu = {\large{ E \over 2(1 + \nu)}} \\[5px] K = {\large{E \over 3 (1-2\nu)}}   \end{array}$$

---

While the ==**Yieldness Tensor  $(\overline{\overline{S}})$ for isotropic materials**== is defined, in the collapsed Einstein notation, as:$$\varepsilon_i = s_{ij} \cdot \sigma_j$$If we expand the terms:<br>![[Pasted image 20240206191557.png]]
- ***Source***: [Internet](https://solidmechanics.org/text/Chapter3_2/Chapter3_2.htm)
- We write the yieldness tensor, instead of the stifness one, since it is more simple.
- $E$ and $\nu$ are the [[SaM - Young and Poisson Modulus|Young Modulus and Poisson Modulus]] respectevely.
- In this course when talking about this matrix we will ignore the effect of temperature variation.
- **NOTE**: how the strain vector is defined: $$\left<\varepsilon_{11},\ \varepsilon_{22},\ \varepsilon_{33},\ 2\cdot\varepsilon_{23},\ 2\cdot\varepsilon_{13},\ 2\cdot\varepsilon_{12}\right>$$And how the stress vector is defined:$$\left<\sigma_{11},\ \sigma_{22},\ \sigma_{33},\ \sigma_{23},\ \sigma_{13},\ \sigma_{12}\right>$$

---
###### Memory Card
![[Samsung_SaM_Notes_09_240516_122356_2.jpg]]

---

%%ORIGINAL NOTES:
![[Pasted image 20231127171415.png]]
- In the first formula we have $\varepsilon_{lk}$, and in the second $\sigma_{kl}$, the pedices of $\varepsilon$ should be inverted to $\varepsilon_{kl}$, as we can see also from the **Einstein notation** of the formula:<br>![[Pasted image 20231127172346.png]]

Using the Einstein Notation:
![[Pasted image 20231127172549.png]]
We see that we can we write a more collapsed or compact notation of this formula with only 6 constants:$$\sigma_i = c_{ij} \kern2px \varepsilon_{j}$$


![[Pasted image 20231127172449.png]]



---

If we expand the formula, using the definition of [[SaM - Definition of Stress and Strain • Definition of Strain and Stress • Stress Vector • Strain Vector#Stress (In Higher Dimensions)|stress and strain in higher dimensions]], and another formula found in the [[SaM - Elastic Waves and Acustic Waves • Calculation of the Wave Equation|"Elastic Waves and Acustic Waves" lecture]]:$$\lim_{\Delta V \to 0} \rho \kern2px \ddot{u_1} = {\partial T_{11} \over \partial x_1} + {\partial T_{12} \over \partial x_2} + {\partial T_{13} \over \partial x_3}$$We can write an usuful wave equation that relates a derivative in time with a derivative in space:$$\rho \ddot{u}_j = c_{ijkl}{\partial u_k \over \partial x_j \partial x_l}$$Here's the original note:<br>![[Pasted image 20230925130532.png|500]]


![[Pasted image 20231127173339.png]]
%%
