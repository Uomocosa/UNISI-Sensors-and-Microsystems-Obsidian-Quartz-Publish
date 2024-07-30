- ***What is the Continuity Equation for Charge Carriers?***:
	- The continuity equation for charge carriers in an electrical current is a fundamental concept in electromagnetism.
	- **It describes the conservation of charge in a conducting medium**.

The formula for the Continuity Equation for Charge Carriers (specifically in this case electrons), is the following:$$\frac{\partial \kern2px n'}{\partial\kern2px t} = \frac{1}{q_e}\nabla \cdot \vec{J}_n + G+\frac{n'}{\tau_e}$$(==*Take it as true*==).
Where:
- $n' = n-n_0$ and it's the **variation of density of charge carriers** (or **density of free electrons**)
- $\nabla \cdot \vec{J}_n$ is the  **divergence of the current density** or **transport current** ($\vec{J}_n$), indicating the net flow of charge out of or into a volume.
	- **REMEMBER** that a divergence of a vector $\vec v$ is defined as:$$\nabla \cdot \vec{v} = \frac{\partial v_x}{\partial x} + \frac{\partial v_y}{\partial y} + \frac{\partial v_z}{\partial z}$$
- $G$ is the **generation of charge due to thermal energy**.
- $\large{ n' \over \tau_e}$ is the **recombintion**.

---
- ***What is the Transport Current?***:
	- 

$$\vec{J}_n = \sigma_n \vec{E} + qD_n (\nabla n)$$Where:
- The first term: $\sigma_n \vec{E}$, represents the **drift current density**.<br>This part of the current is due to the motion of electrons in response to the electric field $\vec{E}$.<br>**It follows Ohm's law, where current is directly proportional to the electric field**.
- The second term: $qD_n (\nabla n)$, represents the **diffusion current density**.<br>This part of the current is due to the concentration gradient of electrons.<br>**When there is a concentration gradient, electrons tend to move from regions of higher concentration to regions of lower concentration due to diffusion**.
- More specifically each term is: %% fold %%
	- $\vec{J}_n$: This is the electron current density vector. (A/m²).
	- $\sigma_n$: This term represents the electrical conductivity of the material for electrons.<br>It's a material-specific property and measures how well the material conducts electric current. (S/m, where S stands for Siemens).
	- $\vec{E}$: This is the electric field vector. It represents the electric force acting on the charge carriers (electrons) in the material. (V/m).
	- $q$: This represents the **charge of an electron**, which is approximately $1.602 \times 10^{-19}$ **Coulombs**.
	- $D_n$: This term represents the **electron diffusion coefficient**.<br>It describes how quickly electrons move through the material due to diffusion. (m²/s).
	- $\nabla n$ is the **gradient of the density of free electrons**, which measures how the electron concentration changes in space.<br>It is usually measured in electrons per cubic meter (1/m³).
- **REMEMBER** by definition the gradient of $f$ is:$$\nabla f = \left(\frac{\partial f}{\partial x} ,\ \frac{\partial f}{\partial y} ,\ \frac{\partial f}{\partial z}\right)$$

![[Pasted image 20230713162603.png]]
![[Pasted image 20230713162631.png]]
![[Lecture 6_230911_165051_3.jpg]]
![[Lecture 6_230911_165051_4.jpg]]
![[Lecture 6_230911_165051_5.jpg]]
![[Lecture 6_230911_165051_6.jpg]]

