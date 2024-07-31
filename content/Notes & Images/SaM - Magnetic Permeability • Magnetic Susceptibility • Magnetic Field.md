##### ***Remeber***:

> In a vacum:$$\vec B = \mu_0 \vec H$$In a material:$$\vec B = \mu \vec H$$Or:$$\vec B = \mu_0 (\vec H + \vec M)$$Where:
> - $\mu$ is the **magnetic permeability**, defined as $\mu = \mu_r \cdot \mu_0$.
> 	- $\mu_r = 1 + \mathcal{X}_M$, where $\mathcal{X}_M$ is the **magnetic susceptibility**, ("*suscettività magnetica*") defined similar to the [[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|electric susceptibility]].
> 	- $\mu$ is measured in $\left[\frac{\text{T}\cdot \text{m}}{\text{A}}\right]$
> 	- $\mu_0 = 4\pi \times 10^{-7} \, {\text{T}\cdot \text{m}\over \text{A}}$
> 	- For **non-magnetic materials** such as: *air*, *plastic*, *glass*, *wood*, *copper*: $\mu_r \approx 1$.
> 	- For **magnetic materials** such as: *iron*, *cobalt*, *nickel*: $\mu_r \in [10^2 \div 10^5]$.<br>*~ For example pure iron at $99.8\%$ has a $\mu_r = 2\cdot 10^3$, while if it is pure at $99.95\%$ it has a $\mu_r = 2\cdot 10^5$*. #IMPORTANTE 
> - $\vec B$ : magnetic field density $\left(\left[\text{T}\right] : \text{Tesla}\right)$<br>*Represents the total magneti field*.
> - $\vec H$ : magnetic field intensity $\left(\left[\frac{\text{A}}{\text{m}}\right]\right)$<br>*Represents the magnetic field produced solely by the presence of current (free current) and not influenced by the magnetic properties of materials*.
> - $M$ : magnetization $\left(M = \mathcal{X}_M \cdot H\right)$

---
###### Memory Card
![[Samsung_SaM_Notes_08_240515_123317_1.jpg]]

---
![[Lecture 8_230912_154531_5.jpg]]
- $\mu$ is the **magnetic permeability**
- $\mathcal{X}_M$ is the **magnetic susceptibility**.<br>⇒ Derived from $\vec M$ the **magnetization of the material**.%%it is the magnetic moment per unit volume of the material.%%
- **Note the similarities** with the "[[SaM - Electric Permittivity • Electric Susceptibility • Electric Field|Electrical Domain]]":
	- $\mathcal{X}$ was the **eletric susceptibility**.
	- $\varepsilon$ was the **eletric permittivity**.
	- $\vec E$: **electric field**.
	- $\vec D$: **eletric displacement field**.

- ***What do $\vec B$ and $\vec H$ represent for magnetism, can you help me understand and visualize them?*** (*ChatGPT 3.5*)
	- Sure! In magnetism, $\vec{B}$ and $\vec{H}$ are both vector fields that describe different aspects of the magnetic field.
		1. $\vec{B}$ (**magnetic flux density or magnetic induction**): ==This represents the total magnetic field==, including the effects of both the magnetic material (if present) and free space. It measures the force experienced by a moving charged particle due to its velocity in a magnetic field. $\vec{B}$ is directly related to the strength and direction of the magnetic force exerted on a moving charge or a current-carrying wire.
		2. $\vec{H}$ (**magnetic field intensity or magnetic field strength**): ==This represents the magnetic field produced solely by the presence of current (free current) and not influenced by the magnetic properties of materials==. In other words, $\vec{H}$ characterizes the magnetic field in the absence of magnetic materials. It's essentially the magnetic field that would exist in space if there were no magnetic materials around.
	- To visualize them, imagine a scenario where you have a bar magnet placed on a table:
		- *$\vec{B}$ would represent the total magnetic field produced by the magnet, including both the magnetic effects of the magnet itself and the surrounding space*.
		- *$\vec{H}$ would represent the magnetic field produced solely by the currents (if any) within the magnet, without considering any magnetic materials around it*.
	- In summary, $\vec{B}$ accounts for all magnetic effects, while $\vec{H}$ isolates the contribution of free currents to the magnetic field.
- ***What do $\vec B$ and $\vec H$ represent for magnetism, can you help me understand and visualize them?*** (*ChatGPT 4o*)
	- Certainly! In magnetism, the vectors $\vec{B}$ and $\vec{H}$ represent different, yet closely related concepts within a magnetic field. Let's break them down:
	- ***Magnetic Flux Density ($\vec{B}$)***:
		- **Symbol**: $\vec{B}$
		- **Also Known As**: Magnetic field, Magnetic induction
		- **Unit**: Tesla (T) or Weber per square meter (Wb/m²)
		- ***Definition and Properties***:
			1. **Physical Meaning**: $\vec{B}$ describes the density and direction of the magnetic flux. It represents how much magnetic field is passing through a given area.
			2. **Equation in Vacuum**: In free space, $\vec{B}$ is related to the magnetic field strength $\vec{H}$ by the permeability of free space ($\mu_0$):$$\vec{B} = \mu_0 \vec{H}$$
			3. **Materials Influence**: In materials, the relationship is influenced by the material's permeability ($\mu$):$$\vec{B} = \mu \vec{H}$$   where $\mu = \mu_0 \mu_r$, and $\mu_r$ is the relative permeability of the material.
			4. **Visualization**: The vector $\vec{B}$ can be visualized as the number of magnetic field lines passing through a given area. The denser the lines, the stronger the magnetic field at that point.
	- ***Magnetic Field Strength ($\vec{H}$)***:
		- **Symbol**: $\vec{H}$
		- **Unit**: Ampere per meter (A/m)
		- ***Definition and Properties***:
			1. **Physical Meaning**: $\vec{H}$ represents the magnetizing force. It describes the amount of magnetizing effect produced by an electric current or a magnetic material.
			2. **Equation in Vacuum**: In free space, $\vec{H}$ is directly proportional to the current that produces it, following Ampère's Law:$$\nabla \times \vec{H} = \vec{J} + \frac{\partial \vec{D}}{\partial t}$$Where $\vec{J}$ is the current density and $\vec{D}$ is the electric displacement field.
			3. **Materials Influence**: In materials, $\vec{H}$ helps to determine the magnetization $\vec{M}$:$$\vec{B} = \mu_0 (\vec{H} + \vec{M})$$
			4. **Visualization**: The vector $\vec{H}$ can be visualized as the force that creates the magnetic field. It is often represented by lines around a current-carrying conductor, showing how the field is generated by the current.
	- ***Relationship and Visualization***:
		- **Interaction**: Both $\vec{B}$ and $\vec{H}$ are essential to describe the magnetic properties of materials and fields. While $\vec{B}$ focuses on the magnetic flux through an area, $\vec{H}$ focuses on the magnetizing force creating the field.
		- **Visualizing Together**: In a diagram, $\vec{B}$ can be represented by dense lines indicating flux through an area, while $\vec{H}$ can be shown as arrows indicating the direction and strength of the magnetizing force. In a simple solenoid, for instance:
		- $\vec{H}$ is represented by arrows along the axis of the solenoid, showing the magnetizing force produced by the current.
		- $\vec{B}$ is represented by loops of flux lines around the solenoid, indicating the density and direction of the magnetic field.
	- Understanding $\vec{B}$ and $\vec{H}$ helps in analyzing and designing magnetic systems, from electromagnets to transformers, and is fundamental in fields like electrical engineering and physics.
