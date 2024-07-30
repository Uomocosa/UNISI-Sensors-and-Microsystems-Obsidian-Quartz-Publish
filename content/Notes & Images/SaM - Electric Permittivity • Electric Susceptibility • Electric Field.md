##### ***Remeber***:

> - We define the ***Electric Displacement Field*** ($\vec D$) in two similar ways depending on the type of solid, specifically if it is [[SaM - Definition of Isotropic and Anisotropic Materials|isotropic or anisotropic]]:$$\begin{array}{l}\text{Isotropic}:& \vec D = \kern1px\varepsilon \kern1px \vec E     \\     \text{Anisotropic}:& \vec D = \overline{\overline{\varepsilon}} \vec E \end{array}$$Where:
> 	- $\vec D$ is the **electric displacement field** (in italiano: "*campo di spostamento elettrico*").
> 	- $\vec E$ is the **electric field** (in italiano: "*campo elettrico*").
> 	- $\varepsilon$ is the **Electric Permittivity** and we have defined it as:$$\varepsilon = \varepsilon_0 \kern2px \varepsilon_r$$And $\varepsilon_r$ is called the **Relative Permittivity**.

> - The formulas you need to remember about the electric permittivity are:
> 	- $\varepsilon_0 = 8.85 \times 10^{-12} \, {\text{C}^2 \text{m}^2 \over \text{N}}$. #IMPORTANTE 
> 	- $\varepsilon_r = 1 + \mathcal{X}$
> 		- $\mathcal{X}$ : ***Electric Susceptibility***. ("*Suscettività Elettrica*")
> 	- $\vec D = \varepsilon_0 \vec E + \vec P$
> 		- $\left[D \right] = {{\text{C}} \cdot \text{m}^2}$<br>*$\vec{D}$ accounts for all electric effects, including the polarization of materials*.
> 		- $\left[E \right] = {{\text{V}} \over \text{m}}= {{\text{N}} \over \text{C}}$<br>*$\vec{E}$ accounts only for the contribution of free charges to the electric field*.
> 	- $\vec P = \varepsilon_0 \mathcal{X} \vec E$
> 		- $\vec P$ is the ***Polarization Vector***, it is useful since it describes the effect that the material has on $\vec D$.<br>For this reason when we talk about [[SaM - Special Materials for the Electric Permittivity • Paraelectric, Piezoelectric, Ferroelectric|special materials for the electric permittivity]] we plot this formula
> 
> ==Finally, the electric permittivity can depend (with a weak dependance) on **temperature**, **humidity** and also **displacement**==.

> - It is really important to remember some of the **relative permittivity** values:
> 	- Especially for **Air** $(\varepsilon_r \approx 1)$, **Water** $(\varepsilon_r = 80)$ and **PZT** (*Lead Zirconate Titanate*)  $(\varepsilon_r \le 6000)$. #IMPORTANTE 
> 	- Also remember that $\varepsilon_r \in [1 \ (\text{Air}) \div 6000 \ (\text{PZT})]$. #IMPORTANTE 
> - Here instead the complete table<br>![[Pasted image 20230713163249.png|500]]

---
###### Memory Card
![[Samsung_SaM_Notes_07_240515_122355_1.jpg]]

---
# Index
- [[#Complete Formulas for Defining the Electric Permittivity]]
- [[#Things to Remeber from the Formulas]]
- [[#Table of Relative Permittivity of Different Materials]] #IMPORTANTE 

---
##### Complete Formulas for Defining the Electric Permittivity
![[Lecture 7_230912_154519_2.jpg]]
![[Lecture 7_230912_154519_3.jpg]]
![[Lecture 7_230912_154519_4.jpg]]
- **NOTE**: ==Actually $\varepsilon_0 = 8.85 \times 10^{-12} \, {\text{C}^2 \text{m}^2 \over \text{N}}$==.

---
##### Things to Remeber from the Formulas
So, what you need to remember is:
- Linear **Isotropic** Solid:$$\vec D = \kern1px\varepsilon \kern1px \vec E$$
- Linear **Anisotropic** Solid:$$\vec D = \overline{\overline{\varepsilon}} \vec E$$
- Where:$$\varepsilon = \varepsilon_0(1 + \mathcal{X})$$
- Also we can define:$$\varepsilon_r = 1 + \mathcal{X}$$
- The polarization vector is defined as:$$\vec P = \varepsilon_0 \mathcal{X} \vec E$$(Useful to plot $\mathcal{X}$)

$\varepsilon$ depends on:
![[Pasted image 20230927184025.png]]
==And the **electric permittivity** depends on **temperature**, it's a weak dependence usually depends on the **humidity** also==.
==And also on **displacement** sometimes==.

***
##### Table of Relative Permittivity of Different Materials
![[Pasted image 20230713163249.png]]

---
- ***What do $\vec D$ and $\vec E$ represent for electrostatics, can you help me understand and visualize them?***
	- Certainly! In electrostatics, $\vec{D}$ and $\vec{E}$ are both vector fields that describe different aspects of the electric field.
		1. $\vec{D}$ (**electric displacement field**): This represents the electric field produced by free charges in a material medium, as well as by external electric fields. ==It includes the effects of both the free charges and the polarization of the material medium==. $\vec{D}$ is related to the total electric flux leaving or entering a surface.
		2. $\vec{E}$ (**electric field intensity**): This represents the electric field produced solely by free charges (if present) and not influenced by the polarization of materials. In other words, $\vec{E}$ characterizes the electric field in the absence of polarizable materials. It's essentially the electric field that would exist in space if there were no polarizable materials around.
	- To visualize them, consider a scenario where you have a charged parallel plate capacitor:
		- *$\vec{D}$ would represent the total electric displacement field between the plates of the capacitor, taking into account both the effects of free charges on the plates and the polarization of the dielectric material (if present)*.
		- *$\vec{E}$ would represent the electric field produced solely by the free charges on the plates of the capacitor, without considering the polarization effects of the dielectric material*.
	- In summary, ==$\vec{D}$ accounts for all electric effects, including the polarization of materials==, while ==$\vec{E}$ isolates the contribution of free charges to the electric field==.